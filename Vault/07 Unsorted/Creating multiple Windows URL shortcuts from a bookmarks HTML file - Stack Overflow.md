---
created: 2025-02-05
source: https://stackoverflow.com/questions/12043989/creating-multiple-windows-url-shortcuts-from-a-bookmarks-html-file
banner: https://cdn.sstatic.net/Sites/stackoverflow/Img/apple-touch-icon@2.png?v=73d79a89bded
tags:
  - clippings
---

![Banner](https://cdn.sstatic.net/Sites/stackoverflow/Img/apple-touch-icon@2.png?v=73d79a89bded)

***
Hmm, in combination with a tool like everything that would be usefull, only you will need to do the operation regularly. I suppose it must be possible to get your source right from chrome, anyway here is a script that does what you ask for.

```
<span class="hljs-keyword">Const</span> ForReading = <span class="hljs-number">1</span>, ForWriting = <span class="hljs-number">2</span>, ForAppending = <span class="hljs-number">8</span>, CreateIfNeeded = <span class="hljs-literal">true</span>
outpath = <span class="hljs-string">"g:\script\shortcut\url2\"</span>
<span class="hljs-keyword">Set</span> objFSO = CreateObject(<span class="hljs-string">"Scripting.FileSystemObject"</span>)
bookmarkfile = <span class="hljs-string">"bookmarks.html"</span>
<span class="hljs-keyword">Set</span> bookmarks = objFSO.OpenTextFile(bookmarkfile, ForReading)
<span class="hljs-keyword">Set</span> regEx = <span class="hljs-built_in">New</span> RegExp
regEx.<span class="hljs-keyword">Global</span> = <span class="hljs-literal">True</span>
<span class="hljs-keyword">Set</span> regEx2 = <span class="hljs-built_in">New</span> RegExp
regEx2.<span class="hljs-keyword">Global</span> = <span class="hljs-literal">True</span>
regEx2.Pattern = <span class="hljs-string">"[^a-zA-Z0-9-_.]"</span>

regEx.Pattern = <span class="hljs-string">"&lt;DT&gt;&lt;A HREF=""(.*)"" ADD_DATE.*&gt;(.*)&lt;/A&gt;"</span>
<span class="hljs-keyword">do</span> <span class="hljs-keyword">until</span> bookmarks.AtEndOfStream
  line = bookmarks.readline()
  <span class="hljs-keyword">if</span> regEx.test(line) <span class="hljs-keyword">then</span>
    shortcut = regEx.Replace(line,<span class="hljs-string">"$1"</span>)
    filename = trim(regEx.Replace(line,<span class="hljs-string">"$2"</span>))
    filename = Regex2.Replace(filename, <span class="hljs-string">"_"</span>)
    filename = outpath &amp; left(filename, <span class="hljs-number">80</span>) &amp; <span class="hljs-string">".url"</span>
    wscript.echo filename
    <span class="hljs-comment">'the following skips invalid filenames, you should add a routine to filter out invalid filename characters in your codeset</span>
    <span class="hljs-keyword">on</span> <span class="hljs-keyword">error</span> <span class="hljs-keyword">resume</span> <span class="hljs-keyword">next</span>
    <span class="hljs-keyword">Set</span> objFile = objFSO.OpenTextFile(filename, ForWriting, CreateIfNeeded)
    <span class="hljs-keyword">if</span> err.number &lt;&gt; <span class="hljs-number">0</span> <span class="hljs-keyword">then</span>
      wscript.echo err.description
    <span class="hljs-keyword">end</span> <span class="hljs-keyword">if</span>
    objFile.write <span class="hljs-string">"[InternetShortcut]"</span> &amp; vbcrlf &amp; <span class="hljs-string">"URL="</span> &amp; shortcut
    objFile.close
  <span class="hljs-keyword">end</span> <span class="hljs-keyword">if</span>
<span class="hljs-keyword">loop</span>
```
