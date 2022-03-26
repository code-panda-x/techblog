---
title: "What happens when you run your program"
date: 2021-09-10T20:37:28-05:00
draft: false
tags: ["What happens when"]
categories: ["General Tech"]
slug: "what-happens-when-run-program"
subtitle: "How program compiles"
description: "How program compiles"
keywords: 
- Compiler
- Program
---

When you click "run" or "compile" in your IDE, you will get a result from the program. 

But **what actually happens** inside the computer?

# Compliation Porcess

```
=====> COMPILATION PROCESS <======

                     |
                     |---->  Input is Source file(.c)
                     |
                     V
            +=================+
            |                 |
            | C Preprocessor  |
            |                 |
            +=================+
                     |
                     | ---> Pure C file ( comd:cc -E <file.name> )
                     |
                     V
            +=================+
            |                 |
            | Lexical Analyzer|
            |                 |
            +-----------------+
            |                 |
            | Syntax Analyzer |
            |                 |
            +-----------------+
            |                 |
            | Semantic Analyze|
            |                 |
            +-----------------+ -----> Compiler
            |                 |
            | Pre Optimization|
            |                 |
            +-----------------+
            |                 |
            | Code generation |
            |                 |
            +-----------------+
            |                 |
            | Post Optimize   |
            |                 |
            +=================+
                     |
                     |--->  Assembly code (comd: cc -S <file.name> )
                     |
                     V
            +=================+
            |                 |
            |   Assembler     |
            |                 |
            +=================+
                     |
                     |--->  Object file (.obj) (comd: cc -c <file.name>)
                     |
                     V
            +=================+
            |     Linker      |
            |      and        |
            |     loader      |
            +=================+
                     |
                     |--->  Executable (.Exe/a.out) (com:cc <file.name> )
                     |
                     V
            Executable file(a.out)
```

- A [compiler](/what-is-compiler) reads, analyses and translates code into either an object file or a list of error messages.
- A [assembler](/what-is-assembler) converts assemlby code to object files.
- A [linker](/what-is-linker-loader) combines one or more object files and possible some library code into either some executable, some library or a list of error messages.
- A loader reads the executable code into memory, does some address translation and tries to run the program resulting in a running program or an error message (or both).

---

ref: https://www.youtube.com/watch?v=QXjU9qTsYCc