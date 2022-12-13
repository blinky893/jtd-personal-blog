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

The default layout of `index.md` files is a **table of contents** - or TOC - that lists all the child pages in the section. This TOC is generated automatically. The only information you need to add to the file is the front matter and (optionally) an H1 heading to help keep the reader orientated:
```
---
layout: default
title: Using this template

# nav_order sets the position of the section in the main navigation 
nav_order: 2

# has_children should be set to **true** so child pages appear inside the section.
has_children: true 
---
# Heading 1

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
