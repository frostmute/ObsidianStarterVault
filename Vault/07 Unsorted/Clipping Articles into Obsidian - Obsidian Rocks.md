---
banner: https://obsidian.rocks/wp-content/uploads/2023/08/elena-mozhvilo-_oFYCifdZJo-unsplash.jpg
banner_y: 0.955
category:
  - "[[../00 - CATEGORIES/Clippings]]"
---
---
created: 2024-05-17T00:51:54 (UTC -05:00)
source: https://obsidian.rocks/clipping-articles-into-obsidian/
author: Tim Miller
banner: https://obsidian.rocks/wp-content/uploads/2023/08/elena-mozhvilo-_oFYCifdZJo-unsplash.jpg

---
Have you ever wanted to copy a whole article into your Obsidian vault? This is referred to as “clipping”, as if you cut an article out of a newspaper and pasted it into your scrapbook. If that sounds interesting to you, then keep reading. We’ll discuss the many different ways for clipping articles into Obsidian.

On This Page

-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Table_of_Contents]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Method_1_Use_a_Bookmarklet]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#How_to_use_the_Bookmarklet]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Bookmarklet_Pros]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Bookmarklet_Cons]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Method_2_MarkDownload]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#How_to_use_MarkDownload]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#MarkDownload_Pros]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#MarkDownload_Cons]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Method_3_Obsidian_Clipper]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#How_to_use_Obsidian_Clipper]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Obsidian_Clipper_Pros]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Obsidian_Clipper_Cons]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#The_Elephant_in_the_Room_Mobile]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Conclusion]]
    -   [[https://obsidian.rocks/clipping-articles-into-obsidian/#Like_this]]

## Table of Contents

-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#method1]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#method2]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#method3]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#mobile]]
-   [[https://obsidian.rocks/clipping-articles-into-obsidian/#conclusion]]

Before we get into each method, I’d like you to know that I have personally tested every one of these methods, and I don’t think there’s a single *best* or *worst* method for clipping articles into Obsidian. Each method has its own strengths and weaknesses, which we will talk about below.

## Method 1: Use a Bookmarklet

The CEO of Obsidian, Kepano, [build a bookmarklet](https://stephanango.com/obsidian-web-clipper) for clipping articles into Obsidian. This is the method I recommended in the previous article, because it was the only method I had used. And it works well, but it does have some limitations.

In my own testing, I found that this bookmarklet only works for articles that are no longer than about 4000 words. For short articles this is fine, but for longer articles it gives you an error message.

Additionally, it’s a little challenging to modify the template that this bookmarklet creates. If you like the default options then you’re good, but otherwise it might be a challenge getting it to work.

Other than that, this bookmarklet is a great solution. Unlike a plugin it doesn’t require any installation, it’s easy to use, and it works consistently for small to medium size articles. It also pulls in some additional metadata (like author and publish date) which can be quite handy.

### How to use the Bookmarklet

Go to [Kepano’s site](https://stephanango.com/obsidian-web-clipper) and follow the instructions. If you’re happy with the default options, then installation is quick and easy.

### Bookmarklet Pros

-   Good default metadata
-   Doesn’t require installing anything

### Bookmarklet Cons

-   Tricky to configure
-   Doesn’t work with long articles

## Method 2: MarkDownload

MarkDownload is a plugin for your web browser. It works on [Firefox](https://addons.mozilla.org/en-GB/firefox/addon/markdownload/), [Chrome/Brave](https://chrome.google.com/webstore/detail/markdownload-markdown-web/pcmpcfapbekmbjjkdalcgopdkipoggdi), [Edge](https://microsoftedge.microsoft.com/addons/detail/hajanaajapkhaabfcofdjgjnlgkdkknm), and [Safari](https://apple.co/3tcU0pD).

Unlike the other options in this list, MarkDownload is not built specifically for Obsidian. It does only one thing, and it does it well: it converts webpages to Markdown files and saves them to your computer.

The best thing about MarkDownload is that it *works consistently*. Once you install it, there are no surprises. It does one thing, and it does it well.

The downside is that it’s not yet integrated with Obsidian. There is no one-click “save to Obsidian”. They are working on that, but it’s a tricky problem, and there’s no telling if or when it will be released.

If you use MarkDownload, you can trust that it will almost always capture what you want. But it requires a little more leg work to get it into Obsidian.

In my own testing, I found that rather than clicking the “Download” button, I prefer to click the MarkDownload button and copy the text straight from the plugin popup itself (see below). Then I paste it into Obsidian. It’s one more step, but unlike the Obsidian integrations, it *always* works, which is nice.

![[https://i0.wp.com/obsidian.rocks/wp-content/uploads/2023/08/markdownload-popup.png?resize=517%2C681&ssl=1]]

### How to use MarkDownload

Go to the store page for your web browser ([Firefox](https://addons.mozilla.org/en-GB/firefox/addon/markdownload/), [Chrome/Brave](https://chrome.google.com/webstore/detail/markdownload-markdown-web/pcmpcfapbekmbjjkdalcgopdkipoggdi), [Edge](https://microsoftedge.microsoft.com/addons/detail/hajanaajapkhaabfcofdjgjnlgkdkknm), or [Safari](https://apple.co/3tcU0pD)) and click “install”. Then click the MarkDownload icon whenever you want to clip an article.

See the [[https://github.com/deathau/markdownload/blob/master/user-guide.md#markdownload-user-guide]] for configuration options.

> Note: Apparently there *is* an Obsidian integration for this plugin, but [it’s a pain to set up](https://forum.obsidian.md/t/help-needed-with-markdownload-web-clipper/54920/3?u=webinspect). It might still be in development. If the Obsidian integration worked better, this plugin would probably be the best option for most people.

### MarkDownload Pros

-   Works with large articles
-   Easy to install
-   Lots of configuration options

### MarkDownload Cons

-   Requires downloading a file or copy/pasting it
-   Configuration is a little harder than Clipper, but not as hard as the Bookmarklet
-   Ugly interface

## Method 3: Obsidian Clipper

Obsidian Clipper is another plugin for your web browser. Clipper is nice because you can configure it with a *visual interface*, and the interface is clean and easy to use:

![[https://i0.wp.com/obsidian.rocks/wp-content/uploads/2023/08/obsidian-clipper-config.png?resize=1024%2C975&ssl=1]]

There are three main downsides to this plugin:

-   Not as many metadata options as the Bookmarklet
-   Doesn’t work with long articles

It you clip mostly short or medium length articles, this might be a great option for you!

### How to use Obsidian Clipper

Go to the [Obsidian Clipper Github repo](https://github.com/jplattel/obsidian-clipper) and follow the instructions.

The first time you run Clipper, it will ask you to configure it. The default options are good as-is, so you might not even need to configure anything, but it’s an option.

### Obsidian Clipper Pros

-   Easy to configure
-   Pretty interface
-   One click copy-to-Obsidian

### Obsidian Clipper Cons

-   Not as much configuration available
-   Doesn’t work with long articles

## The Elephant in the Room: Mobile

Unfortunately, at the moment, none of the above options work for clipping articles into Obsidian.

Web browsers don’t support plugins on mobile, so method 2&3 are eliminated.

In writing this article I tested method 1, because I thought that it might work on mobile, but I was unable to make it work. Perhaps with some tweaks it could work there, but I’m not sure.

For now, if you want to clip content on mobile, you’ll have to use [one of the other options for saving articles to Obsidian](https://obsidian.rocks/save-articles-to-obsidian-five-different-methods/).

## Conclusion

As you can see, these three methods each offer something valuable. My thought process goes something like this:

-   If you want the most customizability or to avoid installing a plugin, go with the Bookmarklet (Method 1)
-   If you want to clip long articles, use MarkDownload (Method 2)
-   If you want the easiest to install and use, go with Obsidian Clipper (Method 3)

There are other reasons to use each one, but the above is a good rule of thumb.

We won't send you spam. Unsubscribe at any time.
> 