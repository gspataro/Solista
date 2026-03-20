# Solista

A simple, fast, and flexible static site builder powered by [Orchestra](https://github.com/gspataro/Orchestra).

Solista lets you build fully static websites using plain files, without a database, without complexity, just content and structure.

## ✨ Features

- 📄 Write content in Markdown, JSON or plain text
- 🧠 Structured content with schemas
- 🔗 Internal linking system
- 🏞️ Image handling and transformations
- ⚡ Fast builds with caching
- 🧪 Rehearsal mode (no build required)
- 🎨 Theme-based rendering

## 🚀 Getting started

Create a new project:

`composer create-project gspataro/solista my-site`

Move into your project:

`cd my-site`

Build your site:

`./solista build`

Start the development server:

`./solista rehearsal`

Open your browser at:

`http://localhost:8080`

---

## 🧱 Project structure

A typical Solista project looks like this:

- /contents (all your media and contents)
- /public (production-ready website)
- /resources/themes (your themes)
- /blueprint.json (the main configuration file)

You are free to organize your contents as you prefer.

## ✍️ Writing content

Content is written in Markdown with frontmatter:

```markdown
---
title: My first post
published_at: 2026-03-17
categories:
    - news
---

Your content goes here.
```

## 🔗 Internal links

Solista provides a custom protocol to link content safely:

`orchestra://articles/hello-world.md`

`orchestra://blog`

`orchestra://blog.page-2`

Links are automatically resolved to the correct URLs, even if your structure changes.

## 🏞️ Media

Media files live inside `/contents/media`.

You can reference them directly:

```markdown
![Alt Text](/hello-world.jpg?variant=medium "Title Text")
```

Solista can:

- generate image variants
- handle resizing
- provide responsive `srcset`

## 🧪 Rehearsal mode

Rehearsal is a development server that renders pages on demand.

- no build required
- instant feedback
- perfect for content editing and theme development

## ⚡ Performance

Solista is designed to be fast:

- content is cached
- builds are incremental
- theme changes do not invalidate content parsing

## 🎨 Themes

Themes control how your content is rendered.

Solista ships with a minimal default theme intended for learning and experimentation.

> A production-ready theme will be introduced in future releases.

If you change or update your theme, Solista will rely on the cached content to only re-build the pages, skipping the content parsing process.

## 🗺️ Roadmap

### 2.1

- Production-ready theme
- Template hierarchy
- Standard theme configuration (e.g. navigation)

### 2.2

- Content validation
- Schema-based structure enforcement

### 2.3

- SourceDriver (external sources support, e.g. APIs)

### 2.4

- Migration to symfony/console

### 2.5

- Rehearsal improvements
- Partial rebuilds based on requested resources

### Future

- WIP

## 🚧 Work in progress

Some parts of the ecosystem are still evolving:

- 📚 Documentation / Wiki
- 🧾 JSON Schema support (`$schema`)
- 🧩 Extended developer tooling

## 🧠 Philosophy

Solista is built around a few core ideas:

- content should live in real files
- structure should be explicit
- tools should stay out of your way
