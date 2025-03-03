---
feature: "![[imagefile.jpg]]"
---

https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839

# Things I Have Tried

I’ve tried using `img:first-of-type` to select the first image of a note, but it still selects every image on the page.

# What I’m Trying to Do

I’m trying to make a css snippet that will make the first image in a note a sort of “banner image” that floats to the top of the page and spans the whole width of the note. Preferably with the first header spanning over it. Essentially, I’m trying to copy this:

# Solved by

> i made few tweaks from your previous example. i must say, make it work in Live Preview is a bit tricky because using position: absolute will throw off editing experience of your note. Luckily I remember a trick I used with display: contents. Anyway, here’s what I managed… use image alt “banner” i.e. ![[imagefile.jpg|banner]] as a way to target a specific image for banner. can use first image by targeting the first one after yaml, but i feel this image alt gives better flexibility make the imag…

## [**Olondre**](https://forum.obsidian.md/u/Olondre)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/2)

I would guess that what you see in that screenshot was done with the `Banners` Plugin by Danny Hernandez.

### [**GitHub - noatpad/obsidian-banners: An Obsidian plugin that adds banners to...**91](https://github.com/noatpad/obsidian-banners)

An Obsidian plugin that adds banners to your notes - GitHub - noatpad/obsidian-banners: An Obsidian plugin that adds banners to your notes

## [**Bluemoondragon07**](https://forum.obsidian.md/u/Bluemoondragon07)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/3)

The person in [this thread111](https://forum.obsidian.md/t/banner-image-like-in-notion/13902/9) claimed they achieved it with CSS. It does look a lot like the plug-in, though.

I’ve used the banner plug-in before, but I wanted to see if there was a solution that would automatically make the first image in the note a banner.

## [**Olondre**](https://forum.obsidian.md/u/Olondre)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/4)

Ah ok, too bad he didn’t post the css back then. You could also try the Obsidian Discord Channel, I think there is a lobby named #csssnippets or something. Lots of CSS gurus there ![[chrome-untrusted://read-anything-side-panel.top-chrome/|:wink:]]

## [**Bluemoondragon07**](https://forum.obsidian.md/u/Bluemoondragon07)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/5)

Okay, I’ll check it out. Thanks for the help!

## [**Olondre**](https://forum.obsidian.md/u/Olondre)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/6)

If someone happens to have the answer, it would be great if you could post the solution here.

## [**gapmiss**](https://forum.obsidian.md/u/gapmiss)INSIDER

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/7)

You could add a class to your note or template’s front-matter:

e.g.

Then add a custom CSS snippet with that class defined. The CSS styles needed could be extracted from the Banner Plugin’s style sheet located here:

### [**obsidian-banners/src/styles at master · noatpad/obsidian-banners**83](https://github.com/noatpad/obsidian-banners/tree/master/src/styles)

[master/src/styles](https://github.com/noatpad/obsidian-banners/tree/master/src/styles)

An Obsidian plugin that adds banners to your notes

## [**lab**](https://forum.obsidian.md/u/lab)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/8)

> I’ve tried using `img:first-of-type` to select the first image of a note, but it still selects every image on the page.

`img:first-of-type` alone will not work, since the images are not direct siblings but each in their own tree of nested divs. Actually, this is good news, since this makes it possible to have a banner for _**multiple**_ open tabs.

Since just one level higher up the parent divs of imgs _**are**_ siblings, I thought that something like `.cm-content div:has(img):first-of-type img` should do the trick. Unfortunately, it does not. I still post it, so maybe somebody can take it up and make it work…

## [**Bluemoondragon07**](https://forum.obsidian.md/u/Bluemoondragon07)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/9)

So far I’ve managed to create a banner image that adapts to the note width using [@gapmiss](https://forum.obsidian.md/u/gapmiss)’ advice. To use it, you type `obsidian-banner` in the frontmatter. This is the code:

```
img {
  : 0;
  : 0;
  right: 0;
  height: 300px;
  width: 100%;
  margin-right: auto;
  : auto;
  : cover;
  object-position: center;
  overflow: hidden;
  user-select: none;
 }
 .obsidian-banner.inline-title {
  margin-top: 300px;
 }

 .obsidian-banner.is-readable-line-widthimg {
  width: var
```

This is what it looks like:

However, with this code the banner uses the last image in the note, not the first one. I still can’t get it to select the first image.

## [**efemkay**](https://forum.obsidian.md/u/efemkay)INSIDER

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/11)

i made few tweaks from your previous example. i must say, make it work in Live Preview is a bit tricky because using `position: absolute` will throw off editing experience of your note. Luckily I remember a trick I used with `display: contents`. Anyway, here’s what I managed…

#### [[https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/1#the-full-css-snippet-with-a-number-of-tweaks-1]]**the Full Css Snippet with a Number of tweaks**

```
/* banner using css only -- https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/ */

    /* make the div (in LP) containing the image doesn't control the css box-sizing */
    .internal-embed.image-embed"banner"] { display/* original forum post snippet with minor tweak */.obsidian-banner[alt*="banner"] {
        ;
        ;
        height: 200px;
        width: ;
        object-position: 50%50%;
        overflow: hidden;
        user-select: none;
     }
     /* add option to adjust vertical position by adding the alt metadata "higher" or "lower" */
     .obsidian-banner[alt*="banner"][alt*="lower"] { [alt*="banner"][alt*="higher"] { /* original forum post with minor tweak to make it overlap */
     .inline-title {
         : 150px: ;
     }

     /* minor tweak for me, since i have snippet to make image has rounded corner */
     .obsidian-banner/* minor tweak for me, to hide snw block reference counter for the banner */
    
```

#### [[https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/1#screenshot-on-editing-view-and-reading-view-2]]**screenshot On Editing view and Reading view**

## [**Bluemoondragon07**](https://forum.obsidian.md/u/Bluemoondragon07)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/12)

Wow! I would have never figured out how to do this on my own. Thanks for sharing. I also found a way to create a gradient that fades into the note.

```
[alt*="banner"] {
-webkit-mask-image: -webkit-gradientrgba: linear-gradientrgba
```

I think you guys have a much better idea with choosing the banner image using the alt. This actually solves my problem. Thanks for your help!

I’m still curious about selecting that first image, though.

## [**efemkay**](https://forum.obsidian.md/u/efemkay)INSIDER

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/13)

