---
banner: 03 - MEDIA & FILES/BANNERS/pixel-banner-image-2.png
created: 2024-12-01
source: https://forum.obsidian.md/t/a-frontmatter-that-finally-supports-links-lilas-frontmatter/53087/31
category:
  - "[[Clippings]]"
tags:
  - clippings
feature: "![[../03 - MEDIA & FILES/ba52c9b804f7b22ef486719b4e1e5686_MD5.png]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/ba52c9b804f7b22ef486719b4e1e5686_MD5.png)

***

```embed
url: "https://forum.obsidian.md/t/a-frontmatter-that-finally-supports-links-lilas-frontmatter/53087/31"
title: "A frontmatter that finally supports links ! (Lila's frontmatter 🌸) - Share & showcase - Obsidian Forum"
description: "Your > characters have been stripped, isn’t it ?  I definitely prefer using a list, it appears clearer to me.  After some tests I’ve managed to get a lighter syntax using a callout :  > [!meta]-   >- creation:: 2023-01-21T18:55:12   >- author:: [[John Doe]]   >- parents:: [[Note]], [[Another note]]   >- status:: #MayBePartial   (the callout title will automatically became “Meta” if not given)      Glad to hear that ! Since it seems that we can select the metadata callout from CSS using div[data..."
image: "https://forum.obsidian.md/uploads/default/original/3X/b/a/ba1a1301f580d34a881803aa5ed8cf7ff3cdf0ef.png"
```

***
Is it possible to have the `class:meta` to be default to all files? I’m wondering if I can configure it so I don’t need to add anything to the actual markdown-files to get the effects?

You could achieve this by using templates ?

I agree that using callout is by far the most future-proof solution due to their nativeness and by the way, I plan to release a version of this frontmatter based solely on callouts.

However, using callouts also implies a bit heavier syntax in Edit mode, which is why at the moment I do prefer using the custom class trick :

- Using callouts-only :

```plaintext
> [!meta] Metadata > - creation:: 2023-01-21T18:55:12 > - author:: [[John Doe]] > - parents:: [[Note]], [[Another note]] > - status:: #MayBePartial
```

- Using _Custom Classes_ plugin :

```plaintext
`.meta` - creation:: 2023-01-21T18:55:12 - author:: [[John Doe]] - parents:: [[Note]], [[Another note]] - status:: #MayBePartial
```

I’m using it in this way:

> \[!meta\] Metadata  
> creation:: 2023-01-21T18:55:12  
> author:: \[\[John Doe\]\]  
> parents:: \[\[Note\]\], \[\[Another note\]\]  
> status:: #MayBePartial

But I’m looking forward to see your new solution!

Your `>` characters have been stripped, isn’t it ?  
I definitely prefer using a list, it appears clearer to me.

After some tests I’ve managed to get a lighter syntax using a callout :

```markdown
> [!meta]- >- creation:: 2023-01-21T18:55:12 >- author:: [[John Doe]] >- parents:: [[Note]], [[Another note]] >- status:: #MayBePartial
```

(the callout title will automatically became “Meta” if not given)

Glad to hear that ! Since it seems that we can select the metadata callout from CSS using `div[data-callout="meta"]`, I’ll simply try to make it look like the metadata blocks in my original post.

Is there any need for the list anymore? Can’t you just do:

```lua
> [!meta]- > creation:: 2023-01-21T18:55:12 > author:: [[John Doe]] > parents:: [[Note]], [[Another note]] > status:: #MayBePartial
```

Or is there some other bits and pieces which then would not work? Would there be a need to query for any particular line in this metadata block (thusly requiring a list scope), or would it be OK that they all reside within the page scope?

No it’s just a matter of preference. By the way, I’ve myself removed those list dots ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:") 
I’ll publish soon, a new CSS file for this front matter based on native callouts.

Oh wow this is great, thanks!

I just decided to move some of my personal notes to Obsidian, and the first thing I got stuck with were the frontmatters. I’ve tried to use some editors with YAML frontmatters before, but I just could not get over the fact that you could not click the stuff in the metadata ![:sweat_smile:](../03%20-%20MEDIA%20&%20FILES/462d94edf47cb225f0e4c08ce52c5efc_MD5.png ":sweat_smile:")

