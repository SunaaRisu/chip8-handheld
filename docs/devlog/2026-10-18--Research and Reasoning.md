# Reasoning and Research — Devlog \[18.10.2026\]

## Why this project?

In my third semester I visited the lecture "Technische Informatik" where we were shown the concept and architecture of a CPU on the example of the ReTII processor and its emulator written by the processor. While we learned the theory of CPUs and even wrote some programs in ReTII assembly language, we never looked at the practical implementation we used. Therefore, the first part of the project was clear. I want to build an emulator.
But I didn't want to build just another emulator for some random CPU. Aside from that, I didn't want to write some software but rather combine it with hardware to build a full embedded product.
After some research on vCPUs, I found CHIP8. A specification for a virtual machine designed in 1977 by Joseph Weisbecker for the COSMAC VIP computer.
This specification matched my requirements perfectly. It's a CPU I can write an emulator for, and it's targeted for running retro games like Pong or Tetris. Now I got the second part of the project. A handheld console that runs CHIP8 games.

## Research

While researching, I found two sources that laid out the functions my emulator needed to have. A [course from Columbia University](https://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/designs/Chip8.pdf) and an [article by Tobias V. I. Langhoff](https://tobiasvl.github.io/blog/write-a-chip-8-emulator/). These describe the function of the CHIP8 CPU but not the hardware abstraction layers or the building of the handheld. These are the three parts of the project.

1. CHIP8-core alongside the SDL-HAL for debugging purposes.
2. The ESP32-HAL alongside the first prototype of the handheld.
3. The final handheld.

## What's next?

For the next sprint my target is to layout the project a bit better and implement the first fundamental functions like create, destroy, and reset the CPU. Additionally, I want to start implementing the memory and memory-related functions to load ROMs and initialization, as well as some debugging functions to print the state of the processor.
