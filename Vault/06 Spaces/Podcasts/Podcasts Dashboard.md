---
banner: ""
date_created: 2025-03-02
date_modified: 2025-03-02
description: Listen to people talking
document_type: dashboard
tags:
  - dashboard
cssclasses:
  - cards
  - page-grid
  - pen-red
---
# Podcasts

## Pages
```dataviewjs
let pages = dv.pages(`"${dv.current().file.folder}" and !"${dv.current().file.path}"`)
if(pages.length > 0){
for(let group of dv.pages(`"${dv.current().file.folder}" and !"${dv.current().file.path}"`).groupBy(p => p.note)) {
	dv.table(["Name", "Description", "Tags"], 
		group.rows 
			.sort(k => k.file.ctime, 'desc')
			.map(k => [
			k.file.link, 
			k['description'],
			dv.span(k.file.tags.values.toString().replaceAll(",", " "))
			]))}
} else {
	dv.el('div', 'No pages')
}

```


