---
title: "Build Your Hugo Blog Using GitHub and Netlify"
date: 2021-06-22T13:46:52-05:00
draft: false
tags: ["Blog", "Hugo", "Git"]
categories: ["Tech"]
---

## Before you start

All hugo commands should be run in the **root level**

## Step 1: Install hugo && git

For Mac user:
```
brew install hugo
brew install git
```

## Step 2: Create a new site
```
hugo new site myblog
cd myblog
```

## Step 3: Add a theme

You can find Hugo themes [Here](https://themes.gohugo.io/)

In this case I use [LoveIt](https://github.com/dillonzq/LoveIt) theme as my example

```
git init
git submodule add https://github.com/dillonzq/LoveIt.git themes/LoveIt

```

## Step 4: Basic Configuration

Copy config.toml content from example site to your config.toml

You can make your own changes in config.toml file

## Step 5: Create your first post 
```
hugo new posts/my-first-post.md
```

In .md file, set:
```
draft: false
```

Command above will generate a my-first-post.md file under the path: ./content/posts

You should **always** use hugo new posts/file.md to create new files

## Step 6: Host the Website Locally

```
hugo serve
```
Go to `http://localhost:1313`

## Step 7: Build the Website

Run: 

```
hugo
```

After you run the `hugo` command above, you will see content created under `public` folder in your blog folder

## Upload your code to GitHub

### 1. Create a new repo on GitHub

### 2. Git Initialiaztion

```
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/your-github-username/your-repo-name.git
git push -u origin main
```

#### Whenever you make changes in your blog folder

Run :

```
hugo
```

Above code will update corresponding changes to public folder

Then run:

```
$ git add .
$ git commit -m "add blog post"
$ git push


```
You can use git status to check your changes
```
$ git status
```


## Deploy on Netlify
```
hugo server -D
```


