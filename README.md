# 4-Bit ALU in Verilog

This project implements a simple 4-bit Arithmetic Logic Unit (ALU) using Verilog HDL. The ALU supports basic arithmetic and comparison operations based on a 3-bit opcode and outputs an 8-bit result along with status flags.

## ⚙️ Features

- **Inputs**: Two 4-bit operands (`A`, `B`)
- **Opcode-controlled Operations**:
  - `000`: Addition
  - `001`: Subtraction
  - `010`: Multiplication
  - `011`: Division (if `B ≠ 0`)
  - `100`: A < B comparison
  - `101`: A > B comparison
- **Outputs**:
  - `Result`: 8-bit output of operation
  - `Zero`: Set if result is 0
  - `Carry`: Set for overflow during addition

## 🧮 Opcode Table

| Opcode | Operation      | Description                |
|--------|----------------|----------------------------|
| 000    | `A + B`        | Adds inputs                |
| 001    | `A - B`        | Subtracts B from A         |
| 010    | `A * B`        | Multiplies A and B         |
| 011    | `A / B`        | Divides A by B (if B ≠ 0)  |
| 100    | `A < B`        | Comparison result (1 or 0) |
| 101    | `A > B`        | Comparison result (1 or 0) |

## 🧾 Output Flags

- **Zero**: Set to 1 if result is 0
- **Carry**: Set to 1 only for specific overflow condition in addition
