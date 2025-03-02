---
created: 2025-02-19T01:01:08-06:00
reviewed:
url: "https://help.obsidian.md/web-clipper/variables"
title: "Variables - Obsidian Help"
author:
  - "Obsidian Help"
published:
description: "Variables - Obsidian Help"
---

#webclip/unread

# Variables - Obsidian Help

```yaml
permalink: web-clipper/variables
```

[Web Clipper templates](https://help.obsidian.md/web-clipper/templates) can use variables to automatically pre-populate data from the page in a template. Variables can be used in the **note name**, **note location**, **properties**, and **note content**. Variables can also be modified using [filters](https://help.obsidian.md/web-clipper/filters).

Use the `...` icon in the [Web Clipper](https://help.obsidian.md/web-clipper) extension to access the current page variables for use in templates. There are five types of variables you can use:

- [Preset variables](https://help.obsidian.md/web-clipper/variables#Preset%20variables)
- [Prompt variables](https://help.obsidian.md/web-clipper/variables#Prompt%20variables)
- [Meta variables](https://help.obsidian.md/web-clipper/variables#Meta%20variables)
- [Selector variables](https://help.obsidian.md/web-clipper/variables#Selector%20variables)
- [Schema.org variables](https://help.obsidian.md/web-clipper/variables#Schema.org%20variables)

## Preset variables

Preset variables are automatically generated based on the page content. These typically work for most websites.

The main content variable is `{{content}}`, which contains the article content, or the [highlights](https://help.obsidian.md/web-clipper/highlight), or the selection if there is any selected text on the page. Note that `{{content}}` attempts to extract the main content of the page, which may not always be what you want. In that case, you can use other preset variables or selector variables to extract the content you need.

| Variable | Description |
| --- | --- |
| `{{author}}` | Author of the page |
| `{{content}}` | Article content, [highlights](https://help.obsidian.md/web-clipper/highlight), or selection, in Markdown format |
| `{{contentHtml}}` | Article content, [highlights](https://help.obsidian.md/web-clipper/highlight), or selection, in HTML format |
| `{{date}}` | Current date, can be formatted using the `date` filter |
| `{{description}}` | Description or excerpt |
| `{{domain}}` | Domain |
| `{{favicon}}` | Favicon URL |
| `{{fullHtml}}` | Unprocessed HTML for the full page content |
| `{{highlights}}` | [Highlights](https://help.obsidian.md/web-clipper/highlight) with text and timestamps |
| `{{image}}` | Social share image URL |
| `{{published}}` | Published date, can be formatted using the `date` filter |
| `{{site}}` | Site name or publisher |
| `{{title}}` | Title of the page |
| `{{time}}` | Current date and time |
| `{{url}}` | Current URL |

## Prompt variables

Prompt variables leverage language models to extract and modify data using natural language. Prompt variables require [Interpreter](https://help.obsidian.md/web-clipper/interpreter) to be enabled and configured.

Prompt variables use the syntax `{{"a summary of the page"}}`. The double quotes around the prompt are important and distinguish prompts from preset variables. Prompt responses can be post-processed with [filters](https://help.obsidian.md/web-clipper/filters), e.g. `{{"a summary of the page"|blockquote}}`.

### When to use prompt variables

Prompt variables have the benefit of being extremely flexible and easy to write, however they come with several tradeoffs: they are slower to run, and may have cost and privacy considerations depending on the [provider](https://help.obsidian.md/web-clipper/interpreter#Models) you choose.

Unlike other variable types, prompt variables need to be processed by an external language model, so they are replaced only once [Interpreter](https://help.obsidian.md/web-clipper/interpreter) has run.

It is best to *not* use prompt variables if the data you want to extract is in a consistent format that could be extracted with other variable types.

On the other hand, prompt variables can be useful if the data you want to extract is an *inconsistent* format across websites. For example, you can make a [template](https://help.obsidian.md/web-clipper/templates) to save books that is agnostic of the book site. Prompt variables like `{{"author of the book"}}` will work across any book site, whereas selector variables typically only work for one site.

### Examples

Prompts can use almost any natural language query. Depending on the model you use, prompts can query or translate data across languages.

- `{{"a three bullet point summary, translated to French"}}` to extract bullet points about the page, and translate them to French.
- `{{"un resumé de la page en trois points"}}` to extract three bullet points using a prompt in French.

Prompts can transform page content into JSON that can be manipulated with [filters](https://help.obsidian.md/web-clipper/filters). For example:

```yaml
{{"return a JSON object for each tweet, that includes the author, tweet_text, date in YYYY-MM-DD format, and images array (if there are any)"|map:tweet => ({text: tweet.tweet_text, author: tweet.author, date: tweet.date})|template:"${text}\n— [[@${author}]], [[${date}]]\n"}}
```

## Meta variables

Meta variables allow you to extract data from [meta elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) in the page, including [Open Graph](https://ogp.me/) data used to populate social share previews.

- `{{meta:name}}` returns the content of the meta name tag with the given name, e.g. `{{meta:name:description}}` for the `description` meta tag.
- `{{meta:property}}` returns the content of the meta property tag with the given property, e.g. `{{meta:property:og:title}}` for the `og:title` meta tag.

## Selector variables

Selector variables allow you to extract text content from elements on the page using [CSS selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_selectors/Selectors_and_combinators).

The syntax is `{{selector:cssSelector?attribute}}`, where `?attribute` is optional. If no attribute is specified, the text content of the element is returned. You can also use `{{selectorHtml:cssSelector}}` to get the HTML content of the element. Selector variables tend to work best on a specific website or set of websites that have consistent HTML structure.

- `{{selector:h1}}` returns text content of the first `h1` element on the page.
- `{{selector:.author}}` returns text content of the first `.author` element on the page.
- `{{selector:img.hero?src}}` returns the `src` attribute of the first image with class `hero`.
- `{{selector:a.main-link?href}}` returns the `href` attribute of the first anchor tag with class `main-link`.
- `{{selectorHtml:body|markdown}}` returns the entire HTML of the `body` element, converted to Markdown using the `markdown` [filter](https://help.obsidian.md/web-clipper/filters#HTML%20processing).
- Nested CSS selectors and combinators are supported if you need more specificity.
- If multiple elements match the selector, an array is returned, which you can process with [array and object filters](https://help.obsidian.md/web-clipper/filters#Arrays%20and%20objects) like `join` or `map`.

## Schema.org variables

Schema variables allow you to extract data from [schema.org](https://schema.org/) JSON-LD on the page. Schema.org data can also be used to automatically [trigger a template](https://help.obsidian.md/web-clipper/templates#Schema.org%20matching).

- `{{schema:@Type:key}}` returns the value of the key from the schema.
- `{{schema:@Type:parent.child}}` returns the value of a nested property.
- `{{schema:@Type:arrayKey}}` returns the first item in an array.
- `{{schema:@Type:arrayKey[index].property}}` returns the item at the specified index in an array.
- `{{schema:@Type:arrayKey[*].property}}` returns a specific property from all items in an array.

You can also use a shorthand notation without specifying the schema type:

- `{{schema:author}}` will match the first `author` property found in any schema type.
- `{{schema:name}}` will match the first `name` property found in any schema type.

This shorthand is particularly useful when you don't know or don't care about the specific schema type, but you know the property name you're looking for.

Nested properties and array access work as well, both with and without the schema `@Type` specified:

- `{{schema:author.name}}` will find the first `author` property and then access its `name` sub-property.
- `{{schema:author[0].name}}` will access the `name` of the first author in an array of authors.
- `{{schema:author[*].name}}` will return an array of all author names.