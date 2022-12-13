---
layout: default
title: Quick tips
parent: Using this template
nav_order: 1
---

# Quick tips
{: .no_toc}

This page is a cheat sheet and style guide for creating content on this template.
{: .fs-6 .fw-300 }  
  

{: .information-title }
> Information
>
> It does not replace the [official documentation](https://just-the-docs.github.io/just-the-docs/).  
  

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Subtitles
The wrapper that creates the sub-heading style seen at the top of this page `{: .fs-6 .fw-300 }` goes at the end of the paragraph on a new line. It is **Font Size 6** and **Font Weight 300**. It makes for a light and large introductory sentence beneath the H1.
 
## Callouts (Note boxes)

 The **Information** callout at the top of this page uses the code.

  ```md
 {: . information-title }
> Information
>
> It does not replace the [official documentation](https://just-the-docs.github.io/just-the-docs/).  
```

{: .warning-title }
> Warning
>
> Warning is red.

{: .information-title }
> Information
>
> Information is blue. 

{: .note-title }
> Note
>
> Notes are purple.

{: .tip-title }
> Tip
>
> Tips are green. 

## Creating new sections

### Creating a new section
You create a new section by creating a **new folder** inside `./docs` and adding an `index.md` file. The name of the folder is not displayed in the public site so can be whatever you want.  

The **section name** in the main nav is from the the `index.md` file > front matter > **page title**.  

The `index.md` files are designed just to have an H1 heading and then a table of contents. The content for these pages is just the front matter plus an H1 heading:

```
---
layout: default
title: Using this template
nav_order: 2 [or whatever position you want it to be in the main nav]
has_children: true [because you're expecting to add other pages to the folder which will be referenced in the TOC.]
---
# Section name

```

---

### Creating pages within a section
Pages within a section (child pages) need to include in their front matter: 

1. the **title** of their parent page and 
2. their **nav_order** for the section

```
---
layout: default
title: Quick tips
parent: Using this template
nav_order: 1 [or whatever position you want it to be in the section nav]
---

```

---
ENDS
---
