---
title: "Ssr vs Csr"
date: 2023-07-23T13:45:28-05:00
draft: false
tags: ["Web"]
categories: ["General Tech"]
slug: "ssr-vs-csr"
subtitle: "Server side rendering vs Client side rendering"
description: "Server side rendering vs Client side rendering"
keywords: 
- Web
---

When user sends a request to a server, different server responses differently depending on the implementations.

## Server side rendering

Whenever you visit a website, your browser makes a request to the server. Once the request is done processing, your browser gets back the fully rendered HTML and displays it on the screen. If you then decide to visit a different page on the website, your browser will once again make another request for the new information. This will occur each and every time you visit a page that your browser does not have a cached version of.

It doesn’t matter if the new page only has a few items that are different than the current page, the browser will ask for the **entire new page** and will re-render everything from the ground up.

### Pros
1. Better SEO
2. The initial page load is faster
3. Good for static sties

### Cons
1. Frequent server requests
2. Overall slow page rendering
3. Full page reloads
4. Non-rich site interactions.

## Client side rendering 

Basically rendering content in the browser using JavaScript. Instead of getting all of the content from the HTML document itself, you are getting a bare-bones HTML document with a JavaScript file that will render the rest of the site using the browser.

This is much faster since you are only loading a very small section of the page to fetch the new content, instead of loading the entire page.

### Pros
1. Rich site interactions
2. Fast website rendering after the initial load
3. No full page reloads
4. Great for web applications (Next.js)

### Cons
1. Low SEO
2. Initial load might require more time