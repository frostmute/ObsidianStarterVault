---
banner: 
created: 2024-06-14T04:38:46
source: https://www.moritzjung.dev/obsidian-meta-bind-plugin-docs/guides/buttons/
author: 
cssclasses:
  - dashboard
---

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

```cardlink
url: https://www.moritzjung.dev/obsidian-meta-bind-plugin-docs/guides/buttons/
title: "Buttons | Meta Bind Docs"
description: "A tutorial for buttons, a spiritual successor the the buttons plugin."
host: www.moritzjung.dev
image: 
```
Button are well… Buttons, inside your notes. They can be configured to do a variety of things, like opening a file, running a command, or even running a JavaScript file.

# Buttons FAQ
## Creating a button

To create a button, you need to create a code block with the language set to `meta-bind-button`. The inside of the code block belongs the configuration in YAML format for the button.

The following example button displays `Meta Bind Help` and opens the meta bind FAQ page.

```
<div><p><span>```meta-bind-button</span></p></div><div><p><span>style</span><span><span>:</span><span> </span></span><span>primary</span></p></div><div><p><span>label</span><span><span>:</span><span> </span></span><span>Meta Bind Help</span></p></div><div><p><span>action</span><span>:</span></p></div><div><p><span>  </span><span>type</span><span><span>:</span><span> </span></span><span>command</span></p></div><div><p><span>  </span><span>command</span><span><span>:</span><span> </span></span><span>obsidian-meta-bind-plugin:mb-open-faq</span></p></div><div><p><span>```</span></p></div>
```

## Inline Buttons

Inline buttons are buttons that are displayed inline with the text. They are created using inline code blocks starting with `BUTTON`. Inline buttons must reference a button code block defined elsewhere in the **same note** via matching ids.

Buttons declared in the plugin’s settings under `Button Templates` can be referenced by inline buttons in every note.

The following example button inline button references the code block button with the `help-button` id below it. By referencing the button code block, the inline button will have the same configuration as the code block button. The code block button can be hidden by setting the `hidden` YAML property to `true`.

```
<div><p><span>Meta Bind has an in plugin help page. `</span><mark><span>BUTTON[</span><span>help-button</span><span>]</span></mark><span>` Isn't that cool?</span></p></div><div><p><span>```meta-bind-button</span></p></div><div><p><span>style</span><span><span>:</span><span> </span></span><span>primary</span></p></div><div><p><span>label</span><span><span>:</span><span> </span></span><span>Meta Bind Help</span></p></div><div><p><span>id</span><span>:</span><span> </span><span>help-button</span></p></div><div><p><span>action</span><span>:</span></p></div><div><p><span>  </span><span>type</span><span><span>:</span><span> </span></span><span>command</span></p></div><div><p><span>  </span><span>command</span><span><span>:</span><span> </span></span><span>obsidian-meta-bind-plugin:open-faq</span></p></div><div><p><span>```</span></p></div>
```

## Button Groups

Inline buttons can display multiple buttons in a row. For this, multiple button ids separated by commas need to be passed to the `BUTTON` inline code block.

The following example displays a button group of two buttons.

```
<div><p><span>Theme Switcher: `</span><mark><span>BUTTON[</span><span>light-mode</span><span>,</span><span> dark-mode</span><span>]</span></mark><span>`</span></p></div><div><p><span>```meta-bind-button</span></p></div><div><p><span>style</span><span><span>:</span><span> </span></span><span>destructive</span></p></div><div><p><span>label</span><span><span>:</span><span> </span></span><span>Light Mode</span></p></div><div><p><span>id</span><span>:</span><span> </span><span>light-mode</span></p></div><div><p><span>hidden</span><span>:</span><span> </span><span>true</span></p></div><div><p><span>actions</span><span>:</span></p></div><div><p><span><span>  </span></span><span>-</span><span> </span><span>type</span><span><span>:</span><span> </span></span><span>command</span></p></div><div><p><span>    </span><span>command</span><span><span>:</span><span> </span></span><span>theme:use-light</span></p></div><div><p><span>```</span></p></div><div><p><span>```meta-bind-button</span></p></div><div><p><span>style</span><span><span>:</span><span> </span></span><span>primary</span></p></div><div><p><span>label</span><span><span>:</span><span> </span></span><span>Dark Mode</span></p></div><div><p><span>id</span><span>:</span><span> </span><span>dark-mode</span></p></div><div><p><span>hidden</span><span>:</span><span> </span><span>true</span></p></div><div><p><span>actions</span><span>:</span></p></div><div><p><span><span>  </span></span><span>-</span><span> </span><span>type</span><span><span>:</span><span> </span></span><span>command</span></p></div><div><p><span>    </span><span>command</span><span><span>:</span><span> </span></span><span>theme:use-dark</span></p></div><div><p><span>```</span></p></div>
```

## Button Configuration

### Button Properties

The YAML configuration of a button has must follow the following TypeScript interface.

```
<div><p><span>interface</span><span> </span><span>ButtonConfig</span><span> {</span></p></div><div><p><span><span>  </span></span><span>label</span><span>:</span><span> </span><span>string</span><span>; </span><span>// The text displayed on the button</span></p></div><div><p><span><span>  </span></span><span>icon</span><span>?:</span><span> </span><span>string</span><span>; </span><span>// An optional lucide icon to display on the button</span></p></div><div><p><span><span>  </span></span><span>style</span><span>:</span><span> </span><span><span>'</span><span>default</span><span>'</span></span><span> </span><span>|</span><span> </span><span><span>'</span><span>primary</span><span>'</span></span><span> </span><span>|</span><span> </span><span><span>'</span><span>destructive</span><span>'</span></span><span> </span><span>|</span><span> </span><span><span>'</span><span>plain</span><span>'</span></span><span>; </span><span>// The style of the button</span></p></div><div><p><span><span>  </span></span><span>class</span><span>?:</span><span> </span><span>string</span><span>; </span><span>// Optional CSS classes to add to the button. Multiple classes can be separated by spaces</span></p></div><div><p><span><span>  </span></span><span>tooltip</span><span>?:</span><span> </span><span>string</span><span>; </span><span>// Optional tooltip to display when hovering over the button. If not set, the label is used</span></p></div><div><p><span><span>  </span></span><span>id</span><span>?:</span><span> </span><span>string</span><span>; </span><span>// The optional id of the button, used for referencing the button in inline buttons</span></p></div><div><p><span><span>  </span></span><span>hidden</span><span>?:</span><span> </span><span>boolean</span><span>; </span><span>// Whether this button should be hidden, useful when only using the button in inline buttons</span></p></div><div><p><span><span>  </span></span><span>action</span><span>?:</span><span> </span><span>ButtonAction</span><span>; </span><span>// The action to perform when the button is clicked</span></p></div><div><p><span><span>  </span></span><span>actions</span><span>?:</span><span> </span><span>ButtonAction</span><span>[]; </span><span>// Optionally multiple actions can be performed when the button is clicked</span></p></div><div><p><span>}</span></p></div>
```

`action` and `actions` are mutually exclusive, meaning that only one of them can be used.

## Button Actions

Button actions can require multiple properties depending on the type of action, but every action has a `type` property, by which it is identified.

A list of button actions and their required properties can be found in the sidebar under `Reference -> Button Actions`.


# My Buttons

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