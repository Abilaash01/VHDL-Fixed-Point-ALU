# Fixed-Point Arithmetic Units in VHDL

This repository contains VHDL implementations of **fixed-point arithmetic units** designed and tested on the DE-2 FPGA board. The project includes a **4-bit adder/subtractor** and a **signed multiplier**. The design demonstrates structural VHDL coding, RTL-level modeling, and synthesis for FPGA deployment.

---

## Table of Contents
- [Overview](#overview)
- [Number Representations](#number-representations)
- [Adder/Subtractor Design](#addersubtractor-design)
- [Multiplier Design](#multiplier-design)
- [Circuit Diagrams](#circuit-diagrams)
- [Simulation](#simulation)
- [Directory Structure](#directory-structure)
- [Usage](#usage)
- [References](#references)

---

## Overview
The goal of this project is to implement **fixed-point arithmetic operations** for signed 4-bit numbers. Completed modules include:
- 1-bit half adder and full adder
- 4-bit ripple-carry adder/subtractor
- 4-bit signed multiplier (shift-and-add method)
- Status outputs for arithmetic operations: CarryOut, ZeroOut, OverflowOut

The project emphasizes **structural VHDL design** with **synthesizable logic blocks**.

---

## Number Representations
All operations use **2’s complement representation** for signed numbers, which allows:
- Easy addition and subtraction
- Unique zero representation
- Direct hardware mapping for multiplication

---

## Adder/Subtractor Design

### 1-Bit Full Adder
The full adder is the fundamental building block for multi-bit addition.

**Truth Table (1-bit Full Adder)**  
![1-Bit Full Adder Truth Table](images/full_adder_truth_table.png)

**Logic Diagram (1-bit Full Adder)**  
![1-Bit Full Adder Logic Diagram]([images/full_adder_logic.png](https://github.com/Abilaash01/VHDL-Fixed-Point-ALU/blob/main/one-bit-adder.png))

### 4-Bit Ripple Carry Adder/Subtractor
Cascading 1-bit full adders forms a **ripple-carry adder**. Subtraction is implemented using 2’s complement:

