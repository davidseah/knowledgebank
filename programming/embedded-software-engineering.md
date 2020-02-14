# Embedded Software Engineering

{% embed url="https://embedded.fm/blog/ese101" %}

A microcontroller is made up of three simple things

1. Instructions
2. Registers
3. Memory

### Instructions

Instructions are the things that a microcontroller knows how to do. 

Instructions operate on numbers that are stored in registers and memory.

### Register

Registers are very fast storage that holds the numbers that instructions operate on. One way to think of it is that a register is a scratchpad for instructions to use. 

A microcontroller has a small number registers, typically 8-32. 

### Memory

Memory is also storage for number but memory is much more plentiful and slower than registers. 

### Where does a microcontroller get instructions from? 

When a microcontroller powers up it looks in a defined memory location for the first instruction to run. It runs the first instruction, and then looks at the next memory location for the second instruction, runs it and so on. 

We have some instructions in memory, along with some data. How does the microcontroller know where to find the instructions? 

It uses a special register called a Program Counter\(PC\) to keep track of where in memory it's looking for instructions. 

When a microcontroller powers up or is reset, the PC is automatically set to some known starting address so it always starts at the same place. 

A microcontroller does its job by following three simple steps

1. Read the instruction at the memory address in the PC register
2. Run the instruction
3. Update the PC register to point to the next instruction in memory

These three steps are repeated forever until the power is turned off. 



### Status Register

the status register is a special register. It doesn't hold regular values like R0-R3 or even PC. Instead the status register has a few different bits that instructions can be use to check the status of previous operation. 