Welcome! Glad it helps! ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:") 
I understand, I’ve been through the same process and that’s why after few years of using ugly frontmatters I took time to find a solution ^^

Note that I do not recommend anymore using the Custom Classes plugin but instead to use native callouts as mentioned above.

Here is the current snippet I use to style callout as frontmatter revealed on hover:

```css
[data-callout="meta"] { width: fit-content; margin: 0; padding: 0; background-color: transparent; border: 2px solid var(--background-secondary); border-radius: 15px; } [data-callout="meta"]::before { content: "Metadata"; display: block; padding: 15px 19px 15px 19px; background-color: var(--background-secondary); opacity: 0.5; font-size: 17px; font-family: monospace; font-weight: 900; letter-spacing: 0.05em; max-height: 100vh; max-width: 100vw; transition: max-height 100ms ease-out, max-width 400ms ease-out, padding 300ms ease-out, opacity 400ms ease-out; overflow: hidden; width: fit-content; border-bottom-right-radius: 15px; white-space: nowrap; } [data-callout="meta"]:hover::before { max-height: 0px; max-width: 0px; padding: 0; opacity: 0; } [data-callout="meta"] .callout-title { display: none; } [data-callout="meta"] .callout-content > p { margin: 0; } [data-callout="meta"] .callout-content { display: block !important; max-width: 0; max-height: 0; white-space: nowrap; overflow: hidden; line-height: 1.8em; opacity: 0; transition: max-height 200ms ease-out, max-width 400ms ease-out, padding 200ms ease-out, opacity 400ms ease-out; } [data-callout="meta"]:hover .callout-content { padding: 21px 25px 23px 25px; max-width: 100vw; max-height: 100vh; opacity: 1; }
```

Note that it may be specific to the theme I use (Minimal) and may need few adjustment to work properly with other themes.

This CSS file will style every callouts called `meta`, e.g.,

```plaintext
> [!meta]- > creation:: 2023-01-21T18:55:12 > author:: [[John Doe]] > parents:: [[Note]], [[Another note]] > status:: #MayBePartial
```

Thanks a lot! These look great out-of-the-box, I just have tweak my theme’s contrast and paddings a bit.

I am still trying to wrap my head around how Obsidian handles the actual metadata currently. Interestingly, when I just paste the callout block before the H1 title, Obsidian seems to accept the properties as the “real YAML”: even the tags. At least the behave like it.

