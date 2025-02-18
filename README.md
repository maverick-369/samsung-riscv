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

<details>
<summary> <b>Task 1</b><br>The task requires a detailed review of lab videos focused on C programming and the RISC-V architecture to develop a deep understanding of both topics. Following this, you are expected to compile C code using two distinct compilers: the GCC compiler and the RISC-V compiler. This exercise will demonstrate your comprehension of the compilation process, allowing you to observe and compare how each compiler converts the C code into machine code. You will analyze the differences and nuances in the compilation processes for different processor architectures, emphasizing the specificities of each..</summary> 
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
</details>


---
<details>
<summary> <b>Task 2</b><br>The task involves reviewing both C-based and RISC-V-based lab videos to understand the nuances of compiling C code for different architectures. Afterward, you are required to execute the process of compiling the C code using two distinct tools: the GCC compiler and the RISC-V compiler simulator. This will allow you to demonstrate your ability to work with both compilers, providing insights into how the C code is processed and converted into machine-readable code for each specific architecture.</summary> 
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
<details>
<summary><b>Task 3</b><br>The goal is to analyze and categorize each of the provided instructions based on their type, whether it be R-type, I-type, or J-type, and then translate them into their respective 32-bit machine instruction codes. These instruction codes should be represented in the appropriate format, ensuring that each instruction is properly encoded according to the specific structure and opcode requirements of the given architecture. The result should provide a detailed mapping of the instructions to their corresponding binary code representations.</summary>

# Understanding RISC-V and Its Instruction Formats

## What is RISC-V?
RISC-V is an open-source Instruction Set Architecture (ISA) that enables developers to design processors tailored to specific applications. Based on Reduced Instruction Set Computer (RISC) principles, RISC-V represents the fifth generation of processors built on this concept. Its open and free nature means developers can utilize RISC-V without purchasing licenses, making it a compelling alternative to proprietary processor technologies.

## Instruction Formats in RISC-V
The instruction format of a processor defines how machine language instructions are structured for execution. These instructions are composed of binary data (0s and 1s), each segment providing details about data location and operations to be performed. In RISC-V, there are six primary instruction formats:

1. **R-format**
2. **I-format**
3. **S-format**
4. **B-format**
5. **U-format**
6. **J-format**

---

### 1. R-type Instruction
R-type (Register-type) instructions operate on registers rather than memory locations. These are used for arithmetic and logical operations. Each instruction is 32 bits and divided into six fields:

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| func3      | 3 bits| Specifies the type of operation       |
| rs1        | 5 bits| First source register                 |
| rs2        | 5 bits| Second source register                |
| func7      | 7 bits| Additional operation specification    |

#### Example: ADD r9, r2, r5
- **Operation:** Adds values in registers r2 and r5, storing the result in r9.
- **Field Breakdown:**

  - Opcode: `0110011`
  - rd (Destination): `r9` -> `01001`
  - rs1 (Source 1): `r2` -> `00010`
  - rs2 (Source 2): `r5` -> `00101`
  - func3: `000`
  - func7: `0000000`
- **32-bit Instruction:** `0000000_00101_00010_000_01001_0110011`


#### Example: XOR r10, r1, r4
- **Operation:** XOR operation between r1 and r4, result in r10.
- **Field Breakdown:**

  - Opcode: `0110011`
  - rd (Destination): `r10` -> `01010`
  - rs1 (Source 1): `r1` -> `00001`
  - rs2 (Source 2): `r4` -> `00100`
  - func3: `100`
  - func7: `0000000`
- **32-bit Instruction:** `0000000_00100_00001_100_01010_0110011`


#### Example: SLT r11, r2, r4
- **Operation:** Sets r11 to 1 if r2 < r4; otherwise, sets r11 to 0.
- **Field Breakdown:**

  - Opcode: `0110011`
  - rd (Destination): `r11` -> `01011`
  - rs1 (Source 1): `r2` -> `00010`
  - rs2 (Source 2): `r4` -> `00100`
  - func3: `010`
  - func7: `0000000`
- **32-bit Instruction:** `0000000_00100_00010_010_01011_0110011`


### 2. I-type Instruction
I-type (Immediate-type) instructions use a register and an immediate (constant) value. These are typically used for load and immediate operations.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| func3      | 3 bits| Specifies the type of operation       |
| rs1        | 5 bits| Source register                       |
| imm[11:0]  | 12 bits| Immediate value                      |

