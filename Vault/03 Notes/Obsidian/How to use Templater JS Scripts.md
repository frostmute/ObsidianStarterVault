---
source: https://shbgm.ca/blog/obsidian/how-to-use-templater-js-scripts
---
# How to use Templater JS Scripts

## What is this? 

Instead of writing your Templater JavaScript command directly in the command block (<%* do some JavaScript %>) you can write the JS in a `script.js` file and call that from a Templater command.

## Why would I want to do this? 

Although it does require two files instead of one, you end up with a much cleaner Templater command. The JS file can be written using an actual code editor with proper syntax highlighting and it makes debugging problems easier. My opinion is that this approach, although requiring a bit more setup, is easier for sharing more complex Templater commands with end users.

## Setup 

This guide assumes you already have Templater installed and a Templates folder defined in the Templater Settings.

### 1. Create a TemplaterJS folder inside your vault 

This is the folder where you'll store the `.js` files for Templater to call

### 2. Set the TemplaterJS folder in the Templater Settings 

## Usage 

Now that you've setup your JS folder, it's time to add your first Javascript file. Let's create a simple script that prompts for input and then displays that input in a notification (not super useful in reality, but should show some basics).

### 1. Write .js file 

Open up VSCode or your favourite code editor and create a new file `notice.js` inside the **TemplaterJS** folder in your vault. Paste the following into the newly created file:

```js
async function notice(tp) {
    const text = await tp.system.prompt("What's Good?")
    new Notice(text, 5000)
}

module.exports = notice
```

We'll breakdown this script to understand it below

### 2. Write the Templater Command 

Now that we have our JavaScript, we can write a Templater command that calls it. Create a new note in your **Templates** folder and name it _Notice_. Paste the following (as plain text!):

```
<%* tp.user.notice(tp) %>
```

**A note on file names**

it appears that Templater uses the name of the JS file and not the function name when you call the user command. I suggest naming the file the same as your exported function to avoid confusion.

### 3. Run your new Command 

Open up the Command Palette and choose **Templater: Insert Template**. Chose the new _Notice_ template you just created. A prompt should appear, type in something fun and hit enter. If everything was copy/pasted correctly, you should see a notification pop up with what you typed.

## Break it Down 

So what happened? Let's break this down a bit, so you can understand and maybe start writing you're own scripts!

### The .js file 

`async function notice(tp) {`

We create a new function called `notice`. Whatever we set as parameters to `notice` are the arguments we provide in the Templater command. In this case, we want to run other `tp` methods, so we set a notice(**tp**) parameter. If we wanted to pass other options, we could include additional parameters.

It's an `async` function because we're doing some asynchronous JavaScript. [Read more about async/await here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function).

`const text = await tp.system.prompt("What's Good?")`

Because we passed in `tp`, we can use all of the Templater command methods! In this case we're displaying a prompt.

`new Notice(text, 5000)`

Because our script is running _inside_ Obsidian, we also have access to the full Obsidian API! In this case we're creating a `new Notice` and displaying the `text` provided in the prompt. We could also access anything off of `app` like `app.vault` or `app.workspace`.

`module.exports = notice`

This export line is important! This is how Templater will be able to read the `notice` function we created. Just make sure to export your user function.

### The Templater Command 

Because we've put all our logic inside the `notice.js` file, the Templater Command is pretty simple.

`<%*`

This specific command doesn't have any expected output, that's why we're using the `*` version instead of `<%`. If we wanted to return something from our JS file, we could use the standard Templater syntax.

`tp.user.notice(tp)`

This is calling the function we created in `notice.js`. Two things to note here:

1. All user specified functions with be under `tp.user`
2. Remember how we specified a `notice(tp)` parameter when writing the `notice` function? We're supplying `tp` as an argument when calling the function. We could supply additional arguments if our JS function required them.

## Advanced 

Now that we have the basics, let's look at a more advanced example. We're going to take a command that creates a new block-reference:

```
<%*
let cmEditorAct = this.app.workspace.activeLeaf.view.sourceMode.cmEditor;
let curLine = cmEditorAct.getCursor().line;
cmEditorAct.setSelection({ line: curLine, ch: 0 }, { line: curLine, ch: 9999 });

function createBlockHash() {
let result = '';
var characters = 'abcdefghijklmnopqrstuvwxyz0123456789';
var charactersLength = characters.length;
for ( var i = 0; i < 7; i++ ) {
result += characters.charAt(Math.floor(Math.random() * charactersLength));
}
return result;
}

let id = createBlockHash();
let block = ![[${tp.file.title}#^${id}]].split("\n").join("");
navigator.clipboard.writeText(block).then(text => text);
tR = tp.file.selection() + ^${id}.split("\n").join("");
%>
```

