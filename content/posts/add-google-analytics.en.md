---
title: "Add Google Analytics to Hugo Blog"
date: 2022-03-05T22:35:38-05:00
tags: ["Blog", "Hugo", "Google Analytics", "JavaScript"]
categories: ["General Tech"]
slug: "add-google-analytics-hugo"
subtitle: "Add Google Analytics to Hugo Blog"
description: "Add Google Analytics to Hugo Blog"
keywords: 
- Hugo
- Blog
- Google Analytics
---


## Google Analytics
0. Register a google analytics account
1. Get your measurement ID that looks like below

        G-6ED0IWOAJK
2. Get gtag js script
```
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-6ED0IWOAJK"></script>
<script>
window.dataLayer = window.dataLayer || [];
function gtag(){dataLayer.push(arguments);}
gtag('js', new Date());
gtag('config', 'G-6ED0KEHXFZ');
</script>
```

---


## Hugo blog 
1. Find config.toml file, enable google analytics as below
```
    enableGoogleAnalytics = true
    trackingCodeType = "gtag"
    trackingID = "G-6ED0IWOAJK"
```
This is my settings above, you may just need

    googleAnalytics = "G-6ED0IWOAJK"

---

2. Add gtag script to path: 

    /themes/your-theme/layouts/_internal/google_analytics_async.html
- You may need to create a new folder and new html file 
- Paste gtag js script above to the html file

---

3. Add template code to path: 
    /themes/your-theme/layouts/partials/header.html
```
    {{ if not .Site.IsServer }}
        {{ template "_internal/google_analytics_async.html" . }}
    {{ end }}
```
- You only need the second line but the if statement prevents local builds being tracked by GA


## Google Analytics should be about to work!
If it doesn't work, wait for a while. I added GA late at night and it didn't make an effect immediately.

The next day I woke up, It worked! 😁