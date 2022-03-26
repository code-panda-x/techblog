---
title: "HTTP"
date: 2022-02-07T15:41:20-05:00
draft: false
tags: ["Network", "HTTP"]
categories: ["General Tech"]
slug: "http"
subtitle: "HTTP methods and status code"
description: "HTTP methods and status code"
keywords: 
- HTTP methods
- HTTP status code
---


## HTTP methods
GET: **Retrieve data** from a server only

- HTTP GET won't have payload or request body, just send URL only, it simply retrieves data

POST: **Add data** (create a new object) on the server

PUT: **Update** an existing object or resource in a server

DELETE: **Delete** data from a server

**Remove** is NOT an HTTP verb


## HTTP status code cheatsheet
- 1xx status codes: Informational requests
- 2xx status codes: Successful requests
- 3xx status codes: Redirects
- 4xx status codes: Client errors
- 5xx status codes: Server errors   

```
Code    Status              Description
200     OK                  The request is successful
201     Created             A new resource was successfuly created
400     Bad request         The request is invalid (My problem)
401     Unauthorized        Requires authentication
403     Forbidden           The client is authenticated but doesn't have permission to access the requested resource
404     Not Found           The requested resource was not found (API's problem)
405     Method not allowed  HTTP request method is not supported (use GET to update)
500     Internal Server error
503     Server unavailable
```

Ref: https://stackoverflow.com/questions/2342579/http-status-code-for-update-and-delete

detailed cheatsheet: https://www.exai.com/blog/http-status-codes-cheat-sheet