#### Example: ADDI r12, r4, 5
- **Operation:** Adds immediate value 5 to the value in r4 and stores it in r12.
- **Field Breakdown:**
  - Opcode: `0010011`
  - rd (Destination): `r12` -> `01100`
  - rs1 (Source): `r4` -> `00100`
  - imm[11:0] (Immediate): `000000000101`
  - func3: `000`
- **32-bit Instruction:** `000000000101_00100_000_01100_0010011`


### 3. S-type Instruction
S-type (Store-type) instructions store register values into memory locations.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rs1        | 5 bits| Base address register                 |
| rs2        | 5 bits| Source register                       |
| imm[11:5]  | 7 bits| Upper immediate value                  |
| imm[4:0]   | 5 bits| Lower immediate value                  |
| func3      | 3 bits| Specifies the type of operation       |

#### Example: SW r3, 2(r1)
- **Operation:** Stores the value in r3 into the memory at the address `r1 + 2`.
- **Field Breakdown:**
  - Opcode: `0100011`
  - rs1 (Base Address): `r1` -> `00001`
  - rs2 (Source): `r3` -> `00011`
  - imm[11:5] (Upper Immediate): `0000000`
  - imm[4:0] (Lower Immediate): `00010`
  - func3: `010`
- **32-bit Instruction:** `0000000_00011_00001_010_00010_0100011`


### 4. B-type Instruction
B-type (Branch-type) instructions handle branching based on conditions.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rs1        | 5 bits| Source register 1                      |
| rs2        | 5 bits| Source register 2                      |
| imm[12|10:5|4:1|11] | 13 bits| Branch offset                      |
| func3      | 3 bits| Specifies the condition for branching |

#### Example: BNE r0, r1, 20
- **Operation:** Branches to the address `PC + 20` if r0 is not equal to r1.
- **Field Breakdown:**
  - Opcode: `1100011`
  - rs1: `r0` -> `00000`
  - rs2: `r1` -> `00001`
  - imm[12|10:5|4:1|11]: `0000010100`
  - func3: `001`
- **32-bit Instruction:** `0000000_00001_00000_001_10100_1100011`

#### Example: BEQ r0, r0, 15
- **Operation:** Branches to the address `PC + 15` if r0 equals r0 (always true).
- **Field Breakdown:**
  - Opcode: `1100011`
  - rs1: `r0` -> `00000`
  - rs2: `r0` -> `00000`
  - imm[12|10:5|4:1|11]: `000001111`
  - func3: `000`
- **32-bit Instruction:** `0000000_00000_00000_000_01111_1100011`


### 5. U-type Instruction
U-type (Upper Immediate) instructions load immediate data into the destination register.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| imm[31:12] | 20 bits| Upper immediate value                  |



### 6. J-type Instruction
J-type (Jump-type) instructions implement jump operations, often used for loops.

#### Structure:

| Field Name | Size  | Description                            |
|------------|-------|----------------------------------------|
| Opcode     | 7 bits| Determines the instruction type        |
| rd         | 5 bits| Destination register                  |
| imm[20|10:1|11|19:12] | 20 bits| Jump offset                        |


This repository contains a list of 15 unique RISC-V instructions extracted from the assembly code along with their corresponding 32-bit instruction codes. These instructions cover different instruction formats, such as **U-type**, **I-type**, **J-type**, **B-type**, and **R-type**.


# RISC-V Instructions

This README contains a table of 23 unique RISC-V instructions, their machine codes, opcodes, formats, and instruction binaries for my assembly codes.

