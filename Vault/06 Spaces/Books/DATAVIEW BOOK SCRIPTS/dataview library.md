---
cssclasses:
  - cards
  - myhome
updated: 2022-10-08 05:30:50
aliases:
  - library
created: 2022-08-13 12:45:38
---



```dataview
table without id ("![](" + cover + ")") as Cover,  "<progress value=" + pageprogress + " max="+pagecount+"  class='yellow'>" as progress,file.link as Name, author as Author,publish,rating as Rating
from #book 
sort rating desc

```