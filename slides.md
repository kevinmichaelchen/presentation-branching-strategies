---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/842ofHC6MaI/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS
css: unocss
---

# Git branching strategies

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/kevinmichaelchen/presentation-branching-strategies" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# What is a Git branch?

- 🖖 Branches allow developers to **diverge** from the main branch by creating
separate branches to isolate code changes
- 👉 A branch is essentially a reference or a **pointer** to the latest commit in
a given context; it’s not a container for commits.
- 🪶 The Git branching model is **lightweight** compared to other version control systems.
- ⛓️ Branches allow for **independent** lines of code that branch off the master branch, allowing developers to work independently before merging their changes back to the code base.

<br>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# What is a Git branching strategy?

Branching strategies help to

- 🧠 Enhance productivity by ensuring proper **coordination among developers**
- ⛓️ Enable **parallel development**
- 🏗️ Help organize a series of **planned, structured releases**
- 🛣️ Map a clear **path** when making changes to software through to production
- 🐛 Maintain a **bug-free** code where developers can quickly fix issues and get these changes back to production without disrupting the development workflow

<br>
<br>

Read more about [branching strategies](https://www.flagship.io/git-branching-strategies/)

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: image-right
image: https://www.flagship.io/wp-content/uploads/gitflow-branching-strategy.png
---

# GitFlow

Created by Vincent Driessen:[^1]

<v-click>

There are 2 immortal branches:

</v-click>

<v-clicks>

- `master` branch is always production-ready.
- `develop` always has the latest delivered dev changes.

</v-clicks>

<v-click>

There are 3 types of supporting branches:

</v-click>

<v-clicks>

- **feature** — both branched off and merged back into `develop`; typically only exist on localhost, not in the remote.
- **hotfixes** — branched off `master` and merged back into both `developer` and `master`
- **releases** — branched off `develop` and merged back into both `developer` and `master`

</v-clicks>

<div v-click>

When `develop` basically resembles a new release, that's when the release branch
is created.
</div>

<br>
<br>

[^1]: [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/)

<style>
p {
  @apply text-sm;
}
li {
  @apply text-xs;
}
</style>

---

# Downsides of GitFlow

<div grid="~ cols-2 gap-4">
<div>

A note from Gitflow's creator: 
<blockquote class="mx-auto w-5/6">
Web apps are typically continuously delivered, not rolled back, and you don't 
have to support multiple versions of the software running in the wild...

If your team is doing continuous delivery of software, I would suggest to adopt 
a much simpler workflow (like GitHub flow) instead of trying to shoehorn git-flow
into your team...

If, however, you are building software that is explicitly versioned, or if you 
need to support multiple versions of your software in the wild, then git-flow 
may still be as good of a fit to your team as it has been to people in the last
10 years.
</blockquote>



</div>
<div class="mb-[-100px]">

<Tweet id="1573001023064789000" scale="0.65" />

</div>
</div>

<style>
.footnotes-sep {
  @apply mt-20 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

---
layout: center
class: text-center
---

# Learn More about SlideV

[Documentations](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/showcases.html)
