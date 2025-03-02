---
created: 2025-02-05
source: https://askubuntu.com/questions/1166881/convert-backup-bookmarks-html-file-to-a-folder-that-contains-url-files-for-e
banner: 
tags:
  - clippings
---

![Banner]()

***
You can have the following approach:

1.  Parse bookmarks.html to
    -   keep lines containting HREF
    -   keep in these lines only what is in HREF="..."
2.  With these strings
    -   remove protocol and slash (`/`)
    -   fill a template file with the good name

***

-   Enter the following code in your favorite editor:

  

```
#! /bin/bash

sites=$(sed '/HREF/!d' &lt; $1 | sed 's/.*HREF="\([^ "]*\).*/\1/')

for site in $sites
do
    file=$(echo $site | sed 's/https*:\/\///' | sed 's/\/.*//')

    cat &lt;&lt; EOF &gt; $file
    &lt;html&gt;
    &lt;head&gt;
    &lt;meta http-equiv="refresh" content="0; url=$site" /&gt;
    &lt;/head&gt;
    &lt;/html&gt;
    EOF

done
```

-   Save it as `extract.sh`
-   In a terminal, make it executable `chmod +x extract.sh`
-   Use it: `./extract.sh /path/to/bookmark.html`
