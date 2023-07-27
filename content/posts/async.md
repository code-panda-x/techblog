---
title: "Async Programming"
date: 2023-07-26T21:03:35-05:00
draft: false
tags: ["Async","Programming"]
categories: ["General Tech"]
slug: "async-programming"
subtitle: "Async Programming"
description: "What is async programming"
keywords: 
- Async
- Programming
---

## Async Porgramming

### What is async programming?


Async programming is about **non-blocking** execution between functions.

It enables your program to **start a potentially long-running task** and still be able to **be responsive to other events** while that task runs, 

So we don’t have to wait our time waiting for that long task to be finished

#### Example
Data may take long a long time to submit to/retrieve from a database. With asynchronous programming, the user can move to another screen while the function continues to execute. When a photo is loaded and sent on Instagram, the user does not have to stay on the same screen waiting for the photo to finish loading. The user can continue in the app or leave the app while the photo loads. 

This can be achieved by taking a call-back reference. The async call takes a call-back reference and returns execution back to your code as soon as the request has been placed with the remote system. Your UI can continue to respond to the user while the remote system does whatever processing is required, once it returns the data to your call-back method then that method can update the UI (“Photo Uploaded!”) as appropriate.

### Sync vs Async

- Synchronous: you cook the eggs, then you cook the toast.
- Asynchronous (single threaded): you start the eggs cooking and set a timer. You start the toast cooking, and set a timer. While they are both cooking, you clean the kitchen. When the timers go off you take the eggs off the heat and the toast out of the toaster and serve them.
- Asynchronous (multi-threaded): you hire two more cooks, one to cook eggs and one to cook toast. Now you have the problem of coordinating the cooks so that they do not conflict with each other in the kitchen when sharing resources.

Async programming can be applied to single or multi-threading

### C# Async Implementation

https://learn.microsoft.com/en-us/dotnet/csharp/asynchronous-programming/

https://learn.microsoft.com/en-us/dotnet/csharp/asynchronous-programming/async-scenarios