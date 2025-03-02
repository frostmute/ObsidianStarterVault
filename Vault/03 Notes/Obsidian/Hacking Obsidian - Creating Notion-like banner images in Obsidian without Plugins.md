---
cssclasses:
  - bannerimage
created: 2024-12-22
source: https://medium.com/obsidian-observer/hacking-obsidian-creating-notion-like-banner-images-in-obsidian-without-plugins-7ad3e0bddc30
tags:
  - clippings
---

![##bannerimg](https://miro.medium.com/v2/resize:fit:1200/1*TP-xSbNriqipj9m83IQI0g.png)

A markdown-friendly and portable solution for banner images

Banner in an Obsidian document, without using any plugins

Welcome to another article in my [Hacking Obsidian series](https://tfthacker.com/HackingObsidian). Today we talk about banner images.

As depicted in this article’s cover image, I have a preference for incorporating banners at the top of my documents.

I can’t pinpoint the exact reason, but incorporating an image with its vibrant colors and shapes undoubtedly adds another layer of visual depth to my notes.

These banners not only clarify the intent of the content but also make it more memorable. When I open a document with a banner, it instantly transports me to a certain mindset. If it’s a technical topic, an image featuring computers or robots sets the mood. If it’s health-related, a serene image ushers in a peaceful state of mind.

In Obsidian, I often achieve this effect using the [Banners plugin](https://obsidian.md/plugins?id=obsidian-banners), which is nothing short of incredible. However, there are times when I’d rather not rely on a plugin, particularly if I want the markdown document to be portable, independent of any plugin.

With that in mind, I’ve devised a handy CSS snippet that can be added to Obsidian, allowing us to seamlessly integrate banners into documents without the need for any plugins.

## The Hard Part (but not so hard)

Perhaps the sole challenging aspect of utilizing this solution is installing the CSS snippet into your vault, that is if you have never done this before.

This approach necessitates a CSS snippet tailored to your vault. The advantages of CSS snippets include portability, easy integration with vaults, and the elimination of any need for JavaScript code or plugins.

To access the specific CSS snippet required for this solution, visit this page: [https://tfthacker.com/banner-image](https://tfthacker.com/banner-image). Once there, scroll down to the section titled “CSS Snippet for this solution” and copy the text as illustrated in the accompanying image.

![](https://miro.medium.com/v2/resize:fit:700/1*srfVLy4IKqsiQXweVy0ppg.gif)

Copy the CSS snippet for use in your vault

This CSS text will need to be added to a snippet file in your vault.

> To learn more about installing CSS snippets, check out the Obsidian Help at this link: [https://help.obsidian.md/Extending+Obsidian/CSS+snippets](https://help.obsidian.md/Extending+Obsidian/CSS+snippets).

## The Fun Part, Creating a Banner

Now comes the enjoyable and fun part — adding a banner to your document.

The subsequent animated image demonstrates the process. Take a moment to observe it, and then we’ll dissect the steps individually.

![](https://miro.medium.com/v2/resize:fit:700/1*vIKlsHlRpT1IjaKRsPu2dA.gif)

Demonstration of adding a banner to a document

First, we need to instruct Obsidian to implement the CSS snippet created in the previous step. The CSS snippet incorporates a CSS class named **banner-image**. To apply this to our document, we must include some [frontmatter](https://help.obsidian.md/Editing+and+formatting/Metadata#Metadata+format) at the very beginning of the document, which will appear as follows:

```
<span id="4117" data-selectable-paragraph=""><span>---</span><br><span>cssclass:</span> <span>banner-image</span><br><span>---</span></span>
```

Next, we can insert our banner image. For this tutorial, let’s assume you have an image in your vault titled **vacation.jpg**.

This method is remarkably simple — here’s what you need to add to your markdown for the banner image to appear on the page when in Preview mode:

```
<span id="7b6c" data-selectable-paragraph="">&gt;[!banner-image] ![[vacation.jpg]]</span>
```

With this markdown, we instruct Obsidian to utilize the vacation.jpg file as a banner. The banner will align at the very top of the pane, without any left or right margin space.

Let’s delve further into the details.

-   The initial part of this line is *\>\[!banner-image\]*. You might recognize this as an [Obsidian callout](https://help.obsidian.md/Editing+and+formatting/Callouts). We are employing a custom type identifier called **banner-image**. This customized type is defined in the CSS snippet. However, don’t worry about the nerdy details, just remember you use the \`banner-image\` type identifier in the callout.
-   Following that is the standard [embedded image](https://help.obsidian.md/Linking+notes+and+files/Embedding+files#Embed%20an%20image%20in%20a%20note) syntax for Obsidian with *!\[\[vacation.jpg\]\]*.
-   Additionally, you can specify an image size, which will affect the sizing of the displayed image in Live Preview. For instance, !\[\[vacation.jpg|200\]\] will resize the image to 200 pixels wide. However, this setting gets disregarded when the page is viewed in Preview mode.
-   *Note*: Refrain from including any other text in the callout.

In review, a document using the previously mentioned example would look like this:

```
<span id="0375" data-selectable-paragraph=""><span>---</span><br><span>cssclass:</span> <span>banner-image</span><br><span>---</span><br><span>&gt;[!banner-image]</span> <span>![[vacation.jpg]]</span><br><br><br><span>My</span> <span>document</span> <span>text</span> <span>here</span> <span>...</span><br><span>...</span><br><span>...</span></span>
```

## Bonus tip

By the way, you can also use an online image, not just one from your vault. For example:

```
<span id="99d4" data-selectable-paragraph="">&gt;[<span>!banner-image</span>] ![](<span>https://publish-01.obsidian.md/access/5482717c61d4cd4a5e39468efa73a612/media/logo.jpg</span>)<br>I also suggest selecting images that are wide and short. Banners are aligned across the top, so you want them to be wide, but not tall. If an image is not wide, it will not be stretched to fill the screen.</span>
```

## Banner Height

The banner height is 150 pixels. This can be adjusted to be less or more pixel height.

To do this, you need to modify the CSS snippet you installed for this solution. In the CSS snippet, you will see the following line:

![](https://miro.medium.com/v2/resize:fit:608/1*DnE9YLgPvn0zInylnao9XA.png)

You can change the 150px to another height. For example: 200px or 250px.

My advice: don’t make it too large. Also, the number of pixels needs to be followed by \`px\`. So you can’t type just 200, it needs to be 200px. Changing it to 200px means the CSS snippet will look like this:

![](https://miro.medium.com/v2/resize:fit:610/1*wq2l9OEVc7ltwizPG4xjVw.png)

> **Note**: The banner height also affects the margin height at the top of the document, it adds additional margin space to move your text down. I mention this because it’s possible that some themes or plugins might not be compatible with this technique. Always do some experimentation to confirm this solution works reliably in your vault.

## Summary

That is it! As a review, you need to:

-   Install the CSS Snippet for the banner-image. This is a one-time step per vault.

Then for each document you want to show a banner:

-   Add the frontmatter cssclass name: *cssclass: banner-image* to the document.
-   Add a callout using the banner-image identifier, followed by an embedded image link: *\>\[!banner-image\] !\[\[vacation.jpg\]\]*

The good news about this solution is that even without the CSS Snippet, your markdown is still valid markdown and will render nicely in vaults that don’t have the CSS snippet installed. The banner-image callouts won’t appear as banners, but they will appear as standard callouts.

Thus this solution is portable and future-proofs our markdown documents.

If you are interested in more articles from my Hacking Obsidian series, check out this [link](https://tfthacker.com/HackingObsidian).
