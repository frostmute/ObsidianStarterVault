---
date_created: 2025-02-26
date_modified: 2025-02-26
document_type: meetings
project: Data annotation.tech
description: List of project meetings.
tags: data-annotation.tech meetings
---
[[Projects/Data annotation.tech/Home|Home]] | **[[Projects/Data annotation.tech/Meetings/All Meetings|Meetings]]** | [[Projects/Data annotation.tech/Notes/All Notes|Notes]] | [[Projects/Data annotation.tech/References|References]]
# Meetings
**Create meeting**
```button
name + Add meeting
type note(Projects/Data annotation.tech/Meetings/untitled meeting) template
action project/Project meeting
templater true
class tailwind-button-white
```
```dataviewjs
for (let group of dv.pages('"Projects/Data annotation.tech/Meetings" and !#meetings').groupBy(p => p.meeting)) {
	dv.table(["Name", "Description", "Date created"], 
		group.rows 
			.sort(k => k.file.ctime, 'desc')
			.map(k => [
			k.file.link, 
			k['description'],
			k.file.ctime.year+"-"+k.file.ctime.month+"-"+k.file.ctime.day
			]))}
```

---
[[Projects/Data annotation.tech/Home|Home]] | **[[Projects/Data annotation.tech/Meetings/All Meetings|Meetings]]** | [[Projects/Data annotation.tech/Notes/All Notes|Notes]] | [[Projects/Data annotation.tech/References|References]]