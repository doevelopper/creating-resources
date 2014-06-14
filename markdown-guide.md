# Raspberry Pi Learning Markdown Guide

Markdown Style Guide for Raspberry Pi Learning Resources

## What is Markdown?

Markdown is a plain text formatting syntax. It's very simple, and it maintains its readability while offering a range of formatting options.

See the Markdown cheat sheet on GitHub for reference.

An example markdown file might look like this:

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

Markdown is easy to write, there's not much to learn to get going, and you get instant visual representation of simple formatted works.

Using markdown in a repository on GitHub allows changes to be managed as the contents evolve. Every revision can be returned to at any point, and it is easy to view a visual difference between any two revisions.

Multiple collaborators can work on the same piece of work, and changes by contributors can be managed by the author or owners of the repository.

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

>*asterisks*

Strong emphasis (bold) uses `**double asterisks**`:

>**double asterisks**

Use both together (bold italic) with `***triple asterisks***` or combined `***bold italic* and just bold**`

>***triple asterisks***

or

>***bold italic* and just bold**

Strikethrough uses two tildes `~~like so~~`:

>~~like so~~

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

>- Python
>- Scratch
>- Sonic Pi
>- Minecraft

#### Ordered lists (numbered)

Ordered lists simply use a number and a dot at the start of each line like so:

```
1. Python
2. Scratch
3. Sonic Pi
4. Minecraft
```

which renders like so:

>1. Python
>2. Scratch
>3. Sonic Pi
>4. Minecraft

You can also just repeat `1.` at the beginning of each line, and the numbers will be automatically generated as you add more. This is especially useful for adding items in the middle of a list as it saves you renumbering the items:

```
1. Python
1. Scratch
1. Sonic Pi
1. Minecraft
```

>1. Python
>1. Scratch
>1. Sonic Pi
>1. Minecraft

### Nested lists

You can nest items in ordered or unordered lists (even combine the two) by indenting to create a sub-list like so:

```
- Hardware
    1. Raspberry Pi
    1. Camera module
- Software
    1. Python Picamera
    1. FFMPEG
```

>- Hardware
>    1. Raspberry Pi
>    1. Camera module
>- Software
>    1. Python Picamera
>    1. FFMPEG

Sub-lists continue with further indentation.

### Links

Links are created by giving the link text in square brackets immediately followed by round brackets containing the link URL:

```
Check out the [Raspberry Pi](http://www.raspberrypi.org/) website
```

>Check out the [Raspberry Pi](http://www.raspberrypi.org/) website

You can also link to other pages in the same repository:

```
See the [worksheet](worksheet.md) for this project
```

>See the [worksheet](worksheet.md) for this project

This would link to the `worksheet.md` file in the same folder as the current document. To go in to another folder:

```
See the [Lesson 1 worksheet](lesson-1/worksheet.md)
```

>See the [Lesson 1 worksheet](lesson-1/worksheet.md)

This would link to the `worksheet.md` file in the `lesson-1` folder, provided the folder is at the same level as the current document.

To go back up a level, use relative links:

```
See the [project requirements](../requirements.md)
```

>See the [project requirements](../requirements.md)

`../` denotes going back up one level. To go back up two levels:

```
See the [project requirements](../../requirements.md)
```

### Images

To include an image in a markdown document, use the link syntax with a leading exclamation mark and leave the square brackets empty:

```
![](http://www.raspberrypi.org/wp-content/uploads/2011/10/Raspi-PGB001-150x150.png)
```

> ![](http://www.raspberrypi.org/wp-content/uploads/2011/10/Raspi-PGB001-150x150.png)

You can also include images inside the repository (a good idea as they're then self-contained) so you refer to them relatively:

```
![](raspberrypi.png)
```

or in another folder:

```
![](../images/raspberrypi.png)
```

#### Images as links

You can make an image a link by wrapping it in square brackets as per the normal link syntax:

```
[![](raspberrypi.png)](http://www.raspberrypi.org/)
```

### Code blocks

### Block quotes

### Tables

### Horizontal rule

### Line breaks