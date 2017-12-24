# Y32 Blog

[https://y32.github.io/](https://y32.github.io/)

## Contributing

**Please do all work inside feature branches, and subsequently open a PR.**

### Submitting posts

1. Make a new markdown (`.md`) file in `_posts` following the convention: `YYYY-MM-DD-some-title.md`

2. Blog to your heart's content. Spell check, and test your build locally with `jekyll serve`.

3. Ensure your front matter at the beginning of the file looks like:

```yaml
---
layout: post
title: "Your title"
date: 2017-07-29 15:57:30 -0500
author: name
tags: ruby tutorial
---
```

The `date` field may be filled initially with the date of authorship, or the date of opening the pull request. It will be updated to the current date when the post is merged & published to reflect the date of publication. Other blog members should add a commit to your PR before they merge it that updates this field.

> **Note:** If you're a new member of the blog, be sure you have an author entry in our `_config.yml`.

**Members: Please *squash posts* into one commit when merging to `master` following approval.**

### Updating Jekyll theme, adding new pages, etc.

- Please discuss these in the Discord beforehand before putting the time into the blog frontend (since this affects everyone)
- If you can, throw up your own host so we can check it out. Otherwise provide screenshots, etc.
- Test the layout as best you can ensuring existing posts render correctly, especially if your addition relies on newly required front matter to render correctly.
- `custom_css` front matter property: Our front matter supports this key for adding special CSS to special pages. I.e.; not blog posts. Make use of this property when adding new top-level pages that need special formatting that doesn't constitute a change to the master CSS pipeline.
