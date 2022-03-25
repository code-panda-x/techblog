# Ultimate guide to build your own blog


## Before you start

All hugo commands should be run in the **root level**

---

## Build Hugo Blog Locally

### Step 1: Install hugo && git

For Mac user:
```
brew install hugo
brew install git
```

### Step 2: Create a new site
```
hugo new site myblog
cd myblog
```

### Step 3: Add a theme

You can find Hugo themes [Here](https://themes.gohugo.io/)

In this case I use [LoveIt](https://github.com/dillonzq/LoveIt) theme as my example

```
git init
git submodule add https://github.com/dillonzq/LoveIt.git themes/LoveIt

```

### Step 4: Basic Configuration

Copy config.toml content from example site to your config.toml

You can make your own changes in config.toml file

### Step 5: Create your first post 
```
hugo new posts/my-first-post.md
```

In .md file, set:
```
draft: false
```

Command above will generate a my-first-post.md file under the path: ./content/posts

You should **always** use hugo new posts/file.md to create new files

### Step 6: Host the Website Locally

```
hugo serve
```
Go to `http://localhost:1313`

### Step 7: Build the Website

Run: 

```
hugo
```

After you run the `hugo` command above, you will see content created under `public` folder in your blog folder

---

## Upload your code to GitHub

### 1. Create a new repo on GitHub
If you want to deploy on GitHub page:

Create a repo named `your-github-username.github.io`

For example: 

My GitHub username is `code-panda-x`
My repo will be named `code-panda-x.github.io`

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

1. Sign in Netlify with GitHub account
2. Add new site - Import an existing project
3. Select your GitHub repo
4. Your site will be pubished with a netlify domain

## Deploy on GitHub Page

Your site will be published on `your-github-username.github.io`

## Customize Domain

1. Purchase your domain at Godaddy.com or namecheap.com
2. Configuration

### DNS Management 
#### Netlify
Add:
1. Type: `A` Name: `@` Value: `75.2.60.5` (Netlify’s load balancer IP address)
2. Type: `CNAME` Name: `www` Value: `your-url.netlify.app`

#### GitHub Page

Add:
1. Type: `A` Name: `@` Value: `185.199.108.153` 
2. Type: `CNAME` Name: `www` Value: `your-github-username.github.io`

---

### Host Settings
#### Netlify
Domains - Custom domains - Add custom domain - Enter your purchased domain

#### GitHub Page
Settings - Code and automation - Custom domain - Enter your purchased domain

---

## Error Messages and Solutions 

```
    Building sites … ERROR 2019/11/30 09:22:03 Failed to read Git log: fatal: your current branch 'master' does not have any commits yet Built in 135 ms
```
In config.toml:

Set `enableGitInfo = true`

---

```   
Error: module "xxx" not found; either add it as a Hugo Module or store it in "/home".: module does not exist
```

In config.toml:

Set `themesDir = "themes"`
