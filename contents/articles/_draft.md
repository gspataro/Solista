---
title: Ignore me
description: This post is just a draft
published_at: 2026-03-19
---

## How to create a draft

It's actually very simple. There are two ways to mark a piece of content as a draft:

1. Prefix the filename with an underscore (e.g. `_draft.md`)
2. Add `draft: true` in the frontmatter

Keep in mind that the frontmatter always takes precedence over the filename.

For example, if you have a file named `_draft.md` but set `draft: false` in the frontmatter, the content will still be published.

## Why can I see it in Rehearsal?

This is intentional. Rehearsal is a preview server, so it makes sense for it to include draft content.

This allows you to safely preview your work before publishing it. Drafts are never included in the final build, so your unpublished content remains private.

## What about slugs?

No worries — Solista takes care of that for you.

If a filename starts with an underscore, the system will automatically strip it when generating the slug. This way, your URLs remain clean and consistent.