And convert it into a JS file + Command. We won't walk through this, but there will be comments in the codeblocks. Some of the. code will be cleaned up as well, but don't worry about that too much.

### The JS File 

Remember, this needs to be inside your TemplaterJS folder

```js
function addBlockRef(tp) {
    
 //Use the Obsidian API to get the CodeMirror Editor
    const editor = app.workspace.activeLeaf.view.editor
    const cursorLine = editor.getCursor().line
    
//Set the selection in the CodeMirror Editor
    editor.setSelection({line: cursorLine, ch: 0}, {line: cursorLine, ch: 9999})
const id = createBlockHash();
const block = `![[${tp.file.title}#^${id}]]`.split("\n").join("");

// Copy the block reference to the clipboard
navigator.clipboard.writeText(block).then(text => text);

//Return the selected text and the generated block id
return tp.file.selection() + `^${id}`.split("\n").join("");
}

//A simple function to create a random block id
function createBlockHash() {
let result = '';
var characters = 'abcdefghijklmnopqrstuvwxyz0123456789';
var charactersLength = characters.length;
for ( var i = 0; i < 7; i++ ) {
result += characters.charAt(Math.floor(Math.random() * charactersLength));
}
return result;
}

//export the addBlockRef function
module.exports = addBlockRef
```

### The Templater Command 

Remember, this should be plaintext in a note inside your Templates folder.

```
<% tp.user.addBlockRef(tp) %>
```

## A Word on Syncing 

**Update**

Obsidian Sync now supports syncing all file types! The scripts below are no longer needed!.

Obsidian Sync won't sync your `.js` files inside of the _TemplaterJS_ folder. Here is a couple of Templater Commands that will convert the `.js` files to Markdown for syncing and then convert back to `.js` once synced.

### JS File 

Create a file called `sync.js` inside the _Templater JS_ folder.

```js
async function jsToMarkdown({js: jsFolder, md: markdownFolder}) {
  await checkFolder(markdownFolder);
  const jsTemplater = app.vault.getAbstractFileByPath(jsFolder).children;
  jsTemplater.forEach(async (file) => {
    const content = await app.vault.cachedRead(file);
    const mdFile = file.name.concat(".md");
    const mdFilePath = `${markdownFolder}/${mdFile}`;
    const exists = await app.vault.exists(mdFilePath);
    if (exists) {
      const mdFile = await app.vault.getAbstractFileByPath(mdFilePath)
      await app.vault.modify(mdFile, content);
    }
    if (!exists) {
      await app.vault.create(mdFilePath, content);
    }
  });
}

async function jsFromMarkdown({js: jsFolder, md: mdFolder}) {
  await checkFolder(jsFolder);
  const mdTemplater = app.vault.getAbstractFileByPath(mdFolder).children;
  mdTemplater.forEach(async (file) => {
    const content = await app.vault.cachedRead(file);
    const jsFile = file.name.replace(".md", "")
    const jsFilePath = `${jsFolder}/${jsFile}`;
    const exists = await app.vault.exists(jsFilePath);
    if (exists) {
      const jsFile = await app.vault.getAbstractFileByPath(jsFilePath);
      await app.vault.modify(jsFile, content);
    }
    if (!exists) {
      await app.vault.create(jsFilePath, content);
    }
  });
}

//nabbed from @zsviczian's awesome settings sync scripts
const checkFolder = async (folderPath) => {
  const folder = app.vault.getAbstractFileByPath(folderPath);
  if (!folder) await app.vault.createFolder(folderPath);
};

function sync() {
    return {jsToMarkdown, jsFromMarkdown}
}

module.exports = sync
```

### Templater Commands 

Create two notes inside your Templates folder (remember to paste this as plain text):

Convert from `.js` to a markdown file

```
<%* tp.user.sync().jsToMarkdown({js: "TemplaterJS", md: "TemplaterMD"}) %>
```

Convert from a markdown file to `.js`

```
<%* tp.user.sync().jsFromMarkdown({js: "TemplaterJS", md: "TemplaterMD"}) %>
```

The arguments in the above commands allow you to specify folder names in case you're using something different than _TemplaterJS_ or want the markdown sync folder to be named something else.

## Questions? 

Feel free to hit me up on the OMG Discord @shabegom if you have questions or run into problems with any of the above!

I hope this is a good introduction to using custom JavaScript commands in Templater! Enjoy!