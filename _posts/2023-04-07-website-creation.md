---
layout: post
title: Website Creation
date: 2023-04-07 19:37 -0400
categories: []
tags: [website, jekyll, github pages, markdown, domain name, hosting, blog]
---

This post is about the creation of this website. I'll go over the process of creating a website from scratch, including the challenges I faced and the solutions I found.

## Goal

Creating a platform to share my work, experiences, and interests. For me, this means creating a personal website.

### Why?

- To share my work and experiences with others.
- To practice my skills, both in development and writing.

### Requirements

- A personal domain name.
- A simple, clean design.
- Must be easy to update and maintain.
- Articles must be easy to write and publish. (Markdown)

## Process

### 1. Domain Name

The first step was to find a domain name. Because this is a personal website, I decided to use my name and I was able to purchase the domain name `dominhquan.com`

The domain name was purchased through [Google Domains](https://domains.google/). I chose Google Domains because it was easy to use and the price was reasonable compared to other domain name providers.

### 2. Hosting

The next step was to decide on how to host the website. At first, I wanted to host the website on my own computer, but I quickly realized that this would be difficult to maintain and update. There were also security concerns, as I would have to expose my computer to the internet.

This led me to look into hosting options. If I wanted to host a fullstack website with both a backend and a frontend, I would need to find hosting for both. Which finally led me to static site hosting, which only requires hosting for the frontend and all the content is stored in markdown files.

I decided to use [GitHub Pages](https://pages.github.com/) to host the website. GitHub Pages is a static site hosting service that is free for public repositories. It is also easy to use and integrates well with GitHub.

After deciding on using GitHub Pages, all I needed to do was follow the instructions on the [GitHub Pages documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) to create a new repository and enable GitHub Pages.

#### Configuring Custom Domain Name

Since this was a personal website, I used the `<username>.github.io` format for the repository name. This allowed me to use the domain name `QuanDo2000.github.io` for the website. But since I already had a domain name, I needed to configure the domain name to point to the GitHub Pages website.

1. Go to the [Verify Domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages) and follow the instructions to verify the domain name.

   - For Google Domains, this involved adding a TXT record to the domain name's DNS settings, specifically the Custom records section.
   - This step verifies that your GitHub account has access to the domain name and not specific to GitHub Pages or to any repository.
   - This step is necessary to prevent malicious users from using your domain name to host their own website.

2. Create a repository named `QuanDo2000.github.io` and enable GitHub Pages for the repository.

   - This step creates the website and allows you to access it at `QuanDo2000.github.io`.
   - There are some challenges with this step, and I'll go over them in the next step [3. Design](#3-design).

3. Go to the [Manage Custom Domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) and follow the instructions to add the domain name to the repository.

   - Here, I followed the sections titled "Configuring a subdomain" and "Configuring an apex domain" because I have an apex domain name (i.e. `dominhquan.com`) and my website is pointed to the subdomain `www`.
   - For Google Domains, this involved adding a CNAME record and an A record to the domain name's DNS settings, specifically the Custom records section.
   - This step allows you to access the website at `www.dominhquan.com` instead of `QuanDo2000.github.io`.

### 3. Design

For the design of the website, I wanted to use a simple, clean design. I also wanted to use a design that was easy to maintain and update. I decided to use [Jekyll](https://jekyllrb.com/) to create the website. Jekyll is a static site generator that uses Liquid templates and Markdown files to generate a static website.

I chose Jekyll because it is easy to use and integrates well with GitHub Pages. It also uses Markdown files to store the content, which makes it easy to write and publish articles.

Knowing that I wanted to use Jekyll, I needed to find a Jekyll theme that I liked, and that theme is [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy). Chirpy is a Jekyll theme that is easy to use and has a clean design. It also has a lot of features that I wanted, such as a dark mode, and a search bar.

This is where I ran into some challenges mentioned in the previous step [2. Hosting](#2-hosting). If we look at the [Getting Started documentation](https://chirpy.cotes.page/posts/getting-started/), we can see that the instructions for using Chirpy are to use the [Chirpy Starter](https://github.com/cotes2020/chirpy-starter) repository. This repository is a template repository that can be used to create a new repository with the Chirpy theme. Using this template repository meant that I can only create the repository after selecting the theme. So, if we created the repository without the template, we would have to delete the repository and create a new one with the template.

<!-- prettier-ignore -->
> TLDR: If your Jekyll theme has a template repository, you need to create the repository with the template repository.
{: .prompt-info }

### 4. Deployment

The final step was to deploy the website. Despite using GitHub Pages, we still needed to make some changes to the settings in order to deploy the website. Because we used a Jekyll theme which was not natively supported by GitHub Pages, we needed to use GitHub Actions to build the website and deploy it to GitHub Pages. More information about this can be found in the [Chirpy documentation](https://chirpy.cotes.page/posts/getting-started/#deployment).

<!-- prettier-ignore -->
> Note: The default deployment workflow works great out of the box and there is no need to create a custom workflow.
{: .prompt-info }

## Conclusion

At the end of this process, I was able to create a personal website that I can use to share my work and experiences. I also learned a lot about the process of creating a website and I hope that this post can help others who are interested in creating their own website.

Some of the things that I learned include:

- How to purchase a domain name.
- The difference between a static site and a fullstack site.
- How to use GitHub Pages to host a website.
- How to use Jekyll to create a website/blog.
- How to connect a custom domain name to a GitHub Pages website.