| Instruction                | Opcode  | Format | Machine Code | Instruction Binary                          |
|----------------------------|---------|--------|--------------|---------------------------------------------|
| addi sp, sp, -128           | 0010011 | I-type | 0xf8010113  | 11111111111100000011000000010011            |
| sd ra, 120(sp)              | 0100011 | S-type | 0x06813823  | 00000000001000010001000100010011            |
| li a5, 0                    | 0010011 | I-type | 0x00000793  | 00000000000010100000011110010011            |          
| mv a0, a5                  | 0110011 | R-type | 0x00078513   | 00000000000001110000000010010011            |
| mv a1, a5                  | 0110011 | R-type | 0x00078593   | 00000000000001110000101000010011            |
| lui a5, 0x21               | 0110111 | U-type | 0x0002b7b7   | 00000000000000100010011110110111            |
| jal ra, 1117c              | 1101111 | J-type | 0x7ad000ef   | 01111010110100000000000001110111            |
| subw a5, a4, a5            | 0110011 | R-type | 0x40f707bb   | 00000000111101000000000010010011            |
| and a5, a4, a5             | 0110011 | R-type | 0x00f777b3   | 00000000011101000000000010010011            |
| bne a4, a5, 103c8          | 1100011 | B-type | 0x02f71063   | 00000000001011110001000001100011            |
| beq a4, a5, 103f8          | 1100011 | B-type | 0x02f70063   | 00000000001011110001000001100011            |
| bge a4, a5, 10428          | 1100011 | B-type | 0x02f75063   | 00000000001011110001000001100011            |
| blt a4, a5, 10458          | 1100011 | B-type | 0x02f74063   | 00000000001011110001000001100011            |
| j 10490                    | 1101111 | J-type | 0x0340006f   | 00000011001100000000000001101111            |
| addw a5, a4, a5            | 0110011 | R-type | 0x00f707bb   | 00000000011101000000000010010011            |
| beqz a5, 104e4             | 1100011 | B-type | 0x02078863   | 00000000001000110000000001100011            |


