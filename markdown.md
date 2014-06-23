# Raspberry Pi Learning Markdown Guide

Markdown Guide for Raspberry Pi Learning Resources

## What is Markdown?

Markdown is a plain-text formatting syntax. It's very simple, and it maintains its readability while offering a range of formatting options.

See the [Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) on GitHub for reference.

An example Markdown file might look like this:

```
# Title

Intro paragraph goes here

Here is a list of things:

- Raspberry Pi
- USB mouse
- USB keyboard
- Power supply

Here is some more text
```

which would render like so:

># Title
>
>Intro paragraph goes here
>
>Here is a list of things:
>
>- Raspberry Pi
>- USB mouse
>- USB keyboard
>- Power supply
>
>Here is some more text

### Why Markdown?

Markdown is easy to write, there's not much to learn to get going, and you get an instant visual representation of simply formatted works.

As stated in the [Markdown project's philosophy](http://daringfireball.net/projects/markdown/syntax#philosophy):

> Markdown is intended to be as easy-to-read and easy-to-write as is feasible.
>
> Readability, however, is emphasized above all else. A Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions.

Using Markdown in a repository on GitHub allows changes to be managed as the contents evolve. Every revision can be returned to at any point, and it is easy to view a visual difference between any two revisions.

## Markdown basics

### Headings

Headings are denoted by the hash symbol. There are six level headings, which are hierarchical:

```
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6
```

### Emphasis

Emphasis (italics) uses `*asterisks*`:

*asterisks*

Strong emphasis (bold) uses `**double asterisks**`:

**double asterisks**

Use both together (bold italic) with `***triple asterisks***` or combined `***bold italic* and just bold**`.

***triple asterisks***

or

***bold italic* and just bold**

Strikethrough uses two tildes `~~like so~~`:

~~like so~~

### Lists

#### Unordered lists (bullets)

Unordered lists simply use a hyphen at the start of each line like so:

```
- Python
- Scratch
- Sonic Pi
- Minecraft
```

which renders like so:

- Python
- Scratch
- Sonic Pi
- Minecraft

#### Ordered lists (numbered)

Ordered lists simply use a number and a dot at the start of each line like so:

```
1. Python
2. Scratch
3. Sonic Pi
4. Minecraft
```

which renders like so:

1. Python
2. Scratch
3. Sonic Pi
4. Minecraft

You can also just repeat `1.` at the beginning of each line, and the numbers will be automatically generated as you add more. This is especially useful for adding items in the middle of a list, as it saves you renumbering the items:

```
1. Python
1. Scratch
1. Sonic Pi
1. Minecraft
```

1. Python
1. Scratch
1. Sonic Pi
1. Minecraft

#### Nested lists

You can nest items in ordered or unordered lists, or even combine the two, by indenting to create a sub-list like so:

```
- Hardware
    1. Raspberry Pi
    1. Camera module
- Software
    1. Python Picamera
    1. FFMPEG
```

- Hardware
    1. Raspberry Pi
    1. Camera module
- Software
    1. Python Picamera
    1. FFMPEG

Sub-lists continue with further indentation.

#### Paragraphs in between list items

If you need to include further text in between list items, indent the text with four spaces. This will allow your list to continue, so that numbering in an ordered list will not break sequence. For example:

```
1. Plug in your mouse and keyboard

    These go in the USB ports along the short side of the Raspberry Pi opposite the SD card slot

1. Connect your HDMI cable

    This goes in the HDMI port on the long side of the Raspberry Pi
```

1. Plug in your mouse and keyboard

    These go in the USB ports along the short side of the Raspberry Pi opposite the SD card slot

1. Connect your HDMI cable

    This goes in the HDMI port on the long side of the Raspberry Pi


### Links

Links are created by giving the link text in square brackets, immediately followed by round brackets containing the link URL:

```
Check out the [Raspberry Pi](http://www.raspberrypi.org/) website
```

Check out the [Raspberry Pi](http://www.raspberrypi.org/) website

You can also link to other pages in the same repository:

```
See the [worksheet](worksheet.md) for this project
```

See the [worksheet](worksheet.md) for this project

This would link to the `worksheet.md` file in the same folder as the current document. To go into another folder use the following format:

```
See the [Lesson 1 worksheet](lesson-1/worksheet.md)
```

See the [Lesson 1 worksheet](lesson-1/worksheet.md)

This would link to the `worksheet.md` file in the `lesson-1` folder, provided the folder is at the same level as the current document.

To go back up a level, use relative links:

```
See the [project requirements](../requirements.md)
```

See the [project requirements](../requirements.md)

`../` denotes going back up one level. To go back up two levels:

```
See the [project requirements](../../requirements.md)
```

### Images

To include an image in a Markdown document, use the link syntax with a leading exclamation mark. Write a brief description of the image in the square brackets.

```
![Raspberry Pi logo](http://www.raspberrypi.org/wp-content/uploads/2011/10/Raspi-PGB001-150x150.png)
```

![Raspberry Pi logo](http://www.raspberrypi.org/wp-content/uploads/2011/10/Raspi-PGB001-150x150.png)

You can also include images inside the repository; this is a good idea as they're then self-contained. You can refer to them relatively:

```
![Raspberry Pi logo](raspberrypi.png)
```

or in another folder:

```
![Raspberry Pi logo](../images/raspberrypi.png)
```

#### Images as links

You can make an image into a link by wrapping it in square brackets as per the normal link syntax:

```
[![Raspberry Pi logo](raspberrypi.png)](http://www.raspberrypi.org/)
```

### Code blocks

Code blocks are used to show snippets of code in the context of some surrounding text.

Code blocks are denoted by three back-ticks on separate lines either side, like so:

<pre lang="no-highlight"><code>```
for i in range(10):
    print(i)
```</code></pre>

```
for i in range(10):
    print(i)
```

Optionally, you can provide the language of the code used in the block, for syntax highlighting:

<pre lang="no-highlight"><code>```python
for i in range(10):
    print(i)
```</code></pre>

```python
for i in range(10):
    print(i)
```

#### Inline code blocks

You can refer to code or technical keywords inline (i.e. in a sentence) with single back-ticks:

```
Install the package `python-picamera` to access the camera directly from Python.
```

Install the package `python-picamera` to access the camera directly from Python.

No syntax highlighting is available for inline code blocks.

### Block quotes

You can format text as a block quote by beginning each line with a `>` like so:

```
>The Raspberry Picademy is a free professional development experience for primary and secondary teachers, initially for those here in the UK.
```

>The Raspberry Picademy is a free professional development experience for primary and secondary teachers, initially for those here in the UK.

This is useful for quoting text from a web page, book, or documentation.

It is good practice to cite the quote, simply with a link back to the origin if it is online, or another suitable reference:

```
>This package provides a pure Python interface to the Raspberry Pi camera module for Python 2.7 (or above) and Python 3.2 (or above).
>
>~ [Python Picamera Documentation](http://picamera.readthedocs.org/en/release-1.5/index.html) by [Dave Jones](https://github.com/waveform80)
```

>This package provides a pure Python interface to the Raspberry Pi camera module for Python 2.7 (or above) and Python 3.2 (or above).
>
>~ [Python Picamera Documentation](http://picamera.readthedocs.org/en/release-1.5/index.html) by [Dave Jones](https://github.com/waveform80)

### Tables

It is possible to tabulate data in Markdown with the use of pipes (`|`) to denote columns:

```
| Workshop   | Language  | Leader      |
| ---------- |:---------:| -----------:|
| Sonic Pi   | Ruby      | Carrie Anne |
| Picamera   | Python    | Ben         |
| Minecraft  | Python    | Craig       |
```

| Workshop   | Language  | Leader      |
| ---------- |:---------:| -----------:|
| Sonic Pi   | Ruby      | Carrie Anne |
| Picamera   | Python    | Ben         |
| Minecraft  | Python    | Craig       |

Note the use of colons to align columns.

Use of pipes at the edges and alignment of columns is not necessary for the output, but it aids readability in the Markdown:

```
A | B | C
:-: | :-: | :-:
*italic* | `code` | **bold**
1 | 2 | 3
```

A | B | C
:-: | :-: | :-:
*italic* | `code` | **bold**
1 | 2 | 3

Note the use of Markdown inside tables.

### Horizontal rule

Horizontal rules can be used by inserting a line with three or more hyphens like so:

```
---
```

---

### Line breaks

Paragraphs are formed by the presence of blank lines around text, and many other formatting styles in Markdown are affected by line breaks.

```
This is a single sentence followed by a blank line

This is another sentence followed by a blank line

This is three lines
without a gap
between each line
```

This is a single sentence followed by a blank line

This is another sentence followed by a blank line

This is three lines
without a gap
between each line

If you want a paragraph, use new lines on either side of your text.

If something doesn't quite look right in the preview window, try adding or removing new lines around it to achieve the desired formatting.

<a name="anchors"></a>
### Anchors

If you require anchors to point at a particular section of a page, use an empty HTML `<a>` element with a `name` attribute as reference, usually above a heading:

```
<a name="raspberrypi"></a>
## Raspberry Pi
```

This will allow you to refer to that section of the page by appending `#raspberrypi` to the URL.

You can create a link to an anchor on the same page by referencing the hash link:

```
[Raspberry Pi](#raspberrypi)
```

or on another page with the relative or full URL:

```
[Raspberry Pi](../#raspberrypi)
[Anchors](https://github.com/raspberrypilearning/creating-resources/markdown-guide.md#anchors)
```

---

*Based on [adam-p](https://github.com/adam-p)'s [Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)*

## Markdown editors

If you're using git on your computer rather than the GitHub editor, you can use a simple text editor. However, it can be useful to use a desktop Markdown editor with a preview pane. Here is a selection:

- [ReText](https://launchpad.net/retext) for Linux (`apt-get install retext`)
- [Mou](http://mouapp.com/) for Mac
- [MarkdownPad](http://markdownpad.com/) for Windows
- [StackEdit](https://stackedit.io/) - an online editor
