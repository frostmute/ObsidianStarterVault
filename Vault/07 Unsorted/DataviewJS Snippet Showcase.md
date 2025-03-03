---
banner: https://forum.obsidian.md/uploads/default/original/3X/b/a/ba1a1301f580d34a881803aa5ed8cf7ff3cdf0ef.png
category:
  - "[[../00 - CATEGORIES/Clippings]]"
feature: "![[../03 - MEDIA & FILES/f3a93b501fe174018e029c96a8b69a4f_MD5.png]]"
---
---
created: 2024-05-27T14:41:31
source: https://forum.obsidian.md/t/dataviewjs-snippet-showcase/17847/20?u=gibson
author: 
banner: https://forum.obsidian.md/uploads/default/original/3X/b/a/ba1a1301f580d34a881803aa5ed8cf7ff3cdf0ef.png

---
Hi I built a quick script with dataviewjs to collate my daily note lists for my weekly note. It’s using regular expressions and the obsidian API to accomplish this. I’m pretty new to using javascript so any feedback will be appreciated.

```javascript
//Set the beginning and end of the week const beg = moment("2021-05-16") const end = moment("2021-05-22") //The RegEx that does the heavy lifting const er = new RegExp(/##.Lists\n([\s|\S]*)##.[I|D]/g); const re = new RegExp(/(?:####.*\n)(?:[-|\d.].*\n)*/g); /* My Lists look like this ## Lists #### a list - markdown #### another list - [ ] it catches these too */ //Obsidian's API has allows you to grab a file's parent const par = app.vault.getAbstractFileByPath("Daily/2021-05-13.md").parent; //Get the files for the week as a Map const week = par.children.reduce((acc,chil) => { let name = chil.basename; let date = moment(name); if (date >= beg && date <= end){ acc.set(name,chil) } return acc },new Map()) const sortWeek = new Map([...week].sort((a,b) => String(a[0]).localeCompare(b[0]))) sortWeek.forEach((v,k,m) => { let path = app.vault.getAbstractFileByPath(v.path) app.vault.read(path) .then( fileText => { let listText = fileText.match(er) return new Promise((resolve,reject) =>{resolve(...listText)}) }) .then(listText => { const lists = listText.match(re); if (lists !== null){ dv.header(4,k) dv.list(lists) } }) });
```

I’m looking to create a dataview table that I think can only be accomplished with Dataviewjs.

I have Literature Notes that look like this:

I would like to show ALL Literature Notes in a table sorted descending by their “secondary tag” frequency. The secondary tags are all tags that are not “#litnote”. In this example the only secondary tag is “#writing” but some notes have more.

This is so I can find clusters of “Literature Notes” that belong to the same tag. I am at a loss at the moment to figure out how to associate the tags with the notes. I can grab the tags themselves and the notes themselves in js, but not the correlation between the two.

I hope this is clear. Thank you in advance for any help.

