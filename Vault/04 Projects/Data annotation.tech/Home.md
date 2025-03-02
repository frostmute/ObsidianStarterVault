---
date_created: 2025-02-26
date_modified: 2025-02-26
document_type: project-dashboard
is_active: true
project: Data annotation.tech
tags:
  - dashboard
  - project
  - data-annotation.tech
cssclasses:
  - cards
---
**[[Home|Home]]** | [[Meetings/All Meetings|Meetings]] | [[Notes/All Notes|Notes]] | [[References|References]]
# Data annotation.tech
**Description**:: AI Training Freelance Job
**Link**: *add link (if relevant)*


## Tasks
*[[Tasks|+ Add a task]]*
```dataviewjs 
dv.taskList(dv.pages('"Projects/Data annotation.tech"').file.tasks .where(t => !t.completed))
```

## Meetings
```button
name + Add meeting
type note(Projects/Data annotation.tech/Meetings/untitled meeting) template
action project/Project meeting
templater true
class tailwind-button-white
```
```dataviewjs
for(let group of dv.pages('"Projects/Data annotation.tech/Meetings" and !#meetings').limit(10).groupBy(p => p.meeting)) {
	dv.table(["Name", "Description", "Date created"], 
		group.rows 
			.sort(k => k.file.ctime, 'desc')
			.map(k => [
			k.file.link, 
			k['description'],
			k.file.ctime.year+"-"+k.file.ctime.month+"-"+k.file.ctime.day
			]))}
```
*Only showing the last 10 meetings*
*[[Meetings/All Meetings|View all meetings →]]*

## Notes
```button
name + Add note
type note(Projects/Data annotation.tech/Notes/untitled note) template
action project/Project note
templater true
class tailwind-button-white
```
```dataviewjs
for(let group of dv.pages('"Projects/Data annotation.tech/Notes" and !#dashboard and !#notes').limit(10).groupBy(p => p.note)) {
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
**[[Home|Home]]** | [[Meetings/All Meetings|Meetings]] | [[Notes/All Notes|Notes]] | [[References|References]]