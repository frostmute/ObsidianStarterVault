---
created: 2024-05-15T02:09:46 (UTC -05:00)
tags: []
source: https://www.whatismybrowser.com/developers/tools/wget-wizard/
author: 
banner: https://cdn.whatismybrowser.com/prod-website/static/main/content/developers/tools/wget-wizard.png
---

# Wget Wizard - WhatIsMyBrowser.com

> ## Excerpt
> Wget Wizard helps you use Wget with an easy to use User Interface to control the most popular options, so you don't need to look the up each time.

---
## Introduction

[Wget](https://www.gnu.org/software/wget/) is an amazing open source tool which helps you download files from the internet - it's very powerful and [configurable](https://www.gnu.org/software/wget/manual/wget.html). But it's hard to remember all the configuration options!

### What does this Wizard do?

This form won't actually download the files for you; it will suggest the command you could run to download the files with Wget on your computer or server. It's like a GUI for Wget.

## Comments, questions?

Constructive feedback on this system is always welcome. If you have any ideas for additions or changes, [we'd love to hear about it](https://www.whatismybrowser.com/about/contact/).

### Things we'd love your feedback on:

_We welcome all feedback, but here's a few items we'd particularly love your thoughts on:_

-   We've included some basic "meta data" filenames; (DS\_Store, Thumbs.db, thumbcache.db)... but are there any more we should include in the sample command? Please suggest some!
-   Are there other command options that you use frequently or find confusing and want added here as well?
-   Is the user interface for this wizard clear enough? Is there anything you were initially confused by, or couldn't figure out?

Is there anything you want to let us know? [Get in touch!](https://www.whatismybrowser.com/about/contact/message)

### Problems with Wget

These are some things we can't seem to get wget to do properly; if you have any ideas, let us know!

-   **Maximum crawl depth** is ignored by wget if **Get complete mirror** is chosen! It seems like it should work; instead of adding the --mirror option (which according to the docs is equivalent to \`-r -N -l inf --no-remove-listing\`, we set those parameters manually and omit \`-l inf\`, instead using whatever value is specified in **Maximum crawl depth**. However wget doesn't respect this value and still crawls many levels deep.

### Usage notes

This isn't meant to be an exhaustive list of every single configuration option or variation of configuration option... it just provides a nice balance of usability without over-complicating the user interface for the "average" user. For example, _really_ advanced options like timeouts, quotas, IP families, encoding, POST data, globbing, content-disposition and so on, are omitted from this wizard. If you use them, you should really [read the documentation](https://www.gnu.org/software/wget/manual/wget.html) and understand it enough to build your own command settings.

Only use wget if you know what you're doing. If you have questions; ask; we're always happy to help people who have done as much research as they're able to; your questions might also help us improve this tool for everyone. Don't use it to pirate stuff or do other illegal things. Don't overload servers with it. Be respectful to the sysadmins and developers who run the sites you love to use and don't overload them.

Make sure you have read and agree to our [Terms and Conditions](https://www.whatismybrowser.com/about/legal/), in particular the [Wget Wizard](https://www.whatismybrowser.com/about/legal/#wget-wizard) section before using this wizard.

You are encouraged to use the sample command this tool generates as the foundation of the command you actually need... for example, if you want to add other "meta-data" file types to ignore, copy the command and edit it before running it! We hope you find this wizard useful.