[@Azulaloi](https://forum.obsidian.md/u/azulaloi) was looking for a dataview snippet that would give the word count of all pages in a vault with a specific tag. Uses the guts of the Better Word Count Plugin by [@lukeleppan](https://forum.obsidian.md/u/lukeleppan). Works really well with MetaEdit to change the search term. Here is what I came up with: [dataviewjs.wordcountfromtag · GitHub 140](https://gist.github.com/gblakehl/af639cba3c32762576d64c34effaf614)

Thanks for this!, one question.

Where I can know more about those ‘inline metadata fields’? they look simple and amazing ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")

Here’s another thread that shows how an idea evolves and *DataviewJS* is used: [@FiekeB](https://forum.obsidian.md/u/fiekeb) and I were talking about how a recipe data collection could be set up.

## REAL Daily Notes previous/next navigation

Sometimes I have large gaps between my Daily Notes, but still like the idea of having a “previous Daily Note / next Daily Note” navigator at the top.

Now this doesn’t work without actually traversing the file tree, and what’s better for that than *DataviewJS*?

I’m a *little* hesitant of putting such an amount of code into *every* Daily Note, so we *might* have to wait for common includes. Nevertheless, here is the code for those who wish to play around with it. It’s quite robust (doesn’t break when there *is* no previous/today’s/next note, and also works for notes with names different from YYYY-MM-DD).

**It’s also great to use in a folder with weekly or monthly notes,** because it “travels” through all files in “this” folder (and its subfolders) that have either

-   a Dataview-recognizable date in their name, or
-   a `date:` (ISO format) field in their YAML.

**If no note with today’s date can be found, it’ll display a “date hint” in parentheses in the middle**, plus the previous and next notes links (based on today’s date). The “date hint” is shown in the format set in the Daily Notes plugin’s settings, or ‘YYYY-MM-DD’ if the plugin is disabled or no date format has been set.

### Code

````java
```dataviewjs /* previous/next note by date for Daily Notes Also works for other files having a `date:` YAML entry. MCH 2021-06-14 */ var none = '(none)'; var p = dv.pages('"' + dv.current().file.folder + '"').where(p => p.file.day).map(p => [[|[|[p => p[1](|| 'YYYY-MM-DD'; var current = '(' + moment(t|[' + moment(t|[t|[format|[p => p[1](function (p, i|p.file.name, p.file.day.toISODate(|[|[p => p[1]]%20{%20if%20(p[[format|1) + '|[p => p[1]]%20+%20')';%20var%20nav%20=%20[[format)%20+%20')';%20var%20nav%20=%20[[format)%20+%20')';%20var%20nav%20=%20[[).file.day.toISODate()%20:%20luxon.DateTime.now().toISODate();%20//%20Obsidian%20uses%20moment.js;%20Luxon’s%20format%20strings%20differ!%20var%20format%20=%20app[[today%20?%20today[0)]]' : none|[today ? today[0]]; //dv.list(nav|[next ? '[' + next[0]]; //dv.paragraph(nav.join(" · "]]]]; dv.paragraph(nav[0] + ' ← ' + nav[1] + ' → ' + nav[2]]]; ```
````

I’ve left in some commented-out other ways for displaying. You can of course also leave out today’s note in the middle.

Suggestions for optimizing the JS without breaking functionality welcome.

### Screenshots

![Auswahl_015](../03%20-%20MEDIA%20&%20FILES/f3a93b501fe174018e029c96a8b69a4f_MD5.png)

![Auswahl_016](../03%20-%20MEDIA%20&%20FILES/6a673889e39ab29f23556504805ee512_MD5.png)

![Auswahl_017](../03%20-%20MEDIA%20&%20FILES/38c556387cdac3ac93cd846395583113_MD5.png)

### Changelog:

-   2016-06-14
    -   initial version
-   2016-06-14
    -   If it’s unable to pick up a note name for today, will now show a hint at “where” we are in the middle, based on the day format set in the Daily Notes plugin settings.
        
        ![Auswahl_018](../03%20-%20MEDIA%20&%20FILES/524f93f6f453b373029b82c0e516042d_MD5.png)  
        <small>Standard date format “YYYY-MM-DD”</small>
        
        ![Auswahl_019](../03%20-%20MEDIA%20&%20FILES/17aa58e4ddb81499345425ba4323aa19_MD5.png)  
        <small><a href="https://forum.obsidian.md/t/daily-notes-next-previous/4573">Unusual date format <span title="9 clicks">9</span></a> “ww’ DD-MMM (ddd) Y” used by <a href="https://forum.obsidian.md/u/den">@den</a></small>
        

Hi - I’m trying to have dataviewjs show me any open Kanban tasks that are due today *or overdue*. It’s beyond my javascript abilities… does anyone have a suggestion on how to change this code to check for any incomplete tasks that are undated or are <= 2021-06-14 ?

```bash
dv.taskList(dv.pages("[[2021-06-14]]").file.tasks .where (t => !t.completed) .where (t => t.text.includes("2021-06-14")))
```

Here’s a code block that finds any tasks which include a date of the form YYYY-MM-DD and are overdue (i.e. have a date earlier than now). Yes my code is verbose ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")

```javascript
function overdue(t) { let dValidate = moment(t.text, 'YYYY-MM-DD', true); let d = moment(t.text, 'YYYY-MM-DD'); let containsValidDate = dValidate._pf.unusedTokens.length==0 ; let isOverdue = d.diff(moment()) <= 0; return (containsValidDate && isOverdue); } dv.taskList(dv.pages("").file.tasks .where (t => overdue(t)) .where (t => !t.completed))
```

Hi! Im trying to have a daview table in my meeting note with the last 3 meetings from the date of the meeting I’m taking notes…can anybody help me please…Thanks in advance

HI! really nice! im having hard times figuring out what to chance in here for tasks unscheduled and coming in the future…can you advice? Thanks!!!

Here you go. If you just want upcoming, then use the commented-out return statement instead

```javascript
function filter(t) { let dValidate = moment(t.text, 'YYYY-MM-DD', true); let d = moment(t.text, 'YYYY-MM-DD'); let unscheduled = !dValidate._pf.unusedTokens.length==0 ; let upcoming = (!unscheduled) && moment().diff(d) < 0; return (unscheduled || upcoming) // return ( upcoming ); } dv.taskList(dv.pages("").file.tasks .where (t => filter(t)) .where (t => !t.completed))
```

Hey, it may just be that I don’t have access to the repo but that link is giving me a 404. Any chance you have a better one?

Perfect! thanks so much!!!

Hey all,

Looking for some help here. I currently have three types of notes:

1.  Subject
2.  Topic
3.  Excerpt

Each excerpt has a dataview field called Topic that contains a link to a Topic note.

Each Topic note has a dataview field called Subject that contains a link to a Subject note.

What I want is to have two queries on each Subject note. Query 1 would be to show all Topic notes that are linked to the Subject. Query 2 would be all Excerpt notes that are linked to any of the Topic notes from Query 1.

Anyone have any idea how I can accomplish this? Thanks!

**First question**:  
Where/how you create that links? Inline Fields or yaml frontmatter field?  
If in YAML frontmatter, then these links works only as a value in one specific field; if in inline field, then these links working in two ways: associated to the field (as yaml) or as an “Implicit Field”, i.e., as a metadata that Obsidian capture as “Outlinks” or “Backlinks” (depends of the direction) and listed in right pane.  
Depending on this, the queries can be build in different ways.

**Second question**  
Your link structure seems to work in this (inverted) way:  
SUBJECT ← TOPIC ← EXCERPT  
Not in top-bottom way:  
SUBJECT → TOPIC → EXCERPT

Thanks so much for responding!

The fields will be created to allow Dataview to be utilized. For example, I may make a note capturing a quote I read, which would look like the following:

```
----

source: [[ForSelfExamination]]
author: [[SorenKierkegaard]]
primaryTopic: [[faithAndWorks]]

----

 If it is to be works...fine, but then I must also ask for the legitimate yield I have coming from my works, so that they are meritorious. If it is to be grace--fine, but then I must also ask to be free from works-otherwise it surely is not grace. If it is to be works and nevertheless grace, that is indeed foolishness." Yes, that is indeed foolishness; that would also be true [[Lutheranism]]; that would indeed be Christianity. Christianity's requirement is this: your life should express works as strenuously as possible; then one thing more is required- that you humble yourself and confess: But my being saved is nevertheless grace. The error of the [[MiddleAges]], meritoriousness, was abhorred..`
```

I have the primaryTopic field to designate the main topic of the note. I then will use inline links in the actual text to capture supporting topics. As displayed above, faithAndWorks is the primary topic of this note, but Lutheranism is a supporting topic mentioned as well.

So, I then want to be able to go to the faithAndWorks note and create a query that lists all the notes that have faithAndWorks in the primaryTopic field. This is easy enough, and I know how to do this.

Here is where I’m stuck at: On each primaryTopic note, I have a field called Subject that designates what the primaryTopic falls under. For example, the faithAndWorks note would have Christianity as its Subject.

When I go to the Christianity note, I want to be able to create a query (or queries) that lists all the notes that have a primaryTopic field populated with a primaryTopic falling under Christianity. So if I went to the Christianity note, it would list the above example note, since its primaryTopic (faithAndWorks) has Christianity in its Subject field.

Let me know if I’ve thoroughly confused you or not and I will try again!

Well, I’m not an expert in Dataview (and a ‘zero’ in DataviewJS).  
Maybe an expert in dataviewjs can help you in better way than me.  
I understand your ‘logic’ and make all sense. The solution would be more obvious (for me) if your system was build in reversed way: from Subject → Topics → Notes.  
But I accepted your ‘challenge’ and forced me to think in reverse way (as your links system). After some gray matter consumed and some white smoke, I found one possibility:

```lua
## Christianity ```dataview TABLE primaryTopic as Topics, sort(rows.file.link) as Notes WHERE primaryTopic.Subject = [[Christianity]] GROUP BY primaryTopic SORT primaryTopic ASC ```
```

-   this is the query to create in *Christianity* note
-   `primaryTopic` is the field you defined in your notes;
-   `Subject` is the field you defined in Topic files;
-   `Topics` is the name for the topics column (you can choose what you want)
-   `Notes` is the name for the notes column (you can choose what you want)

I’m not sure about this but you can try.

Would you mind elaborating on the way that is more obvious to you (Subject—>Topics—>Notes)? Interested to get your thoughts on it, as your way may indeed make more sense and if so, I can then implement it in my vault ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")
> 