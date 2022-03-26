# How to run a program from scratch


This might be a stupid question for a programmer who has years of programming experience. But when I first started programming, I have no clue how to run a program. I simply followed my professor's instruction: downloaded codeblocks/visual studio, typed in some code, and I could run my program magically! Back in the days, I did't understand what an IDE means, [how program compiles](/what-happens-when-run-program) inside the IDE, why the code is layed out in certain ways, etc. But I have figured out these foundemental questions through years.

## Requirements to run a program

Hardware：

1. It must have the correct class of CPU to execute the instructions in the code.
2. It must have sufficient hardware resources to support the code: memory, CPU speed, perhaps graphics or sound subsystems, or other peripheral devices

Software：

1. It must have an OS environment that supports the system calls built into the software by the programmer/designer. This might include configuration items, such as pre-existing directory structures, filesystem permissions, environment variable settings, and numerous other settings. Usually, an installation procedure will look after this part, if there is one.
2. A program needs to start operating system compatibility, and additionally some other support software (for example, programs in Java will need the virtual machine of java). If the program uses any device, you must have the appropriate driver for the operating system, the device and the same program.
3. It must have installed support libraries, often from hardware vendors, or other software products. This might even include the presence of some standalone software products, such as a database server. Often, these are version dependent; specific versions of each must be present.

## What do we need to do exactly?

Three main ways to run a program:

1. Set up IDE (VS, Xcode), and setup environments to run program inside IDE
2. Install compiler on your device (brew install gcc)
3. Use cloud computing (Google cloud platform, School linux server...)
