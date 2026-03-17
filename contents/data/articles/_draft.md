---
title: Ignore me
description: This post is just a draft
published_at: 2026-03-19
---

## How to make a draft?

It's really simple, actually. There are two methods to set a content as draft:

1. Name the file with an underscore at the start (ex. _draft.md)
2. In the frontmatter add "draft: true"

Keep in mind that the frontmatter overwrites the behavior of the file name.

If, for example, you have a file named "_draft.md" but in the frontmatter you set "draft: false", the content
will be published.

## But why can I see it on Rehearsal?

This is a little magic actually. Rehearsal is a preview server, so it makes sense to see the drafted contents
in there.

Thanks to this little feature, you can preview contents before publishing it. Rehearsal promises that it won't
give your secret informations to the build command.

## What about the slugs?

Don't worry. Solista will take care of it, the system will automatically strip the "_" in front of the filename.