I can for example add the current date in the callout with [Natural language dates -plugin 3](https://github.com/argenos/nldates-obsidian), type @today, and the link to the today’s daily note pops up in the YAML properties.

So far I only spotted that I’ve not been able to update the Boolean parameters in the frontmatter via the callout, but that’s not a problem. I just wanted to have the clickable links in the frontmatter ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:") 

Great!

This frontmatter uses Dataview [inline fields 6](https://blacksmithgu.github.io/obsidian-dataview/annotation/add-metadata/#inline-fields) (the `::` syntax). So yeah, if you have Dataview plugin installed it is very likely that most fields in this frontmatter will behave like the native ones ![:upside_down_face:](../03%20-%20MEDIA%20&%20FILES/60ab385a23d77cce196103b1fa8c15a9_MD5.png ":upside_down_face:")

Great! Yes, I’m using Dataview ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")

So, now I have a neat frontmatter-plate which expands by hovering the title to a block with the clickable internal links and tags, which work also as Dataview properties. ![:+1:](../03%20-%20MEDIA%20&%20FILES/cf5917e73af35358fa7a929d1ab82832_MD5.png ":+1:")And which I can edit with Markdown.

Thanks a lot for these [@LilaRest](https://forum.obsidian.md/u/lilarest)!

So here’s my current set-up: I have a few internal-link-properties I want to have in all my the notes. I have a template which pushes this block in each new note before the first H1-heading. Then I can manually enter the internal links in the callout.

Some other stuff pops up in the new note metadata via dynamic front-matter of the template.

I have admit had to reduce your cool-looking CSS snippet to a more simple one, since I did not manage to make the transitions to work in some of my views. I don’t know anything about CSS best-practises, but I share it anyway, since at least for me this has been working so far ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")Please welcome, the first CSS-snippet by me:

> Blockquote  
> .callout\[data-callout=“meta”\] {  
> –callout-color: #fcf8f2;  
> –callout-icon: lucide-folder-heart;  
> }
> 
> \[data-callout=“meta”\]:hover::before.callout-title {  
> display: none;  
> callout-icon: lucide-folder-heart;  
> margin-top: -5px;  
> }
> 
> \[data-callout=“meta”\] {  
> display: block;  
> padding: 20px 20px 20px 20px;  
> background-color: var(–background-secondary);  
> box-shadow: -2px -2px 8px var(–color-base-30);  
> border-radius: 10px;  
> opacity: 0.85;  
> callout-color: #fcf8f2;  
> font-size: 16px;  
> font-family: system-ui;  
> font-weight: 50;  
> letter-spacing: 0.01em;  
> max-height: 100vh;  
> max-width: 100vw;  
> }
> 
> \[data-callout=“meta”\]:hover .callout-content {  
> max-width: 100vw;  
> max-height: 100vh;  
> opacity: 1;  
> }
> 
> \[data-callout=“meta”\] .callout-content {  
> display: block !important;  
> max-width: 0;  
> max-height: 0;  
> font-family: monospace;  
> font-size: 13px;  
> font-weight: 100;  
> white-space: nowrap;  
> overflow: hidden;  
> line-height: 1.5em;  
> opacity: 50;  
> transition: max-height 200ms ease-out,  
> max-width 400ms ease-out,  
> padding 200ms ease-out,  
> opacity 400ms ease-out;  
> }

Do you mind checking the code again. It’s not working for me. Thanks!

Is it accurate to say that the original post is outdated and this is your most current setup which just includes the CSS code and using `[!meta]` in the callout syntax?  
Sorry I’m still new to this metadata thing and everything is just very confusing.

Sorry, I was using not-valid method for posting code-snippets to this forum, and apparently I am not allowed to edit my previous reply!

I am also new here, just decided 10 days ago to migrate to Obsidian from Notion… So I hope you bear with me ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")

But, anyways, I am using Minimal theme (solarized), and for me the following CSS snippet is working.

I guess there is no need to have these fancy-pancy clickable links in the metadata anyway if there is no need to use the Dataview-plugin. And per my understanding, the Dataview is up to some major changes any day soon. So, maybe it’s better to just wait and see ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")

But it was a nice exercise anywaay, and the click-box does look cool ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")

```css
.callout[data-callout="meta"] { --callout-color: #fcf8f2; --callout-icon: lucide-folder-heart; } [data-callout="meta"]:hover::before.callout-title { display: none; callout-icon: lucide-folder-heart; margin-top: -5px; } [data-callout="meta"] { display: block; padding: 20px 20px 20px 20px; background-color: var(--background-secondary); box-shadow: -2px -2px 8px var(--color-base-30); border-radius: 10px; opacity: 0.85; callout-color: #fcf8f2; font-size: 16px; font-family: system-ui; font-weight: 50; letter-spacing: 0.01em; max-height: 100vh; max-width: 100vw; } [data-callout="meta"]:hover .callout-content { max-width: 100vw; max-height: 100vh; opacity: 1; } [data-callout="meta"] .callout-content { display: block !important; max-width: 0; max-height: 0; font-family: monospace; font-size: 13px; font-weight: 100; white-space: nowrap; overflow: hidden; line-height: 1.5em; opacity: 50; transition: max-height 200ms ease-out, max-width 400ms ease-out, padding 200ms ease-out, opacity 400ms ease-out; }
```

I am also pretty perplexed by how Obsidian and Dataview currently handle the metadata. I would really want to love this tool and give credits and stars for all the people who volunteer in the developing the ecosystem, and even pay for working solutions.

I guess I’ll check this tool and forum again after some months, to see if I can figure this stuff out ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/5017c4e4f966427a34c41a67ee968a2a_MD5.png ":slight_smile:")

Thanks for bringing this topic up and the work you put into it. Frontmatter done this way is so much better.

Yeah indeed, the original post can be considered as outdated as it relies on the “Custom Classes” plugin which I don’t maintain anymore.

The callout solution (using `[!meta]`) only relies on native features of the Obsidian editor, which makes it much more sustainable and easier to integrate.

Glad it helped you! ![:upside_down_face:](../03%20-%20MEDIA%20&%20FILES/60ab385a23d77cce196103b1fa8c15a9_MD5.png ":upside_down_face:")
