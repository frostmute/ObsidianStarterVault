---
created: 2024-07-02
source: https://talk.tiddlywiki.org/t/copy-info-from-web-site-to-tiddlywiki-using-bookmarklet-and-json-tiddler-dropzone/6659
category:
  - "[[../00 - CATEGORIES/Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster](../03%20-%20MEDIA%20&%20FILES/4d2ca9093db55eae43fbe37a456978c0_MD5.jpg)"
feature: "![[../03 - MEDIA & FILES/4d2ca9093db55eae43fbe37a456978c0_MD5.jpg]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/4d2ca9093db55eae43fbe37a456978c0_MD5.jpg)

```meta-bind-button
label: Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "001"
style: primary
actions:
  - type: command
    command: editor:fold-all

```

***

```cardlink
url: https://talk.tiddlywiki.org/t/copy-info-from-web-site-to-tiddlywiki-using-bookmarklet-and-json-tiddler-dropzone/6659
title: "Copy info from web site to tiddlywiki using bookmarklet and json tiddler dropzone - Tips & Tricks - Talk TW"
description: "I created a json tiddler text deserializer for use with a Dropzone to import json tiddler text. It works, but turns out that there is a better way to do what I wanted. I shared my findings in this somewhat long post, maybe it will be helpful to somebody.  JSON TIDDLER DROPZONE  The use case I have in mind is to use bookmarklets to scrap info from specific web sites to the clipboard, and import into tiddlywiki by pasting (with CTRL-V) as json tiddler text in a dropzone. Tiddlywiki already support..."
host: talk.tiddlywiki.org
image: https://talk.tiddlywiki.org/uploads/default/optimized/2X/c/c9bda037af6b6c42c2054fba286fbdb703b367e4_2_733x1024.jpeg
```
I created a json tiddler text deserializer for use with a Dropzone to import json tiddler text. It works, but turns out that there is a better way to do what I wanted. I shared my findings in this somewhat long post, maybe it will be helpful to somebody.

**JSON TIDDLER DROPZONE**  
The use case I have in mind is to use bookmarklets to scrap info from specific web sites to the clipboard, and import into tiddlywiki by pasting (with CTRL-V) as json tiddler text in a dropzone. Tiddlywiki already supports import of json tiddler file using the import button and via drag and drop. In contrast, this approach aims to do the followings:

-   uses bookmarklets to capture info from web pages.
-   uses clipboard to export the captured info from bookmarklets, in view of the security-related constraints on bookmarklets.
-   uses json tiddler format to transfer multiple pieces of info, spread across one or more tiddlers, to tiddlywiki.
-   import by directly pasting (using CTRL-V) from clipboard to a dropzone in Tiddlywiki.

A simple use case is to copy a selection of text from a website, along with the site url and title and import as a tiddler like this:

```
  [ { <span>"text"</span>:<span>"A sample selection of text from a web site"</span>,
      <span>"type"</span>:<span>"text/vnd.tiddlywiki"</span>,
      <span>"title"</span>:<span>"Illuminate your world"</span>,
      <span>"url"</span>:<span>"https://thinking-about-things.com/"</span>} ]
```

This is similiar to the use case for BibTex, and from which I took the cue to create the json tiddler deserializer:

