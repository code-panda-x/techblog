# What is Assembler


# Assembler 
An assembler translates **assembly language** into **machine code**

# Assembling Process

![assembler.png](/images/assembler.png)

---

## A SIC/XE source program looks like this

![source-program.png](/images/source-program.png)

## A Intermediate file looks like this

![inter-file.png](/images/inter-file.png)

## An object file looks like this

![obj.png](/images/obj.png)

---

- **Pass-1:**
    1. Define symbols and literals and remember them in symbol table and literal table respectively.
    2. Keep track of location counter
    3. Process pseudo-operations
- **Pass-2:**
    1. Generate object code by converting symbolic op-code into respective numeric op-code
    2. Generate data for literals and look for values of symbols

---
