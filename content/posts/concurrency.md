---
title: "Concurrency vs Parallelism"
date: 2023-07-31T20:30:01-05:00
draft: false
tags: ["OS"]
categories: ["General Tech"]
slug: "concurrency-vs-parallelism"
subtitle: "Concurrency vs Parallelism"
description: "Concurrency vs Parallelism"
keywords: 
- OS
- Program
---

### Concurrency (Multithreading on a Single Processor)

**Concurrency** means executing multiple tasks at the same time but **not necessarily simultaneously**. When you have to perform more than one task but you have **a single resource** then we go for concurrency. In a single-core environment, concurrency is achieved by **context switching**. (the execution of multiple tasks is interleaved, instead of each task being executed sequentially one after another.)



> For example: This is a bit like chatting with different people through various IM windows; although you’re actually switching back and forth, the net result is that you’re having multiple conversations at the same time.

### Parallelism (Multithreading on multi-core) (Multiprocessing)

**Parallelism** means that your program leverages the hardware of **multi-core** machines to execute tasks at the same time by breaking up work into tasks, each of which is executed on a separate core. 

Example
> For example: In a browser, multiple tabs can be different threads. MS Word uses multiple threads: one thread to format the text, another thread to process inputs

#### Note
Concurrency & parallelism are **concepts**

Multithreading are **implementations**