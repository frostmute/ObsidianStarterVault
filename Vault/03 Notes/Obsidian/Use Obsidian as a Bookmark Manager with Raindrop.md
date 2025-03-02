---
cssclasses:
  - bannerimage
created: 2024-12-23
source: https://freedium.cfd/https://medium.com/the-obsidianist/use-obsidian-as-a-bookmark-manager-with-raindrop-3df00f4a0b70
tags:
  - clippings
---
# Use Obsidian as a Bookmark Manager with Raindrop

Recently, I've added a new feature to my Obsidian vault. I can now use it as a bookmark manager. Well, not a real bookmark manager, but I can use it to store content from the web and turn it into notes easily. It's the perfect compromise between Obsidian and a bookmark manager.

I'm going to share with you my workflow to do this.

#### 1\. Raindrop

[Raindrop](https://raindrop.io/) is a bookmark manager. It allows you to save content from the web, and eventually store it in collections.

I've come through an issue when consuming content from the web. Sometimes, there are Reddit posts I want to read later, YouTube videos I want to see later, books found on GoodReads I want to read later, etc…

Many of these apps allow you to save content to read/watch later. But for me, I don't find it convenient to look at several places to find everything I've saved.

Using Raindrop allows me to bookmark anything I want to consume later and to gather everything in the same place. I can now bookmark YouTube videos, Reddit posts, Medium articles, etc… and then go to Raindrop to find everything I've saved instead of going through my "Watch later" list in each app.

This is the first step of my workflow: having a place to gather all the content I have to consume.

#### 2\. Raindrop -> Obsidian

Once you have everything in the same place, you have to sync content from your bookmark manager with Obsidian.

We're lucky, people have made a plugin to sync content from Raindrop to Obsidian in a convenient way. This plugin is called "Raindrop Highlights". Just download it and enable it.

By the way, I use Raindrop, but you can use any bookmark manager as long as you have a way to send its content to Obsidian.

You can then connect the plugin to your Raindrop account. Open the plugin settings, and click on "Connect". Log in to your Raindrop account and click on "Developer Settings" from the plugin settings. Then, you just have to create an application from Raindrop to get your "Test Token" and use the API.

#### 3\. Highlight Template

Once you've connected Obsidian to Raindrop, you choose a folder from the plugin settings to store your highlights. For me, it's just a folder called "Media". In this folder, there is everything, not just bookmarks. For example, there are also reference notes about the books I've read, notes about some attachments in my vault, etc…

By default, the plugin will create folders linked with your Raindrop collections to store bookmarks inside. So for example, let's say you have a "Videos" collection in Raindrop, a "Videos" folder will be created inside your Raindrop highlights folder to store everything you've stored in the "Videos" collection.

I don't like this behavior so I've modified the plugin's code to disable this. I've sent my code to the plugin's maintainers, so I hope in the next update my feature will be implemented, but for now, if you want the modified version feel free to ask me.

To keep track of what my bookmarks are without folders, I've modified the default template to tag the bookmark's note correctly. Here is the YAML I've added:

```css
tags: medias/{{collection.title}}
```

This way, all the Reddit articles I've saved are tagged as "media/reddit" (because I have stored them in a "reddit" collection in Raindrop), all my YouTube videos are stored as "media/youtube", etc…

I've not modified the default highlight template, and I've added other YAML attributes, but I will talk about it in another article because I use them for a specific purpose.

#### 4\. Dataview

Dataview is a wonderful plugin to turn your vault into a database. I'm just going to tell you how I use dataview with this workflow, I won't explain how dataview works, so if you don't know it yet, you can check [this article](https://medium.com/@estebanthi/obsidian-dataview-build-your-vault-as-a-database-fb3920f8cd79).

So, I use dataview to have an overview of all my bookmarks. This way, I don't have to open Raindrop every time I want to see them. Here is my dataview query:

````
```dataview
TABLE
tags as Type,
FROM "200 Media"
```
````

Now, you have direct references to all your bookmarks within Obsidian. Here is how the dataview query looks when parsed:

![None](https://miro.medium.com/v2/resize:fit:700/1*72LBF-Tj9SovNoxwUPqPJw.png)

#### Final Note

Using the Raindrop plugin to sync bookmarks from Raindrop into Obsidian is a great way to combine the best of both worlds.

You get the convenience and organization of a bookmark manager, along with the flexibility and power of Obsidian for taking notes and creating a web of knowledge.

*Find all my Obsidian-related stuff here:* *[Use Obsidian like a Pro](https://medium.com/@estebanthi/use-obsidian-like-a-pro-3946cd68cca0)*

*To explore more of my self-improvement stories, click* *[here](https://medium.com/@estebanthi/self-improvement-845668b69bd0)**! You can also access all my content by checking* *[this page](https://medium.com/@estebanthi/about-me-d63607c8c341)**.*

*If you liked the story, don't forget to clap, comment, and maybe follow me if you want to explore more of my content :)*

*You can also subscribe to me via email to be notified every time I publish a new story, just click* *[here](https://medium.com/subscribe/@estebanthi)**!*

*If you're not subscribed to Medium yet and wish to support me or get access to all my stories, you can use my link:*
