---
title: "Quick way to add or append notes without opening Obsidian (Android tutorial) - Share & showcase - Obsidian Forum"
source: "https://forum.obsidian.md/t/quick-way-to-add-or-append-notes-without-opening-obsidian-android-tutorial/57547"
author:
  - "[[Obsidian Forum]]"
published: 2020-07-01
created: 2025-01-02
description:
tags:
  - "clippings"
---
## Issue

Opening Obsidian on Android is *slow*, so are all solutions that uses URI/intent to interact with Obsidian, for example:

- [Lumberjack 151](https://github.com/ryanjamurphy/lumberjack-obsidian)
- [Advanced URI + Tasker/Automate 140](https://notes.joschua.io/50+Slipbox/How+to+add+an+Obsidian+note+to+the+homescreen+on+Android)

This becomes a pain point, especially with notes that usually taken on-the-go, such as:

- Reminders
- Fleeting notes
- Time log entries

## Solution: Edit markdown files directly

![demo](http://imgur.com/lKDsbDW.gif)

## Apps required

- [MacroDroid 116](https://www.macrodroid.com/) (5 macros for free)
- Optional: [Quick Settings (by Simone Sestito) 77](https://play.google.com/store/apps/details?id=it.simonesestito.ntiles) to create the notification tile

## Set up
### MacroDroid

Create a new macro `QuickAdd` in MacroDroid with the following settings:

- Trigger:
- `User Input` > `Shortcut Launched`
- Actions:
1. `Variables` > `Set Variable`
- Select `[New Variable]` to create a local variable `input` for storing the QuickAdd input:
- Select `Local`
- Name: `input`
- Type: `string`
- Select `[User Prompt]` to define the overlay prompt:
- Title: `QuickAdd`
- Un-check `Display existing value`
2. `Files` > `Write to File`
1. Folder: `<YOUR_DAILY_NOTE_FOLDER>`
2. Filename: `{year}-{month_digit}-{dayofmonth}.md` (Use “…” to insert other fields)
3. Enter text: `\n-[ ] {lv:input}` (This will make a new line, insert a checkbox followed by the text previously stored in the local variable `input`.)
4. Select `Append to file`

### Home widget

The macro can be triggered using the widget `MacroDroid Shortcut`. The icon is customisable.

### Optional: Quick Settings (notification tile)

Although one can create notification tiles directly from MacroDroid, extra app permission must be granted to the app to do so.

The same can be achieved with the Quick Settings app:

1. `Shortcuts` > `App & Shortcuts #1` > `Enable tile`
2. Edit the notification tiles, find the `Application & shortcut` tile
3. `MacroDroid Shortcut` > `QuickAdd`

## Inspiration

[Cool & useful Android shortcuts (made with MacroDroid) (and a tutorial on using URIs as intents on Android) 75](https://forum.obsidian.md/t/cool-useful-android-shortcuts-made-with-macrodroid-and-a-tutorial-on-using-uris-as-intents-on-android/26683)

---

P.S. The previous topic was deleted because I would like to clarify the use cases, but it was no longer editable.

Do the file sync without opening Obsidian?

This macro directly edits the same markdown file that is seen by Obsidian. Whenever Obsidian Sync is triggered, it sees that this file inside the vault folder has been modified and will sync it, even if the file has never been opened in Obsidian.

Note: At the moment, Obsidian Sync only runs when Obsidian itself is in the foreground.

So you can open Obsidian to bring it to the foreground (any page will do) and trigger synchronisation of all files modified by the macro.

I was hoping that wasn’t going to be your answer. I’m glad to see I’m not the only one who wants background sync. Thanks for sharing that link.

I really dig your solution, and once the sync issue is addressed, I will likely be using it.

To avoid sync conflicts, You can have a dedicated “inbox” note for each device.

[@the0](https://forum.obsidian.md/u/the0) and everyone else in this thread - there is a very easy bulletproof solution for the syncing problem:

**Open Obsidian as the first step in your automation ![:grin:](https://forum.obsidian.md/images/emoji/apple/grin.png?v=12 ":grin:")** 

I’m using [Automate 40](https://play.google.com/store/apps/details?id=com.llamalab.automate) on Android, but I’m sure you can do this with MacroDroid too.

Here’s a video. I tell Obsidian to launch, and then pop up the input box for my new task. By the time I’ve finished typing the task, Obsidian is already opened and syncing away. This has completely solved any sync-related quick-add issues for me.

**Note:** I am still directly editing the Markdown file as per the first post, I’m just also opening Obsidian so it can start syncing while I enter my text.

![ezgif-4-4cb450d5a5](https://forum.obsidian.md/uploads/default/original/3X/e/f/ef2dfe619fd96a00f3efc4514687f1262d4ac507.gif)

Here’s the Automate flow, very simple:

[![Screenshot_20230811_153920_Automate](https://forum.obsidian.md/uploads/default/optimized/3X/1/3/134677c2aebe237fc0e9fde2a0968d5145b60bf6_2_293x500.jpeg)](https://forum.obsidian.md/uploads/default/original/3X/1/3/134677c2aebe237fc0e9fde2a0968d5145b60bf6.jpeg "Screenshot_20230811_153920_Automate")

And the Automate flow itself if you want to import it:

If you didnt add a 40mb file recently, or do some other overhaul that requires major syncing

Even still, if you add tasks multiple times per day it’s multiple chances to get all synced up. And Obsidian doesn’t stop syncing immediately when you switch away, it will keep going for a while.

And really, how often do you in your day-to-day use do an overhaul that requires major syncing?

Well even if its just 5-10 seconds of syncing, if I want to append something very quick to the same note (like todays daily note) frequently across devices, I’m still typing into the textbook and just waiting and hoping it has synced.

Maybe I only have the 10+ sync thing happening once/week but either way it’s a pain waiting, hoping things are synced before hitting enter. That’s why I created a shortcut that adds to a per-device note.

iPad adds to the iPad note, iPhone adds to the iPhone note, etc. I have another automation that later combines them daily (with lots of delays between steps for syncing)

And this will effectively guarantee that your per-device note will be synced after you finish your quick append, even if you immediately switch away after inputting your data.

I’m not really sure what you’re trying to argue - they’re complimentary approaches which work together to improve your sync success rate.

[@the0](https://forum.obsidian.md/u/the0) Thank you for making the guide for the shotcut in MacroDroid, altough I’m only halft way there. I have copied your setting for the shortcut, but when I make a note the output/text in Obsidian is this: - {lv:input}  
Is there a simple solution or did I miss something? Also Is there a way to incorporate the time of day with adding notes to Obsidian through MacroDroid?

I faced this same problem a few times and looking for a solution I found this post, which sparked an idea in me.

Just yesterday I made public an application (called [CopyCapture 101](https://play.google.com/store/apps/details?id=com.hector6872.capture); so yes, I’m aware it’s not the best of names tho) that I’ve been using for a while to capture snippets, reminders or ideas quickly (and then save them all at once in Obsidian).

[Try it out 101](https://play.google.com/store/apps/details?id=com.hector6872.capture) and let me know what you think ![:slight_smile:](https://forum.obsidian.md/images/emoji/apple/slight_smile.png?v=12 ":slight_smile:")

DISCLAIMER: there is neither self-promotion nor search for free leads. The app is completely free and has no ads or in-app payments.

A fast simple markdown note app called Notes by a Dev named Bill Farmer availablenin F-droid and Github a way to quick add notes that can automatically have timestamp in the file name.

I had the same issue with `{lv:input}` appearing in the note, but was able to get the instructions to work by changing `{lv:input}` to `{lv=input}` in the MacroDroid “Write to File” action.

Sorry for the late reply. As [@nicholassdesai](https://forum.obsidian.md/u/nicholassdesai) pointed out it should be `=`. This is what I use for Obsidian v1.4.9, MacroDroid v5.37.12:

`\n- [ ] {lv=input}`

Hope that helps.

Thanks so much for the OP and clarification here, [@the0](https://forum.obsidian.md/u/the0). Just got it setup, and it’s working well.

I did modify the Macrodroid macro to open Obsidian as the first action, to begin sync as [@AlanG](https://forum.obsidian.md/u/alang) suggested as a solution for the syncing problem.

[@hector6872](https://forum.obsidian.md/u/hector6872) - I’ve just installed your app, and if I understand correctly, it looks like it’s a glorified clipboard to use the system share to add to, and then all at once, copy all items from and manually add to Obsidian. Is that correct?

Sort of. The main idea behind it is (for example): you browse a website, send the main/most interesting points to CopyCapture (or add them manually), then merge it and share it in an single Obsidian note. Which is (in my case) more productive than using Obsidian directly.

Fastest way on Android I’ve found so far (and it’s *built* to sync with Obsidian): **Fleeting Notes**. [Web app 49](https://www.fleetingnotes.app/), [Android app 49](https://www.fleetingnotes.app/), and [matching obsidian plugin 9](https://github.com/fleetingnotes/fleeting-notes-obsidian), sync can be one-way or both-ways. The client source code is open source (backend isn’t yet, as it uses “nosource” solutions that make opensourcing a challenge).

That said, it’s more a “single channel” (i.e. you sync into a single location in a single vault). Think of it as a Google Keep front-end on one of your notes folders, though with some creative tagging and inbound processing in obsidian, you can do much more.

Very fast, frictionless. It could use some polish, but it’s been easy to setup and use.

Hey Im new here.  
I come up to this when I already had a workflow for quickCapture established.  
I use the App “Notes” from Simple Mobile Tools. (in the future hopefully from Fossify forked and published)  
Within that App you can open any plaintext file located in your Storage.  
So I choose three Notes from Obsidian and put them via a Widget on my homescreen.

1. Its opening very fast
2. you can read and change everything what is yet in that note
3. you can scroll from the homescreen in the widget through the note

Hi [@AlanG](https://forum.obsidian.md/u/alang) - having trouble with your Google Drive link. It keeps failing to download. Would you be able to check it?