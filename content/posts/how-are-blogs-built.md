---
title: "How are blogs built"
date: 2023-07-19T20:43:29-05:00
draft: false
tags: ["Blog", "Hugo", "Git"]
categories: ["General Tech"]
slug: "how-are-blogs-built"
subtitle: "How are most of the websites/blogs really built"
description: "How are most of the websites/blogs really built"
keywords: 
- Hugo
- Blog
- GitHub
---

## How are most of the websites/blogs built? Really?
Typically, there are two layers of website building:
1. Pull content from local file system (md files) or third party CMS
2. Render the website
   
### The first layer - Content pulling 

Conventional blog engines hosted on GitHub (Hexo, Hugo, Jekyll) host their "content" in files stored and managed by Git. 

Gatsby and Gridsome, besides supporting file-based content sourcing, also have plugins that enables them to pull "content" from a third-party CMS, whether it's a self-hosted WordPress or Ghost, or a standalone cloud-based solution like Strapi, DatoCMS, or Contentful.

### The second layer - Content rendering 

Content rendering is handled by our website generator, where it makes use of the data that we provide in the first layer, and compiles / renders the website on demand. 

Again, conventional blog engines (Hexo, Hugo, Jekyll) get their data during build-time, and requires rebuilding the entire site when data is updated (like updating articles, publishing new articles, etc.). 

Newer frameworks (like Next.js) are able to take advantage of "server-side rendering" (SSR) that guarantees to return the newest content pulled from layer one without having to rebuild or re-render the whole site.

## Blog building workflow

![blogflow.png](/images/blogflow.png)

In my case, I store markdown files locally and use Hugo to generate web content. 

I use GitHub to host my code and I use Netlify to depoly my website live.

Detailed blog building processes can be found [here](/build-hugo-blog/)

## More...

Hugo is a static site generator (webiste displays the same to all users). 

If we want dynamic websites (websties that response to different user differently), we need tools like wordpress.

One other way is to code up a website on your own using any frameworks (React/Express/ASP.NET) and deploy it. This is a good practice to learn different tech stacks.

### Some pros and cons for each option
https://devpractical.com/how-are-websites-created/