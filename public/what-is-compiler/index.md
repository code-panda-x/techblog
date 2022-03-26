# What is Compiler


# Dr. Hamer

![hamer.png](/images/hamer.png)

Here's a cartoon of the professor who taught me compiler: [Dr. Hamer](https://www.sdstate.edu/directory/george-hamer)

He's a character and a great professor with humor and fantastic teaching skills. He has influnced me a lot

# Compiler:

In [computing](https://en.wikipedia.org/wiki/Computing), a **compiler** is a [computer program](https://en.wikipedia.org/wiki/Computer_program) that [translates](https://en.wikipedia.org/wiki/Translator_(computing)) computer code written in one [programming language](https://en.wikipedia.org/wiki/Programming_language) (the *source* language) into another language (the *target* language)

---

Origin: The firist compiler was coded in the late 1950's for Fortran

---

A compiler will typically report errors

---

Compiler phases

![compiler.png](/images/compiler.png)

Lexical Analysis: The source program is broken up into individual tokens.

Syntax Analysis: Group the tokens into phases of the language.

Semantic Analysis: Check the meaning of our sentences.

Intermediate Code Generator: Create a machine independent representation of the source.

Code Optimization: Attempt to remove redundant and/or unneeded instructions.

Code Generation: Translate the intermediate code into a machine dependent target language.

---

Compiler performs 2 tasks:

1. Analysis (is this code written correctly?) - machine independent

2. Synthesis (convert to target language) - machine dependent

Front end: lexical analysis, syntax analysis, semantic analysis - Analysis

Both end: intermediate code reprensetation - Synthesis

Back end: code optimization, code generation - Synthesis

---

references：[https://www.tutorialspoint.com/compiler_design/compiler_design_phases_of_compiler.htm](https://www.tutorialspoint.com/compiler_design/compiler_design_phases_of_compiler.htm)
