---
created: 2024-05-26T09:59:34
source: https://publish.obsidian.md/
author: 
cssclasses:
  - banner-image
  - obsidian-banner
category:
  - "[[../00 - CATEGORIES/Clippings]]"
---

# This Solution Allows You to Create Banner Images across the top of a Page without the Need for a Plugin.

## More Information

### CSS Snippet for This Solution

```css
/* Author: TfTHacker - more info https://tfthacker.com/banner-image Date: 2023-08-08 LICENSE: Copyright © 2023 TfThacker. Permission is granted to modify and distribute copies of this CSS file, that credit is given to TfThacker (https://tfthacker.com/) and the banner image source (https://tfthacker.com/banner-image) remains linked and credited. */ :root { --banner-image-height: 150px; } .banner-image > .markdown-preview-section { margin-top: var(--banner-image-height) !important; } .show-view-header div:not(.markdown-embed-content) > .markdown-preview-view:is(.banner-imageright):has([data-callout="banner-image"]) { padding-top: 0px; } .banner-image.markdown-preview-view [data-callout="banner-image"] { position: absolute; top: 0; left: 0; right: 0; height: var(--banner-image-height) !important; margin: 0px !important; padding: 0px; background-color: transparent; border: 0px !important; border-radius: unset !important; .callout-icon { display: none; } .callout-title { padding: 0px !important; border: 0px !important; } .callout-title-inner { padding: 0px !important; margin: 0px !important; } } .banner-image.markdown-preview-view [data-callout="banner-image"] img { position: absolute; min-height: var(--banner-image-height) !important; width: 100%; object-fit: cover; margin: 0px !important; padding: 0px !important; } .banner-image [data-callout="banner-image"] { .callout-icon { display: none; } } @media print { [data-callout="banner-image"] { position: unset !important; top: unset !important } .banner-no-print [data-callout="banner-image"] { display: none; } } /* @settings name: Banner Image id: tft-banner-image settings: - id: banner-image-height title: Height in pixels description: Sets the height of the image and top margin area type: variable-number default: 150 format: px */
```

#### Sample Document for This Solution

```
---
cssclass: banner-image  
---
&gt;[[vacation.jpg|!banner-image]]  
  
# My Header  
My document text here ...  
...  
...
```

#### Exporting to PDF

The banner will export to PDF, however, it is not aligned in the same way. PDF is a print medium and needs to be formatted differently.

If you don't want the banner to show when printing, add `banner-no-print` to the cssclass in the frontmatter. It would like:

```
---
cssclass: banner-image, banner-no-print
---
&gt;[[vacation.jpg|!banner-image]]  
```

When the frontmatter is configured this way, the banner will display in Preview mode in Obsidian, but will not display when using the Export to PDF option.
