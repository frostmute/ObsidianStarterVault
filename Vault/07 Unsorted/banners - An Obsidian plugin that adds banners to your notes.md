---
source: https://github.com/noatpad/obsidian-banners/issues/141
created: 2024-05-16T22:56:48 (UTC -05:00)
banner_y: 0.25582
category:
  - "[[../00 - CATEGORIES/Clippings]]"
---
# noatpad/obsidian-banners: An Obsidian plugin that adds banners to your notes

---
<table class="d-block user-select-contain" data-paste-markdown-skip=""><tbody class="d-block"><tr class="d-block"><td class="d-block comment-body markdown-body  js-comment-body"><p dir="auto">As a workaround, I added a CSS snippet to the Appearance Settings:</p><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code class="notranslate">.obsidian-banner-wrapper {
    margin-top: calc(var(--banner-height) - 200px);
    padding-top: 0.5em;
}
</code></pre><div class="zeroclipboard-container position-absolute right-0 top-0"></div></div><p dir="auto">It works fine on Mac OS but doesn't make any difference on iOS.</p></td></tr></tbody></table>

<table class="d-block user-select-contain" data-paste-markdown-skip=""><tbody class="d-block"><tr class="d-block"><td class="d-block comment-body markdown-body  js-comment-body"><p dir="auto">Not sure why it took me so long, but, adding !important to the snippet got the work around sorted for iOS:</p><div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code class="notranslate">.obsidian-banner-wrapper {
    margin-top: calc(var(--banner-height) - 200px) !important;
    padding-top: 0.5em;
}
</code></pre><div class="zeroclipboard-container position-absolute right-0 top-0"></div></div><p dir="auto">Of course, this is only a workaround, and you'll need to adjust for the height you have your banner set.</p></td></tr></tbody></table>

I've written the following CSS snippet workaround

```css
.obsidian-banner-wrapper {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: var(--banner-height);
    margin-top: 0;
    padding-top: 0;
}

.obsidian-banner{
    position: relative;
}

.markdown-preview-view:has(.obsidian-banner-wrapper) {
    padding-top: calc(var(--banner-height) + var(--file-margins));
}
```

<table class="d-block user-select-contain" data-paste-markdown-skip=""><tbody class="d-block"><tr class="d-block"><td class="d-block comment-body markdown-body  js-comment-body"><p dir="auto">My simple fix (it works best for me in preview and in embed)</p><div class="highlight highlight-source-css notranslate position-relative overflow-auto" dir="auto"><pre class="notranslate">.<span class="pl-c1">obsidian-banner-wrapper</span> {
  <span class="pl-c1">margin-top</span><span class="pl-kos">:</span> <span class="pl-c1">0</span>;
}</pre></div></td></tr></tbody></table>
> 