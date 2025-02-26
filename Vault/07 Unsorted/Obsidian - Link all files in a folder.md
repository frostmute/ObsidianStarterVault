---
url: https://freedium.cfd/https://medium.com/@gareth.stretton/obsidian-link-all-files-in-a-folder-39f50bd0e4a8
title: "Obsidian: Link all files in a folder"
author: Gareth Stretton
description: Often I need to quickly access all files in a folder from a note in Obsidian. This article shares how to use a "DataViewJS view" to link to a folder and all of the files it contains.
tags:
  - clippings
  - medium
  - dataview
  - dataviewJS
  - obsidian
  - plugins
published: 
created: 2025-02-25T21:45:11-06:00
---
# 
Often I need to quickly access all files in a folder from a note in Obsidian. This article shares how to use a "DataViewJS view" to link to a folder and all of the files it contains.
Below is an annotated screenshot that shows how to use this view. It shows both the edit and view mode.

### Options

You can provide 3 options:

**folderURI** — This is the path to the folder in 'file URL' format. I use file URL format to avoid issues when there are spaces in the path. I recommend using the plugin '[File to URI Path](https://github.com/MichalBures/obsidian-file-path-to-uri)' to convert paths when you paste them (the default shortcut is funky CTRL + ALT + SHIFT + L… you can change it if needed).

**heading** — (Optional) When provided, the list will be indented and the top element will be a link to the folder.

**filter** — (Optional) When provided, the files will be filter to those which have the provided text in their filename. It will accept a "regular expression" if you want to perform more complicated filtering. Examples include "this|that", "^starts\_with", "ends\_with$", "anything.\*then\_this"

### How to add this custom view

Step 0. Install and enable the DataView Plugin

![None](https://miro.medium.com/v2/resize:fit:700/0*Y_t5wZQIWw-Aspv3.png)

![None](https://miro.medium.com/v2/resize:fit:700/0*926QOukuSrSh-XaX.png)

Step 1. Recommended: Install the "File to URI Path" plugin too

Step 2. Create the folders: view/folder\_items\_as\_links

![None](https://miro.medium.com/v2/resize:fit:700/1*nPuC57j3au2GDVvb2mWNvA.png)

Step 3. Create a file named 'view.js' in this folder

![None](https://miro.medium.com/v2/resize:fit:700/1*z3FvnbYVdwdbFymRVc6UjQ.png)

![None](https://miro.medium.com/v2/resize:fit:700/1*h8eYSYmgr3ngTjNXQqReMA.png)

Step 4. Add the following code to this file…

```undefined
const url = require('url')
const fs = require('fs')
const path = require('path')
function getInput(name) { 
  return (input && input[name]) ? input[name] : dv.current().file.frontmatter[name]
}
let folderURI = getInput("folderURI")
if (folderURI == undefined) {
  dv.header(1, 'Error: folderURI not provided, e.g {folderURI:"file:///C:/"}')
  return
}
let heading = getInput("heading")
let filter = getInput("filter")
let folderPath = url.fileURLToPath(folderURI)
let folderItems = fs.readdirSync(folderPath)
let folderItemsELinks = folderItems
  .filter(item => (filter === undefined) || new RegExp(filter, 'g').test(item))
  .map(itemName => {
    let pathAsURL = url.pathToFileURL(folderPath + path.sep + itemName, "file:")
    return \`[${itemName}](${pathAsURL})\`
})
if (heading) {
  let folderELink = \`[${heading}](${folderURI})\`
  dv.list([folderELink, folderItemsELinks])
} else {
  dv.list(folderItemsELinks)
}
```

Step 5. Use the view in your note

```undefined
\`\`\`dataviewjs
dv.view("views/folder_items_as_links", {
 heading: "Example",
 filter: "cat|plan",
 folderURI: "file:///C:/Example"
})
\`\`\`
```

That's it! In the above usage, a link to 'C:\\Example' will be generated and all files that have 'cat' or 'plan' in their name will have a nested link generated.

### Pro-tips

If you find that you need a set of folders, create a helper view…

The snippet below will use the last 2 digits of the note and create links for 3 subfolders.

```undefined
let sessionNumber = dv.current().file.name.slice(-2)
let classFolder = "file:///C:/class_on_drawing_cats/";
[
  {folderName: "Provided", folderURI: classFolder + "/Provided/Week_" + sessionNumber},
  {folderName: "Creations", folderURI: classFolder + "/Creations/Week_" + sessionNumber},
  {folderName: "Videos", folderURI: classFolder + "/Week_" + sessionNumber}
].forEach(element => dv.view("/views/folder_items_as_links", element));
```

this view can be loaded with:

```undefined
\`\`\`dataviewjs
dv.view('./relative_path_to/your_local_view')
\`\`\`
```

### Sign-off

Hope this saves you time manually creating links to local files! Enjoy :-)

Check out my [other Obsidian Articles](https://medium.com/@gareth.stretton/list/e42182b5ce63) too.