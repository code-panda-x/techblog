---
title: "How Data Are Stored"
date: 2022-01-30T21:57:04-05:00
draft: false
tags: ["How"]
categories: ["General Tech"]
slug: "how-data-are-stored"
subtitle: "How are data stored in your computer"
description: "How are data stored in your computer"
keywords: 
- Data
- Code
---

# How data are ACTUALLY sotred?

In a nutshell: All data are stored as 1's and 0's, 1 and 0 are represented by high/low voltage of transistors.

---

## Brief Introduction
Data are stored in **bits**, neither binary nor hex. They are both representations of data.

Computer only identifies **voltage levels**. There will be some voltage for 1 (high) and some lower voltage for 0 (low). When ever high voltage is passed its 1 and other one is 0.

We humans have a hard time looking at such and figuring out what’s going on. So we invent ways to make it easier on ourselves to visualize the workings of the computer. One way of doing this is to analogize those on and off signals as the numbers 1 and 0. This thinking of it in terms of binary numbers

---

## Dig into the Machine code

Machine code, to the actual circuitry, isn't numbers or values. Machine code is a bunch of voltage gates that are either open or closed, and depending on what they're connected to, a certain light will flicker at a certain time etc.

The "machine code" dictates the pathway and timing for specific electrical signals that will travel to reach their overall destination.

So for 010101, 3 voltage gates are closed (The 0's), 3 are open (The 1's)

010101 would be easy instructions for a simple circuit, but how does a complex computer process all of the information?

x-Bit-processors tell how many bits the processor can process at once.

A bit is either 1 or 0, "On" or "Off", "Open" or "Closed"

so 32-bit processors process "10101010 10101010 10101010 10101010" - this many bits at once.

A processor is an "integrated circuit", which is like a compact circuit board, containing resistors/capacitors/transistors and some memory. I'm not sure if processors have resistors but I know you'll usually find a ton of them located around the actual processor on the circuit board

Anyways, a transistor is a switch so if it receives a 1, it sends current in one direction, or if it receives a 0, it'll send current in a different direction... (or something like that)

So I imagine that as machine code goes... the segment of code the processor receives changes the voltage channels in such a way that it sends a signal to another part of the computer (why do you think processors have so many pins?), probably another integrated circuit more specialized to a specific task. That integrated circuit then receives a chunk of code, let's say 2 to 4 bits 01 or 1100 or something, which further defines where the final destination of the signal will end up, which might be straight back to the processor, or possibly to some output device.

Machine code is a very efficient way of taking a circuit and connecting it to a lightbulb, and then taking that lightbulb out of the circuit and switching the circuit over to a different lightbulb

Memory in a computer is highly necessary because otherwise to get your computer to do anything, you would need to type out everything (in machine code). Instead, all of the 1's and 0's are stored inside some storage device, either a spinning hard disk with a magnetic head pin that 'reads' 1's or 0's based on the charge of the disk, or a flash memory device that uses a series of transistors, where sending a voltage through elicits 1's and 0's (I'm not fully aware how flash memory works)

Fortunately, someone took the time to think up a different base number system for programming (hex), and a way to compile those numbers (translate them) back into binary. And then all software programs have branched out from there.

Each key on the keyboard creates a specific signal in binary that translates to a bunch of switches being turned on or off using certain voltages, so that a current could be run through the specific individual pixels on your screen that create "1" or "0" or "F", or all the characters of this post.

So I wonder, how does a program 'program', or 'make' the computer 'do' something... Rather, how does a compiler compile a program of a code different from binary? It's hard to think about now because I'm extremely tired (so I won't try) but also because EVERYTHING you do on a computer is because of some program. There are actively running programs (processes) in task manager. These keep your computer screen looking the way you've become accustomed, and also allow for the screen to be manipulated as if to say the pictures on the screen were real-life objects. (They aren't, they're just pictures, even your mouse cursor) (Ok I'm done. enough editing and elongating my thoughts, it's time for bed)

Also, what I don't really get is how 0's are 'read' by the computer. It seems that a '0' must not be a 'lack of voltage', rather, it must be some other type of signal Where perhaps something like 1 volt = 1, and 0.5 volts = 0. Some distinguishable difference between currents in a circuit that would still send a signal, but could be the difference between opening and closing a specific circuit.

If I'm close to right about any of this, serious props to the computer engineers of the world, the level of sophistication is mouthwatering. I hope to know everything about technology someday. For now I'm just trying to get through arduino.

Lastly... something I've wondered about... would it even be possible to program today's computers without the use of another computer?

---

ref:

[https://www.youtube.com/watch?v=Xpk67YzOn5w](https://www.youtube.com/watch?v=Xpk67YzOn5w)