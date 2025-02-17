# Samsung-RISC-V
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this training is Kunal Ghosh Sir.
# Basic Details
Name: VAJRAMANASA PALGUNA H V

College: R V institute of technology and management

Email ID: rvit22bec044.rvitm@rvei.edu.in

GitHub Profile: [maverick-369](https://github.com/maverick-369/samsung-riscv/)

LinkedIN Profile: [VAJRMANASA PALGUNA H V](www.linkedin.com/in/vajramanasa-palguna-h-v-061579253)

# VSDSquadron Mini Overview
<details>
<summary> Preview </summary>
<br>
  
## Block diagram of VSDSquadron Mini RISC-V development board is shown below

![b1](https://github.com/user-attachments/assets/e7339091-3882-4aa0-9fc5-665118aaa264)

## VSDSquadron Mini RISC-V development board Board image

![b2](https://github.com/user-attachments/assets/55c19e7e-ebfd-40cc-bf83-527ba790bb87)

## Information about the VSDSquadron Mini RISC-V SoC device

Refer to [CH32V003F4U6 RISC-V SoC Datasheet](https://www.vlsisystemdesign.com/wp-content/uploads/2024/01/Web01_CH32V003DS0.pdf) and [CH32V003F4U6 RISC-V SoC Reference Manual](https://www.vlsisystemdesign.com/wp-content/uploads/2023/09/Web02_CH32V003RM.PDF)

## Overview of VSDSquadron Mini RISC-V development boards

a) On-board 24MHz RC oscillator

b) 3 groups of GPIO ports, totaling 15 I/O ports

c)  USART, I2C, and SPI

d) UART implemented on USART

e) 2KB SRAM for volatile data storage, 16KB CodeFlash for program memory

f) On-board Programmer. NO NEED of any additional adapter

## Dimensions of the VSDSquadron Mini RISC-V development board

a) Form factor is 50.00 x 28.00 mm

b) Maximum height of the component at the top side: 8mm

c) Maximum height of the component at the bottom side: 1mm

</details>

# Installation of Virtual Box, openlane vdi file, VS Code setup

<details>
<summary> Preview </summary>
<br>
  
## Virtual Box and vsdsquadron vdi file setup screenshots

### For installing vdi file click [openlane_vdi_file](https://forgefunder.com/%7Ekunal/vsdsquadron.vdi)

![Screenshot 2025-01-09 085732](https://github.com/user-attachments/assets/23cbec6d-dd68-41a3-8e49-8f39c73f8d38)

![Screenshot 2025-01-09 085821](https://github.com/user-attachments/assets/5d41e9b4-29ea-4654-a406-5751f8a784d8)

![Screenshot 2025-01-09 085842](https://github.com/user-attachments/assets/9a223b9b-c8d1-4bda-84ad-8ad432def387)

![Screenshot 2025-01-09 085903](https://github.com/user-attachments/assets/20c4d30e-82da-49db-9947-9893a4e9652d)
</details>
---

<details>
<summary> <b>Task 1:</b>The task requires a detailed review of lab videos focused on C programming and the RISC-V architecture to develop a deep understanding of both topics. Following this, you are expected to compile C code using two distinct compilers: the GCC compiler and the RISC-V compiler. This exercise will demonstrate your comprehension of the compilation process, allowing you to observe and compare how each compiler converts the C code into machine code. You will analyze the differences and nuances in the compilation processes for different processor architectures, emphasizing the specificities of each..</summary> 
<br>
Task is to refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler.

**C Language based LAB**

**C and RISC-V Based Labs**

This repository demonstrates the processes involved in compiling C programs and generating assembly code using both a standard GCC compiler and a RISC-V GCC compiler. It includes comprehensive steps and explanations to guide users through each stage of the compilation and debugging workflow.

**C Language-Based Lab**

Steps to Compile a .c File on Your Machine:

1. Open the bash terminal and navigate to the directory where you want to create your file.
2. Use the following command to create and edit a new .c file:
   ```sh
   leafpad sum1ton.c


**Steps to Compile a .c File on our Machine:**
 ```sh
 gcc sum1ton.c
 ./a.out
```

 
Compilation and execution complete.
 
![Image](https://github.com/user-attachments/assets/2ddedf49-a6a4-4cd6-a9a9-f800b3b0a6f2)
)
RISC-V Based Lab

**Steps to Compile Using RISC-V GCC Compiler:**
1. Ensure the RISC-V GCC compiler is installed and accessible on your system.
2. Verify the .c file contents using the cat command:
   ```sh
   cat sum1ton.c


3. Compile the C program for RISC-V architecture using 01 option:
 ```sh
riscv64-unknown-elf-gcc -o1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
4. Disassemble the object file to view its assembly code using:
 ```sh
riscv64-unknown-elf-objdump -d sum1ton.o
```
5.minimize the assembly by using following code:
```sh
riscv64-unknown-elf-objdump -d sum1ton.o | less
```
 a)we extract main function's assembly code by using:
   ```sh
/main
```
6. Use /main in the terminal to locate the main function in the assembly output.
![Image](https://github.com/user-attachments/assets/2ddedf49-a6a4-4cd6-a9a9-f800b3b0a6f2)

7.Compile the C program for RISC-V architecture using ofast option:
```sh
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
8.Disassemble the object file to view its assembly code using:
```sh
riscv64-unknown-elf-objdump -d sum1ton.o
```
9.minimize the assembly by using following code:
```sh
riscv64-unknown-elf-objdump -d sum1ton.o | less
```
 a)we extract main function's assembly code by using:
 ```sh
  /main
```
10. Use /main in the terminal to locate the main function in the assembly output.
![Image](https://github.com/user-attachments/assets/575a7a3c-c918-40ac-a018-ff1a1c90df3f)

Explanation of Key Commands and Options: 
1. -mabi=lp64: Specifies the Application Binary Interface (ABI) for 64-bit integers, pointers, and long data types, suitable for 64-bit RISC-V architecture.

2. -march=rv64i: Indicates the 64-bit RISC-V base integer instruction set architecture.

3. -O1: Enables basic optimization for better performance without significantly increasing compilation time.

4. -Ofast: Optimize the code aggressively for the best possible speed.

5. riscv64-unknown-elf-objdump: A tool for disassembling RISC-V binaries to examine the code structure and debug it effectively.
 
   </details>

---