![Image](https://github.com/user-attachments/assets/fd53b375-d8b2-4b3d-95f3-5567da495eec)

![Image](https://github.com/user-attachments/assets/08114dee-4678-4d6f-a217-057fe13e7e04)

![Image](https://github.com/user-attachments/assets/3e3d9f25-92ef-4738-a428-c31aa00db8ca)

![Image](https://github.com/user-attachments/assets/34773494-2247-4622-8ec2-5ce267ecf60d)

![Image](https://github.com/user-attachments/assets/8c81aa94-75c8-4d0d-9901-9dd55cc10dc1)

![Image](https://github.com/user-attachments/assets/a0be24fa-e9d1-49e5-b7bb-8b98d99166cf)

![Image](https://github.com/user-attachments/assets/3f3a08b6-e5f4-41fc-a55c-49f593b80ec2)

![Image](https://github.com/user-attachments/assets/16cb4f2c-4a8e-4e0e-9fb7-0ff7fa438a0d)

![Image](https://github.com/user-attachments/assets/ee8f3d56-7aab-4e0c-bcb4-824943c6d526)

![Image](https://github.com/user-attachments/assets/4efc915b-1ba1-4e24-ae30-93e5f63a3167)

![Image](https://github.com/user-attachments/assets/8dcda5e0-3de0-49c2-bb84-2f560debdfc0)

![Image](https://github.com/user-attachments/assets/58a1373c-53a4-48ee-8a5a-c0c6ba1f19e9)

![Image](https://github.com/user-attachments/assets/2366e85a-69d8-421d-b2ed-e2c21bbde41a)

![Image](https://github.com/user-attachments/assets/3b7077d0-b829-487d-8f0f-05c48e9c464d)

![Image](https://github.com/user-attachments/assets/8f7a7a4c-9d4b-4507-8aa9-ea13a997181f)

</details>

---
<details>
<summary> <b>Task 4</b><br>This task involves simulating the RISC-V Core using the provided Verilog netlist and testbench. You will set up a simulation environment using tools like Icarus Verilog and GTKWave, run the simulation to verify the functional correctness of the core, and analyze output signals. Waveform snapshots of the executed instructions must be captured and uploaded to your GitHub repository along with a brief description, demonstrating your understanding of RISC-V functional simulation and verification.</summary> 
<br>

## 2. BLOCK DIAGRAM OF RISC-V RV32I
![image](https://user-images.githubusercontent.com/110079631/181293948-beb8622c-7696-4b06-b6c9-eeab9b8ab9d3.png)

## 3. INSTRUCTION SET OF RISC-V RV32I
![image](https://user-images.githubusercontent.com/110079631/181298133-60269bc2-01da-4b5c-8b42-69057b8dc15c.png)

# RISC-V Core Functional Simulation 
## 4. FUNCTIONAL SIMULATION

### 4.1 About iverilog and gtkwave
- Icarus Verilog is an implementation of the Verilog hardware description language.
- GTKWave is a fully featured GTK+ v1. 2 based wave viewer for Unix and Win32 which reads Ver Structural Verilog Compiler generated AET files as well as standard Verilog VCD/EVCD files and allows their viewing.

### 4.2 Installing iverilog and gtkwave

- **For Ubuntu**

 Open your terminal and type the following to install iverilog and GTKWave
 ```
 $   sudo apt get update
 $   sudo apt get install iverilog gtkwave
 ```

- **To clone the repository and download the netlist files for simulation , enter the following commands in your terminal.**

 ```
 $ git clone https://github.com/vinayrayapati/iiitb_rv32i
 $ cd iiitb_rv32i
 ```
- **To simulate and run the verilog code , enter the following commands in your terminal.**

```
$ iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
$ ./iiitb_rv32i
```
- **To see the output waveform in gtkwave, enter the following commands in your terminal.**

`$ gtkwave iiitb_rv32i.vcd`

### 4.3 The output waveform

 The output waveform showing the instructions performed in a 5-stage pipelined architecture.

## Instructions and Pipeline Details  

Below are the 15 instructions and their corresponding pipeline details:  

---

### 1. `add r6, r2, r1`  
**Purpose:** Add `r2` and `r1`, store the result in `r6`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `add` instruction.
  - IF_ID_NPC: Holds the next program counter value.
Decode Stage:
  - ID_EX_IR: Ensures the instruction is decoded.
  - ID_EX_A: Value of register `r2`.
  - ID_EX_B: Value of register `r1`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r2 + r1`.
  - EX_MEM_IR: Holds the `add` instruction.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r6`.
```

---

### 2. `sub r7, r1, r2`  
**Purpose:** Subtract `r2` from `r1`, store the result in `r7`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `sub` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_B: Value of register `r2`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 - r2`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r7`.
```

---

### 3. `and r8, r1, r3`  
**Purpose:** Perform bitwise AND between `r1` and `r3`, store the result in `r8`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `and` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_B: Value of register `r3`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 & r3`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r8`.
```

---

### 4. `or r9, r2, r5`  
**Purpose:** Perform bitwise OR between `r2` and `r5`, store the result in `r9`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `or` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r2`.
  - ID_EX_B: Value of register `r5`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r2 | r5`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r9`.
```

---

### 5. `xor r10, r1, r4`  
**Purpose:** Perform bitwise XOR between `r1` and `r4`, store the result in `r10`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `xor` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_B: Value of register `r4`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 ^ r4`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r10`.
```

---

### 6. `addi r12, r4, 5`  
**Purpose:** Add immediate value `5` to `r4`, store the result in `r12`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `addi` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r4`.
  - ID_EX_IMMEDIATE: Immediate value `5`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r4 + 5`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r12`.
```

---
### 7. `beq r0, r0, 15`  
**Purpose:** Branch to PC + 15 if `r0 == r0` (always true).  
```markdown
Decode Stage:
  - BR_EN: High (branch taken).
Fetch Stage:
  - IF_ID_NPC: Updated program counter.
```
---

### 8. `bne r0, r1, 20`  
**Purpose:** Branch to PC + 20 if `r0 != r1`.  
```markdown
Decode Stage:
  - BR_EN: High if `r0 != r1`.
Fetch Stage:
  - IF_ID_NPC: Updated program counter.
```
---

### 9. `sll r15, r1, r2 (2)`  
**Purpose:** Perform logical left shift of `r1` by 2 (specified in `r2`), store the result in `r15`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `sll` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r1`.
  - ID_EX_SHAMT: Immediate shift value `2`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r1 << 2`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r15`.
```

---

### 10. `slt r16, r14, r2 (2)`  
**Purpose:** Perform logical right shift of `r14` by 2 (specified in `r2`), store the result in `r16`.  
```markdown
Fetch Stage:
  - IF_ID_IR: Holds the `srl` instruction.
Decode Stage:
  - ID_EX_A: Value of register `r14`.
  - ID_EX_SHAMT: Immediate shift value `2`.
Execute Stage:
  - EX_MEM_ALUOUT: Result of `r14 >> 2`.
Write-Back Stage:
  - WB_OUT: Verifies the result is written to `r16`.
```


#### *Analysing the Output Waveform of various instructions*  
**```Instruction 1: ADD R6, R2, R1```**  

![add](https://github.com/user-attachments/assets/ec39b465-af2d-4b5d-84ea-b8f1c9109e23)

**```Instruction 2: SUB R7, R1, R2```**  
  
![sub](https://github.com/user-attachments/assets/bc726bd7-35a8-411e-8ef9-919e9ea9e52c)

**```Instruction 3: AND R8, R1, R3```**  

![and](https://github.com/user-attachments/assets/1086c263-7e29-469e-8212-30b91156fe8d)

**```Instruction 4: OR R9, R2, R5```**  

![or](https://github.com/user-attachments/assets/ca049aae-1152-4ccc-b07f-2cb6c02a6884)

**```Instruction 5: XOR R10, R1, R4```**  

![xor](https://github.com/user-attachments/assets/9cd66bcd-519f-498d-bd3d-7a8689282eff)

**```Instruction 6: ADDI R1, R2, R4```**  

![addi](https://github.com/user-attachments/assets/d5869caf-5472-4bad-bce8-2d99ad67d952)

**```Instruction 7: bne R12, R4, 5```**  

![bne](https://github.com/user-attachments/assets/83eb1278-42d6-474e-a03f-a9450ca7e42f)

**```Instruction 8: BEQ R0, R0, 15```**  
  
![beq](https://github.com/user-attachments/assets/db711a7a-0dc5-489d-89f0-3fa688bf8733)
 
**```Instruction 9:sll r3,r1,2```**

![sll](https://github.com/user-attachments/assets/eb883176-69df-44af-bcf8-3400bb85d274)
  
**```Instruction 10:slt r13,r1,2```**  

![slt](https://github.com/user-attachments/assets/d1dd6ff3-092d-4df7-b5bd-0fb4f997f9a2)


![5 Stage-instruction Pipeline](https://github.com/user-attachments/assets/17d17693-709b-47ba-98d0-0459acc548d7)

</details>

---

<details>
<summary> <b>Task 5</b><br>A fingerprint-based security system is an intelligent setup designed to control access using biometric authentication. The system utilizes a fingerprint sensor to scan and verify stored fingerprints. When a registered fingerprint is detected, the system activates a servo motor, providing access. Additionally, users can enroll new fingerprints, verify existing ones, or delete stored fingerprints using serial commands. If the fingerprint is not recognized, access is denied. This system is widely used in home security, restricted areas, biometric authentication, and access control systems.</summary> 
<br>

# Fingerprint-Based Access Control System using VSDSquadron Mini RISC-V Board

## Project Overview
This project involves the development of a fingerprint-based biometric access control system utilizing the VSDSquadron Mini RISC-V development board. The system enhances security by allowing access only to authorized individuals whose fingerprints are registered in the system. Upon successful fingerprint verification, a servo motor actuates to grant access, making it suitable for applications such as secure entry points in homes, banks, and other sensitive areas.

### Features: 
**Biometric Authentication**: Employs fingerprint recognition to ensure that only authorized users can gain access.
**VSDSquadron Mini Integration**: Leverages the capabilities of the VSDSquadron Mini RISC-V board for efficient processing and control.
**Servo Motor Control**: Activates a servo motor to physically grant or deny access based on fingerprint verification results.
**User-Friendly Interface**: Provides serial prompts for enrolling new fingerprints, verifying existing ones, and deleting stored fingerprints.
**Security Management**: Allows for easy management of fingerprint data, including enrollment and deletion of user fingerprints.

---

## Required Components

| Component                         | Quantity | Description                                               |
|-----------------------------------|----------|-----------------------------------------------------------|
| **VSDSquadron Mini RISC-V Development Board** | 1        | Serves as the central microcontroller unit.               |
| **Fingerprint Sensor Module**     | 1        | Captures and processes fingerprint data for authentication. |
| **Servo Motor**                   | 1        | Mechanically controls the locking mechanism upon successful authentication. |
| **Connecting Wires**              | -        | Establish electrical connections between components.      |
| **Power Supply**                  | 1        | Provides necessary power to the system.                   |


---

## Pin Connections

**Fingerprint Sensor to VSDSquadron Mini:**

- VCC to 3.3V
- GND to GND
- TX to PD6 (USART RX)
- RX to PD5 (USART TX)

**Servo Motor to VSDSquadron Mini:**

- VCC to 3.3V
- GND to GND
- Control Pin to PD4
---

# Breadboard connections

![Breadboard Connections](https://github.com/user-attachments/assets/eeb99885-a731-43d8-8c1f-ae70de6147e0)

---
**Working**
***System Initialization***: Upon powering up, the VSDSquadron Mini initializes the fingerprint sensor and sets the servo motor to its default position (locked state).

***Mode Selection***: Through the serial interface, users can select from three modes:

- ***Enroll (e)***: Register a new fingerprint by assigning it a unique ID.
- ***Verify (v)***: Authenticate a user by matching their fingerprint against the stored data.
- ***Delete (d)***: Remove a stored fingerprint from the system.

***Fingerprint Enrollment***
- The user is prompted to enter a unique ID for the new fingerprint.
- The system captures the fingerprint image, processes it, and stores the associated data under the provided ID.

***Fingerprint Verification***
- The user places their finger on the sensor.
- The system captures and processes the fingerprint image.
- If a match is found in the stored data, the servo motor actuates to unlock, granting access.
- After a predefined period, the servo returns to the locked position.

***Fingerprint Deletion***
- The user enters the ID of the fingerprint to be deleted.
- The system removes the corresponding fingerprint data from its memory.
- This setup provides a secure and efficient method of access control, leveraging biometric authentication to ensure that only authorized individuals can gain entry.
- The integration of the VSDSquadron Mini RISC-V board ensures reliable performance and ease of development.
- --
</details>


<details>
<summary> <b>Task 6</b> <br>A fingerprint-based security system is an advanced solution that manages access through biometric verification. The system employs a fingerprint sensor to capture and authenticate unique fingerprint data. Upon recognizing a registered fingerprint, it actuates a servo motor to grant access. Users can enroll new fingerprints, verify existing ones, or remove stored fingerprints via serial commands. If an unregistered fingerprint is presented, access is denied. This technology is extensively utilized in home security, restricted zones, biometric authentication, and access control systems.</summary> 
<br>

## Project Implementation

### Hardware Setup

#### Fingerprint Sensor Module
- **VCC Pin**: Connect to the 3.3V output on the VSDSquadron Mini board.
- **GND Pin**: Connect to the GND on the board.
- **TX Pin**: Connect to PD6 (USART RX) on the board.
- **RX Pin**: Connect to PD5 (USART TX) on the board.

#### Servo Motor
- **VCC Pin**: Connect to the 3.3V output on the board.
- **GND Pin**: Connect to the GND on the board.
- **Control Pin**: Connect to PD4 on the board.

Use connecting wires to establish all necessary connections securely.

### Software Development

#### Library Integration
- **Adafruit Fingerprint Sensor Library**: Include this library for fingerprint sensor management.
- **Servo Library**: Include this library to control the servo motor.

#### Fingerprint Enrollment
- Develop functionality to enroll new fingerprints, assigning each a unique ID between 1 and 127.
- Ensure the system captures and stores fingerprint data accurately for future verification.

#### Fingerprint Verification
- Implement a routine to read fingerprints and compare them against stored data.
- Upon successful verification, trigger the servo motor to unlock or grant access.

#### Fingerprint Deletion
- Provide a mechanism to delete specific fingerprint IDs from the system as needed.

### Compilation & Upload

- Use a **RISC-V compatible toolchain** to compile the firmware.
- Upload the compiled code to the **VSDSquadron Mini RISC-V Development Board** via the appropriate interface.

### Testing & Debugging

#### Enrollment Testing
- Test the fingerprint enrollment process with multiple users to ensure reliability.

#### Verification Testing
- Verify that only enrolled fingerprints grant access and that the servo motor responds appropriately.

#### Deletion Testing
- Confirm that deleted fingerprints no longer grant access.

#### System Robustness
- Test the system under various environmental conditions to ensure consistent performance.

## Expected Output

### Access Granted
- When a registered fingerprint is scanned, the system verifies the fingerprint and activates the servo motor to unlock or grant access.
- The servo motor moves to the designated position, allowing entry.

### Access Denied
- If an unregistered fingerprint is scanned, the system denies access, and the servo motor remains in the locked position.

### Enrollment Confirmation
- Successfully enrolled fingerprints are stored with unique IDs, and the system provides confirmation messages upon successful enrollment.

### Deletion Confirmation
- Successfully deleted fingerprints are removed from the system, and the system provides confirmation messages upon successful deletion.

## Conclusion

This implementation provides a secure and efficient biometric access control system, enhancing security for various applications by utilizing fingerprint authentication and mechanical actuation through a servo motor.

---

## Code Implementation  
```c
#include <ch32v00x.h>
#include <debug.h>


#define SERVO_PIN 9
#define BAUD_RATE 57600

// Function prototypes
void setup();
void loop();
void enrollFingerprint();
void verifyFingerprint();
void deleteFingerprint();
uint8_t readNumber();
uint8_t getFingerprintEnroll(uint8_t id);

Servo myServo;  // Create a Servo object

int main() {
    setup();
    while (1) {
        loop();
    }
    return 0;
}

void setup() {
    UART1_Init(BAUD_RATE); // Initialize UART instead of Serial
    Fingerprint_Init();  // Initialize the fingerprint module
    myServo.attach(SERVO_PIN);  // Initialize the servo motor
    myServo.write(0); // Set servo to initial position
    printf("\nFingerprint Sensor Management Initialized\n");
}

void loop() {
    printf("Select mode: (e)nroll, (v)erify, (d)elete\n");
    char mode = getchar();
    getchar(); // Consume newline character
    switch (mode) {
        case 'e':
            enrollFingerprint();
            break;
        case 'v':
            verifyFingerprint();
            break;
        case 'd':
            deleteFingerprint();
            break;
        default:
            printf("Invalid mode! Please select (e), (v), or (d).\n");
    }
}

void enrollFingerprint() {
    printf("Enter ID (1-127): ");
    uint8_t id = readNumber();
    if (id == 0) return;
    printf("Enrolling ID #%d\n", id);
    while (!getFingerprintEnroll(id));
}

uint8_t getFingerprintEnroll(uint8_t id) {
    printf("Waiting for valid finger to enroll as #%d\n", id);
    if (Fingerprint_CaptureImage() != 0) {
        printf("Error capturing image\n");
        return 0;
    }
    if (Fingerprint_ConvertImage() != 0) {
        printf("Error converting image\n");
        return 0;
    }
    if (Fingerprint_StoreTemplate(id) != 0) {
        printf("Error storing template\n");
        return 0;
    }
    printf("Fingerprint enrolled successfully!\n");
    return 1;
}

void verifyFingerprint() {
    printf("Place your finger on the sensor\n");
    if (Fingerprint_Search() == 1) {
        printf("Fingerprint verified! Activating servo.\n");
        myServo.write(90);  // Move servo to 90 degrees (or adjust as needed)
        delay(1000);         // Wait for 1 second
        myServo.write(0);   // Return servo to initial position
    } else {
        printf("Fingerprint not recognized.\n");
    }
}

void deleteFingerprint() {
    printf("Enter ID to delete: ");
    uint8_t id = readNumber();
    if (Fingerprint_Delete(id) == 0) {
        printf("Fingerprint ID %d deleted.\n", id);
    } else {
        printf("Error deleting fingerprint.\n");
    }
}

uint8_t readNumber() {
    int num;
    scanf("%d", &num);
    return (uint8_t)num;
}
```
# Applications of Fingerprint-Based Security Systems

Fingerprint-based security systems offer a secure and efficient method of access control. These systems utilize unique biometric identifiers to ensure that only authorized individuals are granted access to restricted areas. Below are some of the key applications of fingerprint authentication technology.

## Applications

### Corporate Offices
Implementing fingerprint-based security systems in corporate environments ensures that only authorized personnel gain access to sensitive areas, thereby enhancing overall security.  


### Healthcare Facilities
Utilizing biometric authentication in healthcare settings safeguards patient information and restricts access to controlled substances, ensuring that only qualified staff members can access sensitive areas.  


### Educational Institutions
Schools and universities can employ fingerprint recognition to monitor student and staff entry, enhancing campus security and ensuring that only authorized individuals access specific facilities.  


### Retail Outlets
Retailers can integrate biometric systems to prevent shoplifting and employee theft by restricting access to inventory and cash handling areas to authorized personnel only.  


### Mobile Device Security
Fingerprint recognition is widely used in smartphones and tablets, allowing users to unlock devices, authenticate payments, and secure applications with a simple touch, enhancing user convenience and security.  

### Building Access Control
Biometric door lock systems provide a high level of security by granting or denying access based on fingerprint data, ensuring that only authorized individuals can enter restricted areas.  


## Conclusion
The integration of fingerprint-based security systems offers a robust and efficient method for access control across various sectors. By leveraging unique biometric identifiers, these systems enhance security measures, reduce reliance on traditional keys or passwords, and provide a seamless user experience. As technology advances, the adoption of biometric authentication continues to expand, underscoring its significance in modern security infrastructures.
</details>
---
