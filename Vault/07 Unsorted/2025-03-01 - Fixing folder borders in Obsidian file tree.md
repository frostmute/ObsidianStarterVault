---
title: Fixing folder borders in Obsidian file tree
category: []
type: 
tags:
  - clippings
author:
  - "[[Aleksei]]"
source: https://technerium.com/fixing-folder-borders-in-obsidian-file-tree/
created:
  - 2025-03-01
description: You might have seen those annoying borders around items in Obsidian file tree:Obsidian applies this effect to an item in the folder tree on right mouse click (context menu action). Due to some reason, the effect is never removed until you restart the app.To disable the visual effect,
image:
---


>This article provides a CSS snippet to fix an issue in Obsidian where folder borders in the >file tree remain highlighted after a right-click context menu action. The fix involves >creating a CSS snippet in the `.obsidian/snippets` folder with the following content: `.tree-item->self.has-active-menu{box-shadow: none;}`. The snippet disables the box-shadow effect that causes the >persistent highlighting.

---
# Fixing folder borders in Obsidian file tree


You might have seen those annoying borders around items in Obsidian file tree:

![](https://technerium.com/content/images/2024/12/Screenshot-2024-12-08-at-1.03.29-AM.png)

Obsidian applies this effect to an item in the folder tree on right mouse click (context menu action). Due to some reason, the effect is never removed until you restart the app.

To disable the visual effect, create a simple CSS snippet (or [download one here](https://technerium.com/content/files/2024/12/folder_border_fix-1.css)):

1. Go to Obsidian Vault/.obsidian/snippets folder. (You can do it from Obsidian: In Obsidian, go to Settings -> Appearance -> scroll down to CSS snippets section -> click on the folder icon).
2. Create a new style file (file extension is css) with an arbitrary name, for example, folder\_border\_fix.css
3. Put the following content into the file:  
`.tree-item-self.has-active-menu{`  
`box-shadow: none;`  
`}`
4. Save the file.
5. In Obsidian, go to Settings -> Appearance -> scroll down to CSS snippets section -> click Reload snippets and you should see the file you just created. Click the toggle to enable snippet and it should resolve the issue.