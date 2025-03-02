---
source: https://forum.obsidian.md/t/get-your-raindrop-io-bookmarks-into-obsidian-using-pandoc/17576
---
# Get your Raindrop.io bookmarks into Obsidian using Pandoc

’ve been wanting to centralize all my notes and knowledge into something cohesive, so I came up with the idea of importing my [Raindrop.io 44](https://raindrop.io/ "raindrop.io/") bookmarks directly (and automatically) into my knowledge base in Obsidian using [Pandoc 151](https://pandoc.org/). I thought some of you might be interested.

## Some caveats

These limitations could be fixed if you care to spend some time on the parsing or use the Raindrop API.

- Tags are not imported.
    
- The parsing is not perfect and some weird markup remains sometimes.
    
- **All** the bookmarks are imported (you can’t pick a specific collection).
    

## What you’ll need

- Raindrop’s [Automatic Backups 17](https://help.raindrop.io/backups#automatic-backups "Automatic Backups") feature activated (requires a [Pro plan 14](https://help.raindrop.io/premium-features) subscription)
    
- A Dropbox or Google Drive account.
    
- Pandoc installed on you computer.
    
- Mac OS (or any Linux / Unix based operating system).
    

## How it works

It’s actually much easier than you’d expect!

- Raindrops’ Automatic Backups exports an HTML file in your Dropbox (or Google Drive) shortly after you add or modify any link.
    
- Your computer then runs a cron job that runs a Pandoc command to convert the HTML file into a Markdown file, and saves it in your Obsidian vault directory.
    

## Step-by-step instructions

1. Activate Raindrop’s Automatic Backups (on Dropbox your file typically goes to `/Apps/Raindrop.io/`).
    
2. [Install Pandoc 56](https://pandoc.org/installing.html "Install Pandoc") if it’s not done already.
    
3. Modify your crontab (in your terminal, type: `crontab -e`) to execute the Pandoc command (mine runs every day at 5PM). Add the following line to the file: `0 17 * * * pandoc -s -r html /Users/username/Dropbox/Apps/Raindrop.io/Export.html -o /Users/username/Dropbox/path-to/yourvault/Raindrop-Bookmarks.md`
    

That’s it, you’re all set! You’ll now find in your Obsidian Vault a file called Raindrop-Bookmarks.md that has a markdown version of all your Raindrop bookmarks.

---

Cross posted here: [Get your Raindrop.io bookmarks into Obsidian using Pandoc - The Aspiring Nerd - Opinion, analysis and commentary around all things digital 65](https://theaspiringnerd.com/raindrop-bookmarks-to-obsidian-markdown-with-pandoc/)