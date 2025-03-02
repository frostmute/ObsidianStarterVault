# [How to Build Beautiful Dashboards With Obsidian Canvas](https://www.productnook.com/tag-dashboards-with-obsidian-canvas/)
Are you just getting started with Obsidian? If so, our [Obsidian Essentials e-book](https://www.productnook.com/obsidian-essentials/) can help you get off the ground running. Want to be involved? You can even suggest content if you're interested in learning a specific topic. Find out more [here](https://www.productnook.com/obsidian-essentials/).

The beauty of Canvas is that you can shape it into whatever you need it to be. I've already [discussed at length](https://www.productnook.com/obsidian-canvas-excalidraw-for-product-management/) about how I use Canvas for product development, but I was also looking for a solution that allowed me to easily surface *and* group together notes that I had tagged, with whatever contextual information I wanted to display.

The **Kanban** plugin doesn't easily allow for this kind of workflow, though it *would* be great if I could configure a list to "pick up" whatever I specify, and the more recent **Cardboard** which *does* was just a bit too involved. **Dataview,** unfortunately, only allows for the note name rather than the note contents to be displayed. While I didn't dive too deeply into Dataview, I wanted to stay as lightweight as possible.

Instead, I turned to using Obsidian's native [embedded queries](https://help.obsidian.md/Plugins/Search?ref=productnook.com#Embed+search+results+in+a+note) which is really just a simple search function.

```
```query
tag:#task
```


Querying for the #task tag

This query will get you 90% of the way there, but with queries there is no inherent markdown styling and it will either look a little barebones, or your themes and added CSS snippets will distort the appearance, so I went digging for a way to render the embed nicely.

Previously, I had used [Obsidian Query Control](https://github.com/nothingislost/obsidian-query-control?ref=productnook.com) by [@NothingIsLost](https://github.com/nothingislost?ref=productnook.com) to do this, but as of Obsidian 1.2.x, this is no longer supported (nor in active development). At this time, I **highly recommend** using Obsidian Tasks for querying specific tags instead.

I've written a small series on how I use Obsidian Tasks. For this particular article, the first in the series is likely all you need to get started, but you can read the others if you want to get *fancy*.

Once you're all set up with Obsidian Tasks, you'll want to create a new note that houses all of your individual tag queries which will drive the Dashboard. I've just called mine `Canvas Queries`, and added a query for each tag I'd like to be displayed in Canvas under its own respective heading. **The heading step is important, otherwise you can't set Canvas to just look at a specific section of the note.** For example:

```
### Zelda

```tasks
tags include zelda
not done
hide edit button
```


If you've set up Obsidian Tasks, this query will result in something similar to the following output, where all my `#zelda` tags are picked up.

<img alt="" src="https://www.productnook.com/content/images/2023/05/CleanShot-2023-05-29-at-20.56.16.png" height="513" width="790" />

Example #Zelda Tasks

I've tweaked the CSS a bit here such that the backlink is only displayed on hover, so they're hidden in this screenshot. Also note that if you've set a `Global Task Filter` for Obsidian Tasks, these tasks will only be picked up if the task also has the filter. For me, that's `#task`, as shown below. If you don't set a `Global Task Filter`, *all* tasks will be picked up.

<img alt="" src="https://www.productnook.com/content/images/2023/05/CleanShot-2023-05-29-at-21.00.34-1.png" height="187" width="578" />

Once you have a few queries embedded into your `Canvas Queries` note, you can throw them onto your Canvas for as many tags as you want displayed, simply drag the note onto the Canvas and use the `Narrow to heading...` contextual menu option to only display *that* tag header.

<img alt="" src="https://www.productnook.com/content/images/2023/05/CleanShot-2023-05-29-at-21.04.46.png" height="726" width="1031" />

It's that simple. You can then make your dashboard as expansive or as minimal as you want. You could even create *multiple* dashboards depending on individual usecases, or themes. **The Canvas is your oyster.**