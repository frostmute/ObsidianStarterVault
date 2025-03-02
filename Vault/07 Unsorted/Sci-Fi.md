---
tags:
  - movies/genres
cssclasses:
  - cards
---

```dataview
table without id
	file.link as Movie,
	rating as "Rating"
where
	contains(category,[[Movies]]) and
	contains(genre,this.file.link)
sort rating desc
```