> `"banner"]mask-image:`

superb! this will go into my boilerplate/reference notes. my knowledge on gradient so far has been limited to background-color. this definitely will come handy in the future.

anyway, i tried with targeting the first image. but i couldn’t make it work for editing view/live preview. it works just fine for reading view. either there’s another hidden first image or codemirror just behave differently (coz when i choose the last image, it selected the second last in my note).

so the best bet right now is using the image alt there. with that u can place the image practically anywhere in the note and it won’t disrupt any flow i can think of right now. plus u might want the custom control to adjust the position (my example using `[[.md|higher]]` to make a notch higher.

## [**gapmiss**](https://forum.obsidian.md/u/gapmiss)INSIDER

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/14)

Perhaps the CSS `has()` pseudo-class could be used to target the `img` without using the `alt` tag. With Obsidian’s recent upgrade to Electron v21, `has()` is now available. I may experiment with it but am curious if someone else(more adept) might take a crack at it.

[[|[)6](.md|Sibling Scopes in CSS, thanks to has(|[)6]]6]]6)

[[|[) as a CSS Parent Selector and much more6](.md|Using has(|[) as a CSS Parent Selector and much more6]] as a CSS Parent Selector and much more6]]%20as%20a%20CSS%20Parent%20Selector%20and%20much%20more6)

## [**holroy**](https://forum.obsidian.md/u/holroy)

[Jan 2023](https://forum.obsidian.md/t/css-how-to-style-the-first-image-in-a-note/52839/15)

> anyway, i tried with targeting the first image. but i couldn’t make it work for editing view/live preview. it works just fine for reading view. either there’s another hidden first image or codemirror just behave differently (coz when i choose the last image, it selected the second last in my note).

There is some trickery to be done, which could potentially target the first image (without doing the alternate text trick, which is a far better solution). For the reading view it looks something like this:

```
: yellow;
} 

```

Now the first image will have a background-color of yellow, whilst the other have a blue background. In other words, if you want to set something for the first image, you need to revert that setting for all other images.

Of course, in the live preview, the CSS is different, and a lot more messy, so it’s not as easy to find selectors which can be considered siblings which make that trick useful in the reading view. You could target all images using something like `.cm-contentContainer :has(div.cm-line > dv.image-embed, div.image-embed) div.image-embed`, but this selector doesn’t co-operate with the sibling selector, `~`, since the selector targets elements on different levels.

Another option, _**could be**_ to use the `:nth-child(n of <selector>)` selector, but this is not supported in chromium until version 111, and we’re currently at ver 106 for Obsidian.

Closed on Jan 30, 2023

This topic was automatically closed 7 days after the last reply. New replies are no longer allowed.

### **Hello! Looks like you’re Enjoying the Discussion, but You haven’t Signed up for an account yet.**

Tired of scrolling through the same posts? When you create an account you’ll always come back to where you left off. With an account you can also be notified of new replies, save bookmarks, and use likes to thank others. We can all work together to make this community great. ![[chrome-untrusted://read-anything-side-panel.top-chrome/|heart]]
