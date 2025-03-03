---
created: 2024-07-01
source: https://superuser.com/questions/709702/how-to-crawl-using-wget-to-download-only-html-files-ignore-images-css-js
category:
  - "[[../00 - CATEGORIES/Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster](../03%20-%20MEDIA%20&%20FILES/83f74fd863ff5c7e05952cb1c74e996a_MD5.png)"
feature: "![[../03 - MEDIA & FILES/83f74fd863ff5c7e05952cb1c74e996a_MD5.png]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/83f74fd863ff5c7e05952cb1c74e996a_MD5.png)

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

***

```cardlink
url: https://superuser.com/questions/709702/how-to-crawl-using-wget-to-download-only-html-files-ignore-images-css-js
title: "web crawler - How to crawl using wget to download ONLY HTML files (ignore images, css, js) - Super User"
description:
host: superuser.com
image: https://cdn.sstatic.net/Sites/superuser/Img/apple-touch-icon@2.png?v=e869e4459439
```
# [[ignore images, css, js|[ignore images, css, js)](ignore images, css, js|How to crawl using wget to download ONLY HTML files (ignore images, css, js|[ignore images, css, js)]]]])

## Question
Essentially, I want to crawl an entire site with Wget, but I need it to NEVER download other assets (e.g. imagery, CSS, JS, etc.). I only want the HTML files.

[Google searches](https://www.google.com/search?q=wget%20crawl%20no%20assets&oq=wget%20crawl%20no%20images) are completely useless.

Here's a command I've tried:

```
wget --limit-rate=200k --no-clobber --convert-links --random-wait -r -E -e robots=off -U "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/32.0.1700.102 Safari/537.36" -A html --domain=www.example.com http://www.example.com
```

Our site is hybrid flat-PHP and CMS. So, HTML "files" could be `/path/to/page`, `/path/to/page/`, `/path/to/page.php`, or `/path/to/page.html`.

I've even included `-R js,css` but it still downloads the files, THEN rejects them (pointless waste of bandwidth, CPU, and server load!).

***

    
    what's the command you've tried so far? If the naming of files is consistent, you should be able to use the -R flag. Alternatively, you could use the --ignore-tags flag and ignore script and img tags.

***

-   I've tried using --accept=html, but it downloads CSS files THEN deletes them. I want to prevent them from ever downloading. A headers request is fine, though -- E.g. I notice `Length: 558 [text/css]` on the files I don't want. If I could stop the request if the header doesn't return `text/html`, I'd be elated.


## Answers

@ernie's comment about `--ignore-tags` lead me down the right path! When I looked up `--ignore-tags` in `man`, I noticed `--follow-tags`.

Setting `--follow-tags=a` allowed me to skip `img`, `link`, `script`, etc.

It's probably too limited for some people looking for the same answer, but it actually works well in my case (it's okay if I miss a couple pages).

If anyone finds a way to allow for scanning ALL tags, but prevents `wget` from rejecting files only after they're downloaded (they should reject based on filename or header Content-type before downloading), I will very happily accept their answer!

***
    
    `--follow-tags=a` might not be strict enough because it will still permit downloading other file types (e.g., images) if they are linked in `<a>` tags.
    

***

what about adding the options:

```
--reject '*.js,*.css,*.ico,*.txt,*.gif,*.jpg,*.jpeg,*.png,*.mp3,*.pdf,*.tgz,*.flv,*.avi,*.mpeg,*.iso'
--ignore-tags=img,link,script 
--header="Accept: text/html"
```

***
    
    I like to use both `--follow-tags=a` with `--reject`.