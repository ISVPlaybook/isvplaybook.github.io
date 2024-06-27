# ISV Playbook on GitHub Pages

This repository contains the source code for the ISV Playbook on GitHub Pages. 

The ISV Playbook is designed to help the Microsoft ISV partners navigate the Microsoft Partner Network and leverage the resources available to build, go-to-market, and sell with Microsoft. The playbook provides guidance on the Microsoft Partner Network, programs, resources, and tools available to the ISV partners.

The repository is built using Just the Docs theme powered by [Jekyll](https://jekyllrb.com/) and hosted on GitHub Pages.

Following is the guidance to help you contribute to the ISV Playbook:

Note: Some of the features mentioned below are specific to the Just the Docs theme and may not render on this page itself. However, they will be generated as expected for the GitHub Pages content. For more information on the features supported by the theme, refer to the [Just the Docs documentation](https://pmarsceill.github.io/just-the-docs/).

## Page organization and navigation:

- The ISV Playbook is organized into sections and articles. Each section is a folder in the `_docs` directory and each article is a markdown file in the respective section folder.
- The navigation is automatically generated based on the folder structure and the front matter of the markdown files.
- To add a new section, create a new folder in the `_docs` directory and add a markdown file with the same name as the folder.
- To add a new article, create a new markdown file in the respective section folder.
- To change the order of sections or articles, update the `nav_order` in the front matter of the markdown file.

## Front matter:

The front matter for ISV Playbook markdown files is used to define the layout, title, navigation order, parent, and permalink of the pages. An example is as follows:

```markdown
---
layout: default
title: Article Title (shows up in the navigation)
nav_order: 1 (order of the page in the navigation)
parent: Parent Section (required for child pages)
permalink: /docs/parentsection/short-page-name/
---

# Article Title (this is the title of the page)
{: .no_toc } - This excludes the article title from the table of contents.

Add a description of the article here in a few lines.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc} - These lines automatically generate a table of contents based on the headings in the markdown file.

---

The article content follows from here.

```

Some more guidance on the front matter:
- Each markdown file should have front matter at the beginning of the file. The front matter is used to define the layout, title, navigation order, parent, and permalink of the page.
- The front matter should be enclosed in `---` at the beginning and end of the front matter.
- The front matter should have the following fields:
    - layout: default
    - title: Title of the page
    - nav_order: Order of the page in the navigation
    - parent: Parent section of the page
    - permalink: Permalink of the page
- Example front matter:
    ```
    ---
    layout: default
    title: Article 1
    nav_order: 1
    has_children: true
    parent: Section 1
    permalink: /docs/section-1/article-1
    ---
    ```
- The `permalink` field is optional. If not provided, the permalink is generated based on the folder structure and the file name.
- The `has_children` field is used to indicate if the page has child pages. If set to true, the page will be displayed as a section in the navigation with a dropdown menu of child pages.
- The `parent` and `has_children` field are mutually exclusive. If `parent` is provided, `has_children` should not be provided.

Example for a section with child pages:
```markdown
---
layout: default
title: Partner Programs
nav_order: 3
has_children: true
permalink: /docs/partner-programs
---
```

Example for an article with a parent section:
```markdown
---
layout: default
title: Article 1
nav_order: 1
parent: Partner Programs
permalink: /docs/partner-program/article-1
---
```

The combination of above front matter will result in the following navigation structure:
- Partner Programs
    - Article 1

Note: Absence of front matter will result in the HTML page not being generated during the build.

## Code snippets:

- To add a code snippet to a markdown file, enclose the code in triple backticks.
- To add a code snippet with syntax highlighting, add the language identifier after the first set of triple backticks.
- Example code snippet:

```
    ```
    your code here
    ```
```

To add a code snippet with syntax highlighting, please add the programming language identifier after the first set of triple backticks. For example, to add a code snippet in Python, use the following syntax:
```markdown
```python
```
```python
    ```
    print("Hello, World!")
    ```
```

## Callouts

Callouts can be used to highlight important information. This theme supports various type of callouts including note, warning, tip, and important.

Untitled callout:
```markdown
{: .highlight }
A paragraph
```

Note callout:
```markdown
{: .note }
A note
```

Warning callout:
```markdown
{: .warning }
A warning
```

Tip callout:
```markdown
{: .tip }
A tip
```

Important callout:
```markdown
{: .important }
Important information
```

## Buttons:

To add a button to a page, use the following syntax:
    ```
    [Link button](https://isvplaybook.github.io/){: .btn }
    ```

## Headings

Headings can be added using the following syntax:

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>

## Inline elements


```
Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](https://isvplaybook.github.io/isvplaybook/).

```

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](https://isvplaybook.github.io/isvplaybook/).


## Lists

Add unordered list by adding line with a * or - at the start of the line.

```
- Item 1
- Item 2
- Item 3
```

- Item 1
- Item 2
- Item 3

To add ordered list, add line with a number at the start of the line.

```
1. Item 1
2. Item 2
3. Item 3
```

1. Item 1
2. Item 2
3. Item 3

Please note that the numbers in your markdown file do not need to be in order. The list will be automatically numbered in the rendered page.

To add a task list in a tutorial, use the following syntax:

```markdown
- [x] Task 1
- [ ] Task 2
- [ ] Task 3
```

- [x] Task 1
- [ ] Task 2
- [ ] Task 3

## Blockquotes

To add a blockquote, use the following syntax:

```markdown
> This is a blockquote.
```

> This is a blockquote.

## Tables

To add a table, use the following syntax:

```markdown
| Header 1 | Header 2 |
| -------- | -------- |
| Row 1, Col 1 | Row 1, Col 2 |
| Row 2, Col 1 | Row 2, Col 2 |
```

| Header 1 | Header 2 |
| -------- | -------- |
| Row 1, Col 1 | Row 1, Col 2 |
| Row 2, Col 1 | Row 2, Col 2 |

## Images

To add an image, use the following syntax:

```markdown
![Image description](/path/to/image.jpg)
```

### Collapsed Section

The following uses the [`<details>`](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-collapsed-sections) tag to create a collapsed section.

```
<details markdown="block">
<summary>Shopping list (click me!)</summary>

This is content inside a `<details>` dropdown.

- [ ] Apples
- [ ] Oranges
- [ ] Milk

</details>
```

<details markdown="block">
<summary>Shopping list (click me!)</summary>

This is content inside a `<details>` dropdown.

- [ ] Apples
- [ ] Oranges
- [ ] Milk

</details>
