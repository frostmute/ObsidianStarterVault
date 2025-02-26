---
date_created: 2025-02-26
date_modified: 2025-02-26
document_type: notes
project: Data annotation.tech
description: List of project notes.
tags: data-annotation.tech notes
---
[[Projects/Data annotation.tech/Home|Home]] | [[Projects/Data annotation.tech/Meetings/All Meetings|Meetings]] | **[[Projects/Data annotation.tech/Notes/All Notes|Notes]]** | [[Projects/Data annotation.tech/References|References]]
# Notes
**Create new note**
```button
name + Add note
type note(Projects/Data annotation.tech/Notes/untitled note) template
action project/Project note
templater true
class tailwind-button-white
```
**Flat view**
```dataviewjs
for (let group of dv.pages('"Projects/Data annotation.tech/Notes" and !#dashboard and !#notes').groupBy(p => p.note)) {
	dv.table(["Name", "Description", "Date created"], 
		group.rows 
			.sort(k => k.file.ctime, 'desc')
			.map(k => [
			k.file.link, 
			k['description'],
			k.file.ctime.year+"-"+k.file.ctime.month+"-"+k.file.ctime.day
			]))}
```


**Hierarchical view**
```dataviewjs
for (let group of dv.pages('"Projects/Data annotation.tech/Notes" and !#dashboard and !#notes').groupBy(p => p.file.folder)) {
  let headerLevel = group.key.split("/").length;
  dv.header(headerLevel, `${group.key.replace(group.key.split("/")[0], "").slice(1).replaceAll("/", " / ")}`);  
  dv.table(["Name", "Description", "Date created"],
  group.rows.map(k => [k.file.link, k['description'], k.file.ctime.year+"-"+k.file.ctime.month+"-"+k.file.ctime.day]))
}
```

---
[[Projects/Data annotation.tech/Home|Home]] | [[Projects/Data annotation.tech/Meetings/All Meetings|Meetings]] | **[[Projects/Data annotation.tech/Notes/All Notes|Notes]]** | [[Projects/Data annotation.tech/References|References]]