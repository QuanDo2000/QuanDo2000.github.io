---
layout: post
title: Writing My First Post
date: 2023-04-08 18:30 -0400
categories: []
tags: [website, jekyll, markdown, blog]
---

This post will define the layout/structure of the posts on this website. I'll go over the process of creating a post, including the steps I took and the decisions I made.

## Goal

Outline the steps to create a post and the layout of the post.

### Why?

- I want to have a resource that I can refer to when creating a new post.
- I want all posts to have a consistent layout.
- This allows me to focus on writing the content instead of overthinking about the structure of the post.
- This also allows reader to know what to expect when reading a post.

### Requirements

- The process of creating a post should be simple.
- The layout should be simple and easy to understand.

## Process

### Setup

When creating my first post, I went through [Writing a New Post](https://chirpy.cotes.page/posts/write-a-new-post/) from the Chirpy documentation. This was a great first step because it gave me a good overview of the required fields for a post.

This was also a great start because it led me to [Jekyll Compose](https://github.com/jekyll/jekyll-compose), which is a plugin that allows you to create a new post from the command line. This was a great addition because it allowed me to create a new post without having to manually create a new file.

That's everything I needed to get started. I'll go over the steps I took to create a new post.

### 1. Create a draft

The first step will be to create a draft of the post. This will allow me to write the content of the post without the post being published even if I push the changes to the repository.

Following the steps from Jekyll-Compose, I'll run the following command:

```bash
bundle exec jekyll draft "Post Title"
```

This will create a new file in the `_drafts` folder with the following content:

<!-- prettier-ignore-start -->
```markdown
---
layout: post
title: "Post Title"
---

```
{: file="_drafts/post-title.md" }
<!-- prettier-ignore-end -->

#### Development Notes

When developing locally, I'll add the `--drafts` flag to the `bundle exec jekyll serve` command. This will allow me to see the draft posts when I run the website locally.[^1]

### 2. Publish the post

Once I'm done writing the post, I'll publish it by running the following command:

```bash
bundle exec jekyll publish _drafts/post-title.md
```

This will move the file from the `_drafts` folder to the `_posts` folder and rename the file to include the date in the filename and Front Matter.

### 3. Update the Front Matter

After publishing the post, I'll update the Front Matter to include the `categories` and `tags` fields. Updating the Front Matter will allow me to categorize the post and make it easier for readers to find the post.

The `categories` field can contain up to 2 categories and category names should be capital case. The `tags` field can contain any number of tags and all tag names should be lowercase.

### Layout

The general layout of the post will be as follows:

```markdown
---
layout: post
title: Post Title
categories: [Category 1, Category 2]
tags: [tag1, tag2, tag3]
---

## Goal

## Process

## Conclusion

## Footnotes (optional)
```

## Conclusion

This post outlined the process of creating a new post and the layout of the post. I'll use this post as a reference when creating new posts.

I aim to have most of the posts on this website follow this layout whenever possible. In some cases, I may need to deviate from this layout, but it will generally be the goal, followed by the main content, and finally the conclusion.

## Footnotes

[^1]: [Jekyll Drafts](https://jekyllrb.com/docs/posts/#drafts)
