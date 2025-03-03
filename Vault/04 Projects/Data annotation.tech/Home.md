---
date_created: 2025-02-26
date_modified: 2025-02-26
document_type: project-dashboard
is_active: true
project: Data annotation.tech
tags:
  - dashboard
  - project
cssclasses:
  - cards
---
**[[Home|Home]]** | [[Notes/All Notes|Notes]] |


# Data annotation.tech
**Description**:: AI Training; prompt creation, analyzation, evaluation, annotation. Freelance Job.
**Link**: [https://dataannotation.tech](https://dataannotation.tech)


## Tasks
*[[Tasks|+ Add a task]]*
```dataviewjs 
dv.taskList(dv.pages('"04 Projects/Data annotation.tech"').file.tasks .where(t => !t.completed))
```

## Notes
```button
name + Add note
type note(Projects/Data annotation.tech/Notes/untitled note) template
action project/Project note
templater true
class tailwind-button-white
```
```dataviewjs
for(let group of dv.pages('"04 Projects/Data annotation.tech/Notes" and !#dashboard and !#notes').limit(10).groupBy(p => p.note)) {
	dv.table(["Name", "Description", "Date created"], 
		group.rows 
			.sort(k => k.file.ctime, 'desc')
			.map(k => [
			k.file.link, 
			k['description'],
			k.file.ctime.year+"-"+k.file.ctime.month+"-"+k.file.ctime.day
			]))}
```
*Only showing the last 10 notes*
*[[Notes/All Notes|View all notes →]]*

---
**[[Home|Home]]** | [[Notes/All Notes|Notes]] |