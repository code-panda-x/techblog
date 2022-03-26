---
title: "What is Code"
date: 2021-12-20T21:40:15-05:00
draft: false
tags: ["What is"]
categories: ["General Tech"]
slug: "what-is-code"
subtitle: "Collection of code"
description: "Collection of code"
keywords: 
- Code
- Program
---

# About code

Sometimes I got confused by some concepts, such as machine code and object code. Here's a collection of "code" definitions

---


## Source code: (.c file)

Any collection of code, with or without comments, written using a human-readable programming language, usually as plain text.

---

## Assembly code (.s file)

is plain-text and (somewhat) human read-able source code that mostly has a direct 1:1 analog with machine instructions. This is accomplished using mnemonics for the actual instructions, registers, or other resources. Examples include `JMP` and `MULT` for the CPU's jump and multiplication instructions. Unlike machine code, the CPU does not understand assembly code. You convert assembly code to machine code with the use of an **assembler** or a **compiler**, though we usually think of compilers in association with high-level programming language that are abstracted further from the CPU instructions.


---

## Machine code (1000101)

- Machine language is made up of instructions and data that can be executed directly by the CPU. They are all **binary** code. **(Basically 0 and 1)**
- Machine language is normally displayed in **hexadecimal** form so that it is a little bit easier to read.
- If you open a machine code file in a text editor you would see garbage, including unprintable characters

---

## Object code (.o file)

is a **portion** of machine code not yet linked into a complete program. It's the machine code for one particular library or module that will make up the completed product. It may also contain placeholders or offsets not found in the machine code of a completed program. The **linker** will use these placeholders and offsets to connect everything together.

---

ref:

[https://stackoverflow.com/questions/466790/assembly-code-vs-machine-code-vs-object-code](https://stackoverflow.com/questions/466790/assembly-code-vs-machine-code-vs-object-code)

[https://cloud.tencent.com/developer/ask/196917](https://cloud.tencent.com/developer/ask/196917)