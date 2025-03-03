---
created: 2024-11-30
source: https://forum.obsidian.md/t/cards-view-for-dataview-tables/85808
category:
  - "[[Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster](../03%20-%20MEDIA%20&%20FILES/e2aa40b827171c05451eb5f38d48fa83_MD5.jpg)"
tags:
  - clippings
  - csssnippets
  - dataview
  - cardview
  - Obsidian
  - plugins
feature: "![[../03 - MEDIA & FILES/e2aa40b827171c05451eb5f38d48fa83_MD5.jpg]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/e2aa40b827171c05451eb5f38d48fa83_MD5.jpg)


```meta-bind-button
label: Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "001"
style: primary
actions:
  - type: command
    command: editor:fold-all
```

```meta-bind-button
label: Un-Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "002"
style: primary
actions:
  - type: command
    command: editor:unfold-all
```

***

```cardlink
url: https://forum.obsidian.md/t/cards-view-for-dataview-tables/85808
title: "Cards View for Dataview tables - Share & showcase - Obsidian Forum"
description: "I have created my own css snippet for Cards View from Dataview tables. I was inspired by Minimal Cards but they were lacking some things I’d like to see or have. That’s why I’ve written my own snippet and also ability to change styles via Style Settings plugin.  This is how it looks by default in some themes     I tried to implement some basic settings in Style Settings plugin. It has settings for Desktop and mobile versions(mobile activates if width less than 400 points:     Here is a link to G..."
host: forum.obsidian.md
image: https://forum.obsidian.md/uploads/default/optimized/3X/0/4/041e1af5d15361249feef6efdc446432cc2c1f30_2_1024x576.jpeg
```

***

![](../03%20-%20MEDIA%20&%20FILES/e2aa40b827171c05451eb5f38d48fa83_MD5.jpg)

Looks great!

Like it more than the Minimal Cards look.  
Ran into one problem for me though. I have one note where I use horizontal pictures and one note where I use vertical pictures. Would be great if there was some way to control the width via cssclasses in the metadata or something. So setting one single width which is applied to all cards like shown in your Github demo wouldn’t work.

Added this line for myself so I can apply `card-height-120` to the cssclasses property to get the horizontal images to look better:

```css
.cards.card-height-120 table.dataview tbody>tr>td:has(img){ height: 120px; }
```

How hard would it be to make the gap space consistent so it does not change regardless of screen size and amount of elements? And then either align the whole group to the center or start (left).

Otherwise it’s great ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")Thank you for making this!
> 