-   “Tiddlytalk: Drag and Drop and specified deserializer for string data” [https://groups.google.com/g/tiddlywiki/c/OR48TT\_loB8 2](https://groups.google.com/g/tiddlywiki/c/OR48TT_loB8)
-   “Tiddlytalk: Is there a way to create a tiddler using text that is stored in the clipboard?” [https://groups.google.com/g/tiddlywiki/c/Bn4ffIpe4B4/m/8pVUFVubBQAJ 5](https://groups.google.com/g/tiddlywiki/c/Bn4ffIpe4B4/m/8pVUFVubBQAJ))

The dropzone and deserializer works !! With it, I can select some text from a web site, launch the bookmarklet to copy the text and url to the clipboard, then click the dropzone in tiddlywiki and CTRL-V (paste) to import the info as a tiddler.

There are other bookmarklets I tried as well, such as to capture all the image links from a web site into a tiddler, or likewise, capture a list of local file links through the browser so they can be referenced within tiddlywiki. The latter is possible as the web browser can browse local file directories and file links in the directory page can be captured with a bookmarklet. The json tiddler dropzone and deserializer plus the bookmarklet examples are packaged in this json file: [json tiddler dropzone.json](https://talk.tiddlywiki.org/uploads/short-url/h5rFiY6u28W5LMmWQiOJVjiDwNL.json) (12.1 KB)

**JSON TIDDLER INPUT BOX**  
In my exploration before I hit on creating the json text deserializer myself (the thread above came closest to creating a json text deserializer yet somehow didn’t take that last step. Tiddlywiki has a built-in json text deserializer too for file import but I have no idea how to use it for my purpose. I copied it’s javascript codes instead for my json text deserializer ![:slight_smile:](../03%20-%20MEDIA%20&%20FILES/eba8244de357e7b93373e85af016f560_MD5.png ":slight_smile:")) , I found an alternate solution using text input box instead of a dropzone. The idea came from this thread “[Importing a tiddler with a specific name - #4 by sobjornstad 1](https://talk.tiddlywiki.org/t/importing-a-tiddler-with-a-specific-name/680/4)” by saqimtiaz which breakdowns the tiddlywiki file import button into its component steps:

`$browse -> import with deserializer -> Import preview using "$:/Import" tiddler -> tm-perform-import`

I learnt that if I start instead with a text input box that accepts json tiddler text in the format for “$:/Import”, I can create the “$:/Import” tiddler directly and send a “tm-perform-import” message to complete the importing, like this:

```
\define handleTextPaste()
    &lt;$vars textin=&lt;&lt;actionTiddler&gt;&gt;&gt;
    &lt;$action-createtiddler  
        $basetitle=<span>"$:/Import"</span> 
        type=<span>"application/json"</span> 
        plugin-type=<span>"import"</span> 
        status=<span>"pending"</span> 
        text=&lt;&lt;textin&gt;&gt; 
    &gt;
    &lt;$action-sendmessage $message=<span>"tm-perform-import"</span> $param=&lt;&lt;createTiddler-title&gt;&gt;<span>/&gt;
    &lt;/</span>$action-createtiddler&gt;
    &lt;<span>/$vars&gt;
\end

&lt;style&gt; .wideEdit { width:100%; } &lt;/s</span>tyle&gt;
&lt;$edit-text field=<span>"dropjsontext"</span> placeholder=<span>"Paste JSON IMPORT text here"</span> tag=textarea class=<span>"wideEdit"</span>  /&gt;
&lt;$button&gt;
   &lt;$vars actionTiddler={{!!dropjsontext}} &gt;
   &lt;$action-setfield dropjsontext=<span>''</span>/&gt;
   &lt;&lt;handleTextPaste&gt;&gt; 
   &lt;<span>/$vars&gt;
{{$:/</span>core/images/copy-clipboard}} Import
&lt;/$button&gt;
```

The json tiddler format for “$:/Import” is well documented in this thread “[How do TWs JSON Formats Look Like](https://talk.tiddlywiki.org/t/how-do-tws-json-formats-look-like/5998)” by pmario. Only minor change is needed in my bookmarklet to create it. Below is a sample of “$:/Import” json tiddler format. If you copy and paste it into the text input box above, and click the \[Import\] button, a new tiddler is (silently) created. No json tiddler text deserializer required.

```
{<span>"tiddlers"</span>:
     {<span>"Illuminate your world"</span>: 
        { <span>"text"</span>:<span>"A sample selection of text from a web site"</span>,
          <span>"type"</span>:<span>"text/vnd.tiddlywiki"</span>,
          <span>"title"</span>:<span>"Illuminate your world"</span>,
          <span>"url"</span>:<span>"https://thinking-about-things.com/"</span>}}}
```

**JSON TIDDLER DROPPABLE ZONE**  
I tried to do the same with Droppable widget. The Droppable zone below uses the same handleTextPaste() actions as the text input box above. If you DRAG the json text above (or a text file containing the json text) into this Droppable zone, the tiddler will also be created (silently). However, I can’t find a way to paste the json text from the clipboard into the Droppable zone using CTRL-V.

```
&lt;$droppable actions=&lt;&lt;handleTextPaste&gt;&gt;&gt;

&lt;$button style=<span>"width:10em;height:10em;"</span>&gt;Droppable zone - Drag your JSON IMPORT text/file here&lt;<span>/$button&gt;

&lt;/</span>$droppable&gt;
```

**BOOKMARKLET EXAMPLES FOR JSON TIDDLER INPUT BOX AND FDIR@VIEWER APPLICATION**  
The json text input box plus the example bookmarklets are packaged in this json file [json tiddler input box.json](https://talk.tiddlywiki.org/uploads/short-url/saK5QvWswUBEpESgNy3JJOQjPV2.json) (22.3 KB).

The bookmarklets in this case output the contents in the “$:/Import” json format that is expected by the text input box. Included also is a “fdir@viewer” tiddler to navigate and inspect imported tiddlers. This application started life as a basic $list to check the contents of tiddlers imported thru the bookmarklets, and sort of grew into a pseudo folder-based navigator and viewer. It shows a navigable folder view of imported tiddlers in the top half and the content of selected tiddler in the bottom half.  

*Screenshot of fdir@viewer showing list of files and directories captured from the browser directory view*

You can explore the sample bookmarklets using fdir@viewer as well.

**SUMMARY**  
In retrospect, I prefer the text input box approach to the json tiddler dropzone:

-   Dropzone doesn’t have the “actions” option for further processing. It does provides an import preview which I do not need for my purpose but I understand can be tapped for some intermediate processing by modifying the import view template to add some button actions.
    
-   The text input box approach doesn’t invoke import preview. Note that the import using tm-perform-import will overwrite existing tiddlers with the same name. I can’t find an option to disable overwrite.
    
-   The text input box approach has the flexibility to process the json tiddler text further before sending “tm-perform-import” to import the tiddlers. An example is in “fdir@viewer” application, the input box processing extracts info from the json tiddler text to update the $:/Import tiddler before importing, so that the $:/Import tiddler can be re-purposed as a import cum directory tiddler by fdir@viewer.
    
-   It would be best if the droppable zone can support CTRL-V pasting via the clipboard. It’s a pleasant surprise to me that the text input box with an Import button works equally well, and a json tiddler text deserializer is not needed after all.
> 