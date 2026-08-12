---
title: What is Webpan
---

# What is Webpan?

Webpan is a _blank-canvas_ take on the static site generator: a _blank-canvas_
software is a skeleton program that can be easily extended by installing plugins.
This ensures there are no hard-coded behaviours - that all features are customisable.

## What can Webpan do?

| Use case         | Status                                                                                  |
| ---------------- | --------------------------------------------------------------------------------------- |
| Documentation    | ✅ **_YES!_** There are plugins - this page is generated with Webpan!                     |
| Notes publishing | ✅ **_YES!_** Use the same plugins as documentation, which supports unlimited folder depth. |
| Blog site        | ⏳ **_WIP!_** I am writing plugins for that.                                            |

- Renders everything into HTML and CSS, so **JavaScript is not required** to
  display $\LaTeX$, Mermaid diagrams and syntax highlighting.

  ```mermaid
      gitGraph
         commit
         commit
         branch develop
         commit
         commit
         commit
         checkout main
         commit
         commit
         merge develop
         commit
         commit
  ```
  ```ts
  console.log("syntax highlighting without client side JS");
  ```
- Ability to use multiple plugins at once to maximise chaos.
    ```mermaid
    ---
    config:
      themeVariables:
        treeView:
          labelColor: '#FFFFFF'
          lineColor: '#FFFFFF'
          iconColor: '#FFFFFF'
          descriptionColor: '#FFFFFF'
    ---
    treeView-beta
        "blob-posts/"
            "why-im-really-cool.md"
            "demonstrating-my-coolness.html"
            "demonstrating-my-coolness.css"
            "demonstrating-my-coolness.js"
        "notes/"
            "rust-lang.md"
            "discrete-maths.tex"
            "digital-electronics.typ"
    ```
  > There are currently no plugins supporting `.tex` or `.typ` files, but file
  > format cross-play is entirely doable.
  
## Developer Experience

- **Quick subsequent builds** - remembers the previous build, and only rebuild what's
  changed.
- **Instant preview** - edits reflected in browser without refreshing the page.
- **Reproducible builds** - all plugins are installed as npm packages on the
  project.
  
> #### Human-made notice
> Webpan is human-made, the experience of human programmers are prioritised.
