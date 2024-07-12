# Corporate theme for Marp
[Marp](https://marp.app) allows you to build slideshows from Markdown code. This repo brings a simple and clean theme to your professional and school presentations.

Take a look at the [slideshow example](./doc/slideshow.pdf) using this theme.

![](./doc/screenshots/first.png)

## Installation
Download the [stylesheet](corporate.css).

### VSCode
Install the [Marp extension](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode).

Go to Settings > Search _markdown.marp.theme_ > Add Item > Set the path to the theme stylesheet you downloaded.

Go to Settings > Search _markdown.marp.enable-html_ > Check the box to enable HTML and access extra features.

In your markdown file header:
```md
---
marp: true
theme: corporate
---

# Title 1
```

### Marp CLI
See the [documentation](https://marpit.marp.app/usage?id=apply-theme).


## Usage
Marp's markdown directives are listed in their [documentation](https://marpit.marp.app/markdown).

For a full list of Markdown directives, see the [specifications](https://spec.commonmark.org/current/).

You can find a example slideshow's code [here](./doc/slideshow.md).

Some theme's features are available with the following directives:
- `# h1`
- `## h2`
- ```md
  - left column
  - right column
  ```

### Specific slides style
Special slide layouts can be enabled using classes:
```md
---

<!-- _class: <class-name> -->

# Your slide title
```

Here are some of them:
- `first` slide of your presentation, with right sided image and company logo, title, subtitle, date, author
  ```md
  <!-- _class: first -->

  # Title
  ### Subtitle for this n<sup>th</sup> presentation

  ![bg right:40%](./assets/background.jpg)

  _28/06/2024_
  ```

- `toc` for _Table Of Content_, which pimps up an [ordered list](https://spec.commonmark.org/0.31.2/#ordered-list-marker)
  ```md
  <!-- _class: toc -->

  # Table of content

  1. Introduction
  2. Part X
  3. Part Y
  ```
- `last` slide of your presentation, with colored background and company logo in the center
  ```md
  <!-- _class: last -->

  ![width:500px](./assets/company-logo.svg)
  ```

### Useful directives
- Disable pagination for a single page:
  ```md
  <!-- _paginate: false -->
  ```
