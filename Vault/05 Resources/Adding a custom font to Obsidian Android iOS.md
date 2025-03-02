Hi, I want to share how I added a custom font to Android/iOS devices. This technique employs Obsidian’s CSS snippet feature so you do not need to install or create a custom theme.

You need a WOFF2 file for your custom font. If you only have TTF file or something, convert them to WOFF2. There are plenty of tools online to do this.

Convert WOFF2 to base64-encoded string and embed it in fonts.css file (you can name this file as you want). You can do this on https://hellogreg.github.io/woff2base/ 1.6k. Copy the generated string to your CSS file.

Add your fonts.css under .obsidian/snippets/ folder.

Open Obsidian and go to Settings > Appearance > CSS snippets and enable your fonts.css.

Now Obsidian will recognize your custom font even if your phone does not have it. You can go to Settings > Appearance > Font and change the font to yours.

If Obsidian does not recognize your font, check the font-family property in your fonts.css. font-familiy property and Settings > Appearance > Font setting must exactly match.


