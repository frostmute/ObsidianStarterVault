---
banner: https://miro.medium.com/v2/resize:fit:1155/0*MZt2PQ_KewmQ-vON.jpeg
category:
  - "[[../00 - CATEGORIES/Clippings]]"
feature: "![[../03 - MEDIA & FILES/0!VoWjh_23ZAS1Bio3.jpeg.jpg]]"
---

![[../03 - MEDIA & FILES/0!VoWjh_23ZAS1Bio3.jpeg.jpg]]

Dashboard ++ on tablet and mobile phone

I have been experimenting with a simple method to organize better and navigate my ever-growing vault of notes.

I call my method Dashboard++ (yes plus, plus). It is a dashboard designed to be an easy-to-maintain index into the notes of my vault. I had some goals when starting this experiment:

- Make my notes more discoverable by grouping them into related topics.
- As with Wikipedia, promote linking between notes and topics.

My goal was not to force some top-down structure but rather acknowledge that systems form naturally as relationships between notes are made.

After using Dashboard++ for a few months, it has become a personal Wikipedia, or even better stated, a “living and expanding” table of contents into my cross-linked notes.

This article will explain how Dashboard++ works and then walk you through the steps to enable the same method in your vault.

The method is strongly opinionated to my approach to work.

While I want to teach you this method, I hope you will seriously adapt it to your own needs. Remember that _Personal_ Knowledge Management, or PKM, starts with the word _Personal._ You need to customize this method to your _personal_ needs and preferences.

