---
title: "Clip an article straight to your Obsidian with one click - Share & showcase - Obsidian Forum"
source: "https://forum.obsidian.md/t/clip-an-article-straight-to-your-obsidian-with-one-click/2615"
author:
  - "[[Obsidian Forum]]"
published: 2020-07-01
created: 2025-01-02
description:
tags:
  - "clippings"
---
I’ve checked out solutions available [here 281](https://forum.obsidian.md/t/how-do-i-get-content-from-websites-into-my-notes/1738), but the ones I’ve tried require too much friction:

1. click on the button,
2. copy the text,
3. create a new file manually,
4. paste the text.

Some of them do download the actual file, but they place it in `~/Downloads` and you have to manually move them over.

My solution:

1. click on the button in your browser.

That’s it! It automatically creates the file, adds some metadata at the top of the Markdown file, and you can see it straight from your Obsidian.

## Example

- I went to the random article on my Medium homepage: [https://medium.com/@lancengym/the-endgame-for-linkedin-is-coming-31d4a8b2a76 71](https://medium.com/@lancengym/the-endgame-for-linkedin-is-coming-31d4a8b2a76)
- I clicked on the button, which created a file named `20200701-the_endgame_for_linkedin_is_coming.md` whose top looks like this:

```markdown
# The Endgame for LinkedIn Is Coming

* **Source:** [medium.com](https://medium.com/@lancengym/the-endgame-for-linkedin-is-coming-31d4a8b2a76)
* **Author:** Lance Ng
* **Word count:** 1844
* **Extracted at:** 2020-07-01 14:03

![lead image](https://miro.medium.com/max/1200/1*F13E-o2ErInkVjeIFGw9rA.png)

After two years, Microsoft still hasn’t delivered on its grand vision for LinkedIn. And it may never do so. [...]
```

It saves the full content, adds some metadata, and loads images externally from the same location as the article.

## How to set it up

1. Make sure you have python3 installed, though it should be available out of the box in most Linux distributions.
2. Install [mercury-parser 65](https://github.com/postlight/mercury-parser/) somewhere in your path: `npm -g install @postlight/mercury-parser` (`yarn` also works).
3. Modify the 9th line in the script below to point to the directory where you will store the links. Use absolute path instead of relative (so `/home/input_sh/Notes` instead of `~/Notes`).
4. Install [External Application Button 118](https://add0n.com/external-application-button.html) in your preferred browser.
5. Fill out its preferences like this:

[![Screenshot from 2020-07-01 14-05-41@2x](https://forum.obsidian.md/uploads/default/optimized/2X/7/7f9002362fa05283b8984fb5d808230ea5851ddd_2_327x250.png)](https://forum.obsidian.md/uploads/default/original/2X/7/7f9002362fa05283b8984fb5d808230ea5851ddd.png "Screenshot from 2020-07-01 14-05-41@2x")
6. There’s also a “Surround arguments with quote characters” option below what’s visible in the screenshot, which would be nice to tick. Optionally, you can also upload a custom icon to be shown in your browser’s interface (32x32), as well as to close the tab automatically when the button in clicked.

## Script

```python
#!/usr/bin/python3
# -*- coding: utf-8 -*-

import os, sys, json
import datetime

link = str(sys.argv[1])
print("Processing " + link)
directory = "/home/input_sh/Notes/Links/"

resp = json.loads(os.popen("mercury-parser " + link + " --format=markdown").read())
today = datetime.datetime.now()

out_content = resp["content"]
out_title   = resp["title"]
out_url     = resp["url"]
out_domain  = resp["domain"]
out_wc      = resp["word_count"]
if resp["author"]:
    out_author = resp["author"]
else:
    out_author = "Unknown"

# Ewww, www
if "www." in out_domain:
    out_domain = out_domain.replace("www.", "")

if resp["lead_image_url"]:
    out_lead_img = resp["lead_image_url"]
    header = "* **Source:** [" + out_domain + "](" + out_url + ")\n* **Author:** " + out_author + "\n* **Word count:** " + str(out_wc) + "\n* **Extracted at:** " + today.strftime("%Y-%m-%d %H:%M") + "\n\n"
    content = "# " + out_title + "\n\n" + header + "![lead image](" + out_lead_img + ")\n\n" + out_content
else:
    header = "* **Source:** [" + out_domain + "](" + out_url + ")\n* **Author:** " + out_author + "\n* **Word count:** " + str(out_wc) + "\n* **Extracted at:** " + today.strftime("%Y-%m-%d %H:%M") + "\n\n---\n\n"
    content = "# " + out_title + "\n\n" + header + out_content

# Formats the title of the file
title = today.strftime("%Y%m%d-" + out_title)
title = title.lower().replace(" ", "_").replace("(", "").replace(")", "")

# Writes to the actual file
f = open(os.path.join(directory + title + ".md"), "w+", encoding="utf-8")
f.write(content)
f.close()

print("Done!")
```

Don’t forget to make the script executable! If you’ve saved the script as `web-clipper.py`, you’d do something like `chmod +x web-clipper.py`. You can test if it works from your terminal by running `./web-clipper.py "https://medium.com/@lancengym/the-endgame-for-linkedin-is-coming-31d4a8b2a76"` before you proceed with setting up External Application Button.

Feel free to let me know if you encounter some quirks.

Howdy,  
Great potential here, I am getting the One Last Step page with a successful check of the connection and the correct path to the folder I want the links in:

D:\\Files\\Vault\\ObsidianVault\\02 - Links

Obviously I am doing something wrong.

Guy Pelletier

[@input\_sh](https://forum.obsidian.md/u/input_sh)  
Thanks for that script! I was thiking about a better way to clip articles and you just found the perfect soluton for me ![:purple_heart:](https://forum.obsidian.md/images/emoji/apple/purple_heart.png?v=9 ":purple_heart:")

[@glpelletier](https://forum.obsidian.md/u/glpelletier)

Make sure you don’t use spaces in the path, that will result in errors.

Before you use the browser extensions test/debug the script one time in the terminal to make sure it works correctly with `./path/to/web-clipper.py`

There might be some caveats:

- The script is not executable by default (on linux just make it executable with `chmod a+x web-clipper.py`)
- Ther mercury parser is not installed correctly, it might help to install it globally with `yarn global add @postlight/mercury-parser` (see documentation)

Sorry I can’t give exact instructions for windows but this might be a start.

Thanks for the reply, I will give it a shot and let you know how it goes.

Guy

If you get an error `bad interpreter` then you can change the shebang line (first in python script) to `#!/usr/bin/env python3`

if you still get that error you need to make sure python 3 is installed

Hi,

many thanks ![:slight_smile:](https://forum.obsidian.md/images/emoji/apple/slight_smile.png?v=9 ":slight_smile:")

I have a strange problem…

1. Direct call: ./web-clipper.py “[https://medium.com/@lancengym/the-endgame-for-linkedin-is-coming-31d4a8b2a76 6](https://medium.com/@lancengym/the-endgame-for-linkedin-is-coming-31d4a8b2a76)” works perfect
2. The same call from External Application Button displays the error:  
Error: /bin/sh: mercury-parser: command not found  
So, it calls web-clipper.py correctly, but it looks like the python script can’t call mercury-parser.

I’ve configured External Application Button as you suggested.

Any idea?

Many thanks in advance, Your script is a really killing feature to me…

Yours,

Andy

[![Zrzut ekranu 2020-07-17 o 17.11.34](https://forum.obsidian.md/uploads/default/original/2X/b/b16482a5fed1c685cad9cf426322434b7a885651.png)](https://forum.obsidian.md/uploads/default/original/2X/b/b16482a5fed1c685cad9cf426322434b7a885651.png "Zrzut ekranu 2020-07-17 o 17.11.34")

Rather than loading the images externally, it would be great if there was the option to clip the images locally as well.

I realize that it can be done manually.

Clipping text only from a web site is essentially 50% a bookmark as you still need access to their web server to load the images.

I prefer to keep the content of everything I clip locally. It wouldn’t do me much good if the pictures contain some information necessary for the text to make sense & I either don’t have an internet connection, the site was taken down, the article was removed, etc.

Hi,

Did you find a solution to this problem?  
I’m having the same issue, and can’t find a way to solve it.

Great job, I’d definitely try it.

Is there a way to extract images and other media together with the article, so that I don’t need a connection to access them?