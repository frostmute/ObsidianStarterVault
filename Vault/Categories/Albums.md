---
tags:
  - music
  - categories
cssclasses: cards
---

```dataview
table without id
	file.link as Album,
	artist as Artist,
    cover as cover,
	genre as Genre
where
	contains(category,this.file.link) and
	!contains(file.name, "Template")
sort rating desc
```