---
title: "Enable Spotlight search on Mac"
date: 2022-03-26T11:45:57-05:00
draft: false
tags: ["Mac", "Spotlight"]
categories: ["General Tech"]
slug: "express-restapi"
subtitle: "Spotlight doesn't work"
description: "Spotlight doesn't work"
keywords: 
- Mac
- Spotlight
---

## Method 1
Navigate to
1. System Preferences
2. Spotlights
3. Privacy
4. Add your local disk to the list 
5. Remove your local disk from the list
The above steps will reindex spotlight on the selected disk

## Method 2
In terminal run:
```
sudo mdutil -E /
sudo mdutil -a -i on
```
Above commands fixed everything for me
