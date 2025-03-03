---
created: 2024-05-26T03:40:19
source: https://publish.obsidian.md/
author: 
banner: 
feature: "![[../03 - MEDIA & FILES/6425e223361da79872f7eebf9d52b406_MD5.png]]"
---
## Overview

Image grids are a simple way to arrange [images](https://minimal.guide/images) in columns. This feature is compatible with [Block width](https://minimal.guide/features/block-width) options for image widths.

![minimal-img-grid.png](../03%20-%20MEDIA%20&%20FILES/6425e223361da79872f7eebf9d52b406_MD5.png)

## Demo

Image grids are easy to use, and don't rely on any special syntax. All you do is add an extra line break between images to create a row, and columns take care of themselves

![minimal-img-grid-demo.gif](../03%20-%20MEDIA%20&%20FILES/15a14f0169f745a2958d8811fe6505d9_MD5.gif)

## Known limitations

### Reading mode only

Image grids are only available in reading view. Image grids are not available in Live Preview or PDF exports. For the best user experience, it is recommended to edit image grids via source mode, rather than Live Preview.

### Publish support

Image grids are compatible with [Minimal for Obsidian Publish](https://minimal.guide/publish/download), however they use a newer feature of CSS `:has()` which is not available on older browsers.

## Hotkeys

-   Toggle image grids globally
-   Cycle through image block width options

## Helper classes

| Class | Description |
| --- | --- |
| `img-grid` | Sets image layout to grid mode |
| `img-100` | Image blocks fill 100% of the pane width |
| `img-max` | Image blocks fill the max line width |
| `img-wide` | Image blocks fill the wide line width |

## Settings

Additional options can be accessed via [Style Settings](https://minimal.guide/plugins/style-settings) plugin, under **Images**:

**Image grid crop** either *Crop to fit* which fills the dimensions of each grid cell, or *Show full image* which turns off cropping and scales down the image to fit fully inside the grid cell.

**Image grid background** can be set to a color, which is useful if you want to retain the masonry look when cropping is turned off.
> 