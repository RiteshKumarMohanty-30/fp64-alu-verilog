# 🚀 64-bit Floating Point ALU (FP64) in Verilog

## 📌 Overview

This project implements a **resource-efficient 64-bit Floating Point Arithmetic Logic Unit (ALU)** compliant with the **IEEE 754 double-precision standard**.
It integrates both **arithmetic** and **logical operations** into a single modular design, optimized for **FPGA-based embedded and high-performance computing (HPC)** applications.

---

## ⚙️ Features

* ✅ IEEE 754 Double Precision (64-bit)
* ✅ Arithmetic Operations:

  * Addition
  * Subtraction
  * Multiplication
  * Division
* ✅ Logic Operations:

  * AND, OR, XOR, NOT
  * Shift Left (SHL), Shift Right (SHR)
* ✅ 4-bit Opcode Controlled ALU
* ✅ Fully Modular Verilog Design
* ✅ Parallel Architecture (Low Latency)

---

## 🧠 Architecture

The ALU consists of multiple modules working in parallel:

* `fp64_adder`
* `fp64_subtractor`
* `fp64_multiplier`
* `fp64_divider`
* `logic64`

A **multiplexer (MUX)** selects the final output based on the opcode.

```
Input A, B → Functional Units → MUX → Output
```

---

## 🔢 Opcode Table

| Opcode | Operation      |
| ------ | -------------- |
| 0000   | Addition       |
| 0001   | Subtraction    |
| 0010   | Multiplication |
| 0011   | Division       |
| 0100   | AND            |
| 0101   | NOT            |
| 0110   | OR             |
| 0111   | Shift Left     |
| 1000   | Shift Right    |
| 1001   | XOR            |

---

## 🛠️ Tools & Technologies

* **Language:** Verilog HDL
* **Simulation & Synthesis:** Xilinx Vivado
* **Design Methodology:** RTL (Register Transfer Level)

---

## 🧪 Simulation Results

* ✔ All arithmetic operations matched expected IEEE 754 outputs
* ✔ All logic operations verified successfully
* ✔ Tested using multiple input combinations and edge cases

---

## 📊 Resource Utilization (Vivado)

* LUT Usage: ~11%
* DSP Usage: ~3.75%
* I/O Utilization: ~93%

---

## 🚧 Challenges

* Mantissa alignment for large exponent differences
* Normalization after subtraction
* Handling 106-bit multiplication results
* Division latency due to long division algorithm

---

## 🔮 Future Improvements

* Pipeline architecture for higher speed
* Advanced division algorithms (Radix-8 / SRT)
* Fused Multiply-Add (FMA)
* IEEE 754 exception handling (NaN, overflow, etc.)
* Integration with RISC-V processor

---

## 📂 Project Structure

```
├── fp64_alu.v
├── fp64_adder.v
├── fp64_subtractor.v
├── fp64_multiplier.v
├── fp64_divider.v
├── logic64.v
├── fp64_alu_tb.v
└── README.md
```

---

## 👨‍💻 Authors

* Ritesh Kumar Mohanty
* Nilay Pandey
* Sambhav Pattnaik
* Chinmay Pandey

---

## 📜 License

This project is licensed under the **MIT License**.

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!
