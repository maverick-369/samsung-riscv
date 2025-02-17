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

![Image](https://github.com/user-attachments/assets/2ddedf49-a6a4-4cd6-a9a9-f800b3b0a6f2)

![Image](https://github.com/user-attachments/assets/575a7a3c-c918-40ac-a018-ff1a1c90df3f)

![Image](https://github.com/user-attachments/assets/7803d585-135b-44c3-9a59-ed015a403341)

![Image](https://github.com/user-attachments/assets/ed8be547-89cb-4ba3-ac94-377d1512d084)
)



<details>
<summary> <b>Task 2:</b> The task involves reviewing both C-based and RISC-V-based lab videos to understand the nuances of compiling C code for different architectures. Afterward, you are required to execute the process of compiling the C code using two distinct tools: the GCC compiler and the RISC-V compiler simulator. This will allow you to demonstrate your ability to work with both compilers, providing insights into how the C code is processed and converted into machine-readable code for each specific architecture.</summary> 
<br>

Task is to analyze the SPIKE simulation performance using RISC-V GCC with -O1 and -Ofast optimization levels.  

*SPIKE Simulation and Compiler Optimization*

This repository demonstrates how to compile a C program using RISC-V GCC, simulate it using SPIKE, and compare the performance of different optimization levels (-O1 and -Ofast). It includes detailed steps and explanations to ensure clarity.  

**Steps to Complete the Task**  

1.Write a Simple C Program  

2.The following program calculates the swaping of two numbers:  

3.Compile Using RISC-V GCC

4.Compile with -O1 Optimization.

*Use the following command to compile the program with the -O1 optimization flag:*
```sh
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o swift.o swift.c
```
**Disassemble Object Files to View Assembly Code(in new terminal)**
*Generate Dump for -O1 Optimization*
```sh
riscv64-unknown-elf-objdump -d swift.o
```
*Minimize the assembly by using following code:*
```sh
riscv64-unknown-elf-objdump -d swift.o | less
```

**Run SPIKE Simulation**
*Run a compiled RISC-V program on the SPIKE simulator in non-debug mode.*
```sh
spike pk swift.o
```
*Invoke the debug mode of the SPIKE RISC-V simulator.*
```sh
spike -d pk swift.o
```

**Compile with -Ofast Optimization.**
*Use the following command to compile the program with the -Ofast optimization flag:*
```sh
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o swift.o swift.c
```
**Disassemble Object Files to View Assembly Code(in new terminal)**
*Generate Dump for -Ofast Optimization*
```sh
riscv64-unknown-elf-objdump -d swift.o
```
*Minimize the assembly by using following code:*
```sh
riscv64-unknown-elf-objdump -d swift.o | less
```

**Run SPIKE Simulation**
*Run -O1 Binary in SPIKE*
```sh
spike pk swift.o
```
*Invoke the debug mode of the SPIKE RISC-V simulator*
```sh
spike -d pk swift.o
```
![Image](https://github.com/user-attachments/assets/83e58b8d-b346-4ce5-8a97-dd86cfa8c9b4)

![Image](https://github.com/user-attachments/assets/4cd88e69-80ed-4175-ba3b-a869cd7ca414)

![Image](https://github.com/user-attachments/assets/8aff14f7-847a-4cbd-a017-a47433256271)

![Image](https://github.com/user-attachments/assets/4d050220-0378-42ec-9bd3-2173acbabb61)

![Image](https://github.com/user-attachments/assets/0b671f41-e0d2-4c88-84e9-7a7597d62226)

![Image](https://github.com/user-attachments/assets/30c0f6dd-ead9-4105-b8b9-b96c81610f81)

![Image](https://github.com/user-attachments/assets/3ddeefdf-dc56-4a4e-9f86-1724a60e3827)

![Image](https://github.com/user-attachments/assets/db2f3484-0d02-47e2-8c87-a9b91f922b4c)

![Image](https://github.com/user-attachments/assets/85ec7274-b5e1-4340-b102-0f3b895f29a3)

![Image](https://github.com/user-attachments/assets/cc546fbb-f498-44f6-9c35-281bf3a587c3)

![Image](https://github.com/user-attachments/assets/657ba0c1-f12c-46f9-9934-74200b6fd62e)

![Image](https://github.com/user-attachments/assets/a61f1319-908e-4a53-a7a3-9ade2f23380d)


**After(spike -d pk swift.o) Observe the Instructions:**

1)After loading, SPIKE initializes and displays the Program Counter (PC) and Stack Pointer (SP).

2)Press Enter repeatedly to step through the execution.

3)Each press displays the next instruction executed by the program.

4)The displayed instructions directly correspond to the C code of the main program, providing insights into the program's execution flow.
**Explanation of Key Commands and Options:**

1. spike:RISC-V simulator that runs RISC-V programs on a virtual machine.

2. pk:Proxy kernel that acts as a minimal runtime environment for RISC-V programs, handling system calls like I/O and memory management.

3. swift.o:The compiled RISC-V binary of your program (created using a RISC-V GCC compiler).

4. -d (for debugging):Debugging mode in SPIKE, allows stepping through the instructions and inspecting the program's behavior.

5. riscv64-unknown-elf-gcc:RISC-V GCC compiler used to compile the C program into a RISC-V object file (.o).

6. -O1, -Ofast:Compiler optimization flags:
      a.-O1: Basic optimizations for performance.
      b.-Ofast: Aggressive optimizations for maximum speed.

7. riscv64-unknown-elf-objdump:Disassembles RISC-V binaries to examine assembly code.

These tools together enable compiling, running, and debugging RISC-V programs on a simulated environment.

</details>

---