By the way, make sure to check out my amazingly useful tools for bringing Obsidian to another level of productivity: [https://store.tfthacker.com/](https://store.tfthacker.com/)

# The Need for Simplicity

I can’t emphasize this enough: simplicity. I didn’t want to place any constraints on my note-making. I want ideas to flow, research to be gathered, knowledge to be synthesized, and creativity to flourish.

I also wanted to keep the setup and configuration super simple. In other words, I didn’t want to depend on complex plugins or extensive hacks. Complexity creates a mental barrier, a subconscious resistance towards use. On the other hand, simplicity encourages use and allows achieving results with the least time and emotional investment.

As you will see, Dashboard++ is made up of two simple things:

- A CSS style sheet you add to your vault that provides some missing formatting powers
- The use of markdown lists for creating structured indexes

I use some plugins to add sugar and spice to Dashboard++, but they are totally optional.

# The Dashboard++ Approach

In the opening picture of this article, you see my home page. This is the file that I see every time I open Obsidian. It is a living dashboard, organized as a simple index into my notes.

I use the term index to refer to how the Dashboard is laid out. But in fact, Dashbaord++ is made of two concepts merged into one from the world of books:

- _Table of Contents:_ the information at the beginning of the book to identify the structure of a book
- _Index:_ the topic-based reference at the end of the book for finding specific topics.

As you look at the picture from the beginning of the article, you will notice that the design is simple; the index is organized by main topics like family, personal projects, work, and a few other topics.

Under each main topic are subtopics. These subtopics might lead to another dashboard page that focuses on that subtopic, which contains another index to notes in my vault on that subtopic.

The following picture demonstrates the flow between the home page, a subtopic, and, finally, an actual note. If you click on the image, it will expand to fill the screen. Study it for a moment.

![[03 MEDIA & FILES/0!MZt2PQ_KewmQ-vON.jpeg.jpg)

A typical Dashboard++ workflow

It all starts with the home page. The home page has a delightful banner running across the top. The banner is an image of a pile of books and notes. This banner inspires me to enter a mental note-making mode subconsciously.

All my Dashboard++ pages have a banner, and in fact, many of my notes have a banner. They add character to each page.

Under the main topic of Family, there is a subtopic of Objectives. One objective is Family Recipes. This is where I keep a list of exciting recipes to prepare for my family.

The Family Recipes dashboard is organized like the home page, with main topics and subtopics. Finally, when I click on Spicy-Sweet Buffalo Popcorn, it opens a note, which is a recipe.

Of course, this is a simple example, but it shows how I create a simple top-level dashboard that can link into many other subtopic dashboards that link into pages.

By the way, make sure to check out my amazingly useful tools for bringing Obsidian to another level of productivity: [https://store.tfthacker.com/](https://store.tfthacker.com/)

# Structure without Structure

I don’t force any structure, but I add new topics and subtopics as I add new notes to my vault. In fact, I often create notes in the root folder of the vault and let them pile up for a few weeks. As the notes become fine-tuned, I usually start to see where those notes belong in the dashboard structure, or even better yet, new topics appear that need to be added to the Dashboard.

![[../03 - MEDIA & FILES/0!NvmtZA3XFrTwehly.png.jpg]]

Dashboard++ structure of topic dashboards to subtopic dashboards

Again, this is a living and breathing index of my notes. I constantly add, modify and delete topics from these dashboards in the pursuit of fine-tuning the index to be valuable and relevant.

As I do this “maintenance” work on the indexes, I see that my retention of information from the notes I have made improves. I better remember what notes I have added into Dashboard++ and how they connect them into multiple places.

> ==_With time, structure forms from non-structure._==

It is so simple that even if it doesn’t solve all the world’s problems, I find it a joy to use, and my vault steadily becomes more valuable.

It is truly a personal Wikipedia.

# Preparing Your Vault for Dashboard++

The Dashboard++ method is straightforward to implement in your vault. I am going to show you step-by-step how to do it. I will focus on the requirements for this method and then provide optional “bonus” suggestions on improving Dashboard++.

Additionally, I have created a sample vault that you can download from GitHub: [https://github.com/TfTHacker/DashboardPlusPlus](https://github.com/TfTHacker/DashboardPlusPlus). This sample vault is already configured with Dashboard++ so you can play with it in Obsidian. You can download this simple vault by clicking on the Code button, then Download it as a zip file:

![[../03 - MEDIA & FILES/0!ZtECg0u5tgglbrmi.png.jpg]]

Download the vault as a zip file

Now let us get into the step-by-step process of adding Dashboard++ to your vault.

## Step 1: Install the Dashboard++ CSS Snippet

As I mentioned earlier, one of my main goals was to keep Dashboard++ super simple. With this in mind, you only have to install one thing: the CSS snippet for Dashboard++.

> _NOTE: If you have never installed a CSS snippet into Obsidian, you can find instructions on how to this at this link:_ [_Add custom styles to Obsidian_](https://help.obsidian.md/How+to/Add+custom+styles)_._

1. Create a dashboard.css file in your Obsidian snippets folder.
2. Paste into the dashboard.css file the CSS code from this link: [Dashboard CSS Snippet](https://github.com/TfTHacker/DashboardPlusPlus/blob/master/.obsidian/snippets/dashboard.css).
3. In Obsidian settings, refresh the CSS snippets and enable the dashboard.css file under appearance.

![[../03 - MEDIA & FILES/0!--O5Azy_MWhzwyhx.png.jpg]]

Enabling dashboard.css in Obsidian

You have now successfully installed Dashboard++. It was that simple.

> _NOTE: The dashboard.css has been tested with many standard Obsidian themes on the desktop, tablet and mobile phone. However, it may not work with every theme, so some testing may be required on your part. If you are curioius, for this article I am using the Minimal theme._

## Step 2: Create Your First Dashboard

Create a new file in your Obsidian vault. This file will be the home page for your primary Dashboard. We will refer to this page as the home page for this article. You can name it whatever you like.

You see my home page in the Reading mode in the background and the same page in Editing mode in the foreground in the following picture. Notice how the Markdown in edit mode renders when in Reading mode.

![[../03 - MEDIA & FILES/0!v5cNQsdUixraZ3vR.png.jpg]]

Let us break down what we are seeing.

- The first few lines define a cssclass in the [front matter](https://help.obsidian.md/Advanced+topics/YAML+front+matter) for this page. It includes cssclass, a special parameter that tells Obsidian to use the dashboard CSS class we created in step 1 when adding dashboard.css to our vault. This front matter is needed in each dashboard page you make in your vault.

---  
cssclass: dashboard  
---

- Then there is **# Family**. This is the Markdown for a Heading at level 1. As you can see in my Dashboard, I have a few Headers: Family, Personal Projects, and Work. The Heading level 1 creates a logical grouping of topics.

# Family

- After # Family, we see a simple [Markdown list](https://help.obsidian.md/How+to/Format+your+notes) with this syntax:

- 🏈 Sunday Game   
	- [[99 DASHBOARD++/Family/Recipes/Spicy-Sweet Buffalo Popcorn]]  
	- [[99 DASHBOARD++/Family/Guests/Guest list]]   
	- [Jalapeno Popper Wantons](https://www.allrecipes.com/166991)  
- 👨‍👩‍👦 Objectives   
	- [[99 DASHBOARD++/Family/Objectives/Family Recipes]]   
	- [[99 DASHBOARD++/Family/Objectives/Family Calendar]]   
	- [[99 DASHBOARD++/Family/Objectives/Education Plan]]   
	- [[99 DASHBOARD++/Family/Objectives/Yearly Budget]]  
- 🌅 Exotic Vacations    
	- [[99 DASHBOARD++/Family/Vacations/Peru]]   
	- [[99 DASHBOARD++/Family/Vacations/Austria]]   
	- [[99 DASHBOARD++/Family/Vacations/Texas]]    
- 🎥 Movies to Watch   
	- [Sleepless in Seattle](https://www.imdb.com/title/tt0108160/)   
	- [Joe vs the Volcano](https://www.imdb.com/title/tt0099892/)

Sunday Game, a topic, is the first item in the [list](https://help.obsidian.md/How+to/Format+your+notes) and starts with a dash. The subtopics or page links are child items under the first item.

![[../03 - MEDIA & FILES/0!H448PQg3i2kDKw9s.png.jpg]]

This is it; we just create a list. The first item is the parent and serves as the topic. All child items are the subtopics and pages related to that topic. Everything else is standard Markdown, links to internal or external pages.

In Reading view, as you add new topics with their subtopics, a new column is made for each new topic. These topics will spread out across the screen in columns.

I like this approach because I am working with simple [Markdown lists](https://help.obsidian.md/How+to/Format+your+notes) and can rapidly create and edit topics with their related content.

To create additional dashboards that will serve as subtopic dashboards, you create a new file for that subtopic using the instructions for step 2. Add the front matter, a Heading, and a list. You can then link from your home page to the new page you just created as the subtopic dashboard.

# Optional Bonus Ideas

We have finished the setup and explanation of using the Dashboard++ method for organizing notes and making your vault easier to navigate.

For the remainder of the article, I will share some other ideas I have found useful but are by no means required to use the Dashboard++ method.

Also, please note that many of these suggestions are opinionated based on my preferences.

# Optimizing Obsidian

There are a few tweaks I like to make in Obsidian’s settings to make Dashboard++ more useful. They are circled here:

![[../03 - MEDIA & FILES/0!VQsmLbleWRC4bKkr.png.jpg]]

## Reading Mode

When I started working with Obsidian, I had all notes open in the Editing view. However, I have found it more beneficial to open notes in Reading view mode over time. This means that notes are not editable when opened, but I need to switch to Editing mode when I want to edit.

I do this because I view my vault as a personal Wikipedia, a personal reference database of knowledge. So I often want to reference notes in my vault. Navigating your vault in Reading mode is much faster than in Editing mode.

> _NOTE: You may not want to set reading mode to be the default view in your vault, but still want the dashboard to always be in Reading mode. This can be accomplished with the_ [_Force note view mode_](https://github.com/bwydoogh/obsidian-force-view-mode-of-note) _plugin._

## Readable line Length

This setting controls the viewable or reading area width on a page. A narrow reading width tends to make it easier to read. However, for Dashboard++, I have disabled this. I prefer that the Dashboard consume the entire width of the screen. Again, this is an opinionated recommendation, but I encourage you to experiment with this setting.

> _NOTE: If you don’t want to disable Readable line length, I have another CSS snippet you can add and enable in your vault that will force dashboards to use the full width of the page. The CSS snippet is in this_ [_dashboard-ReadLineLength.css_](https://github.com/TfTHacker/DashboardPlusPlus/blob/master/.obsidian/snippets/dashboard-ReadLineLength.css) _file._

## Fold Headings and Indents

Since we are working with headers and lists, Obsidian gives you the ability to Fold or collapse these structures when viewed. Again this is worth experimenting with.

![[../03 - MEDIA & FILES/0!SqcgVoongA-rBucG.png.jpg]]

I have my Family Recipes subtopic dashboard open, as demonstrated on this page. I have folded the **Family Favorites to**focus on **Recipes to try**.

# Plugin: Emoji Toolbar

I have installed the Emoji Toolbar plugin. I find it visually appealing to use emojis to call out various topics in my Dashboard, such as for projects:

![[../03 - MEDIA & FILES/0!CdAEMIc-aN_5WWcu.png.jpg]]

Notice how each topic has its own emoji, helping it stand out from other topics? We know that we better differentiate between things when visual elements are involved. These little emojis provide that subtle visual separation that helps the topics to stand out.

The Emoji Toolbar plugin makes it easy to find emojis that fit well into our Dashboard.

![[../03 - MEDIA & FILES/0!8D4Q24Vl3oOKf1DE.png.jpg]]

Emoji Toolbar plugin in action

# Plugin: Banners

You may have noticed that many of my pages have a delightful image running across the top. I like to select images related to the topic of a page. These images contribute to the brain’s emotional connection to the page through a visual representation. These image banners put me in the proper “mood” for working with that page.

As much as I like note-taking, I don’t always enjoy it. So the image banners can stimulate the emotional centers of our mind that spur us on.

For this, I recommend installing the Banners plugin. This plugin can add a banner to the top of a page and properly do all the work to format it for height and width.

By the way, for the Dashboard++ method, I recommend changing the default height of banners to 150. This can be done in settings of the Banners plugin:

![[../03 - MEDIA & FILES/0!JMdjJL96Q_gkX3or.jpeg.jpg]]

Banners is a great plugin. You can easily add banners to your pages from images you store in your vault or from the internet. I enjoy browsing [https://unsplash.com/](https://unsplash.com/) to find good banners. After you get a collection of images in your vault, they can be easily accessed through the Banners plugin via the command palette.

![[../03 - MEDIA & FILES/0!JTceGWIryCwuLAfZ.png.jpg]]

Choosing from images to make a page banner

# Adding a Page Title

You may have noticed on my home page that the word HOME appears in the banner area of the page. How is this accomplished? The dashboard.css includes some formatting for positioning a title in the banner. To add your title to a banner, you add the following HTML to your page:

<div class="title">HOME</div>

Obsidian allows us to type HTML directly into a page. When in Reading view, this HTML is rendered.

As I mentioned, dashboad.css contains the formatting you need to make this work. The key is to add the class=” title” to the DIV element.

Since it is just HTML, you can even add additional style elements, for example, to change the color of the text:

<div class="title" style="color:Sienna">HOME</div>

Notice the sytle=” color:Sienna”, which can be changed to a preferred color. I like to use this [page at w3schools](https://www.w3schools.com/cssref/css_colors.asp) to find out what CSS colors are available.

![[../03 - MEDIA & FILES/0!2PpBiPQ2RaYCWWpg.png.jpg]]

w3schools list of CSS colors

# Plugin: Homepage

This is another super cool plugin. It allows you to define a home page that Obsidian opens when opening your vault.

![[../03 - MEDIA & FILES/0!khOLYckec8yr-kP9.png.jpg]]

Here you see I have defined my startup home page and set it to open in Reading view.

The homepage also has a command palette command for opening your homepage. I have assigned a hotkey **ALT+H** to open my home page. So no matter where I am in my vault, I can always return quickly to the home page, which serves as a center point for navigating my personal Wikipedia.

# Plugin: Customizable Page Header and Title Bar

This plugin gets my vote for the worst named plugin and my vote for one of the most useful. It allows you to add additional buttons to the Obsidian interface. You might have noticed in my screenshots that I have these buttons in the page header section of pages:

![[../03 - MEDIA & FILES/0!eQ1YgNg3Ki_tvwUO.png.jpg]]

I have added three buttons:

- The left arrow that navigates to the last page that was edited
- The right arrow that navigates you back to a page you just left
- Home button that opens your home page dashboard using the Homepage plugin

Here is what my settings look like for this plugin:

![[../03 - MEDIA & FILES/0!OVjfJwyGlkXBwqKB.png.jpg]]

I also recommend toggling on **Show buttons on desktop**.

# Plugin: Dataview

Dataview is a wildly popular Obsidian plugin. I use Dataview to display some simple information about the status of my vault, such as recently updated files, files that match a specific tag, and some stats.

![[../03 - MEDIA & FILES/0!ambpJUTc5-Lidoa1.png.jpg]]

Status of my vault via Dataview

This is a bit more advanced, but I think even if you don’t know JavaScript, you can copy and paste this into your Dashboard if you would like to have these Dataview queries in your Dashboard.

# Vault Info
- 🗄️ Recent file updates  
 `$=dv.list(dv.pages('').sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`  
- 🔖 Tagged: favorite   
 `$=dv.list(dv.pages('#favorite').sort(f=>f.file.name,"desc").limit(4).file.link)`  
- 〽️ Stats  
	- File Count: `$=dv.pages().length`  
	- Personal recipes: `$=dv.pages('"Family/Recipes"').length`

It is beyond the scope of this article to explain the code, but basically, I am using the inline JavaScript feature of Dataview to create a list displayed in the Dashboard.

If you use this feature of the Dashboard, you will need to install the Dataview plugin, and in the settings for this plugin, enable JavaScript support by toggling on these two options:

![[../03 - MEDIA & FILES/0!xat2QSFUrME4EZ-L.png.jpg]]

# Sources of Inspiration

I have been in the pursuit of effective note-taking tools and knowledge management solutions for about 25 years. Dashboard++ is building on a few concepts I have seen along the way. I share them here to provide additional context that might help you in your pursuits.

## Yahoo of the 2000s

I know this sounds funny, but I remember in the early 2000’s how much I enjoyed using Yahoo. Yahoo was a decent search engine, but the most useful was how they categorized content into topics. They had a large team that ranked sites into topics and subtopics, if I understand correctly. They then presented these on a page that showed main topics with subtopics.

![[../03 - MEDIA & FILES/0!01p3320CR8BMbTVE.png.jpg]]

Yahoo categorized pages into topics.

My goal with Dashbaord++ is similar. As time moves along and I create and refine more notes, I want to curate these notes into collections of related topics with a simple way to navigate those related topics.

## Wikipedia

This source of inspiration probably doesn’t require too much explanation, as most people value Wikipedia and its interlinked content approach.

Notice in the following picture how Wikipedia organizes content. They have categories of topics that link to pages. Each page often has many pages leading to other pages.

![[../03 - MEDIA & FILES/0!H8PglII-wvwl_LBz.png.jpg]]

Wikipedia organized by category into pages

The wonderful thing about Wikipedia is that you learn about one thing, but its connectivity to other topics keeps you there. You almost always learn about multiple things.

This is the kind of experience I want in my personal Wikipedia.

I usually come from the right side of this picture, creating notes that eventually feed into topics in my dashboards.

## Nick Milo’s Map of Contents

A recent source of inspiration is [Nick Milo’s](https://twitter.com/NickMilo) Map of Contents. You can get more info from the [LYT website](https://notes.linkingyourthinking.com/Umami/LYT+Kit). As Nick says on his site: “In a nutshell, MOCs help you gather, develop, and navigate ideas.”

![[../03 - MEDIA & FILES/0!zCGe6wh4jxgGpXlE.png.jpg]]

LYT Kit

This is basically what I am trying to do, but with a different layout than the standard Obsidian links page.

Nick’s material is worth the time to check out since you will learn more about the life cycle of the birth of a single note to its integration into a more extensive collection of information.

# That’s A Wrap

Dashboard++ is a straightforward concept using simple features of Obsidian. I intentionally avoided adding too many advanced features to be easy to use and thus no mental friction.

I can tell you that the number of dashboards I have in my vault continues to increase in number, and I am better at organizing my notes, grouping them, and linking them.

I am also finding it easier to rediscover my notes because the dashboard structure nurtures retention.

As always, please reach out to me on [Twitter](http://twitter.com/tfthacker) with your opinions on this approach or let me know if I can be of further help.

Thank you for reading this article. Please check out more of my work at [https://tfthacker.com](https://tfthacker.com/)
