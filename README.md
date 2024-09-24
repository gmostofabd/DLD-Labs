# 🟢 **Digital Logic Design: Basic Experiments**

Welcome to the **Digital Logic Design** repository! This collection contains experiments focusing on the basics of digital logic gates using common ICs, equivalent circuits, and practical implementation using a breadboard.

<p align="center">
 <img src="https://github.com/user-attachments/assets/08ca6583-971a-4da3-be36-7a3aeebf28e2" alt="AT89C51 Dot Matrix Circuit" width="50%">
</p>

---


## 🌟 **Contents**

1. [Introduction to Digital Logic](#-introduction-to-digital-logic)
2. [Basic Logic Gates](#-basic-logic-gates)
3. [Universal Gates](#-universal-gates)
4. [Combinational Circuits](#-combinational-circuits)
   - [Half-Adder](#half-adder)
5. [Sequential Circuits](#-sequential-circuits)
   - [D Flip-Flop](#d-flip-flop)
6. [Common ICs: 74HC Series](#-common-ics-74hc-series)
7. [Equivalent Circuits for Basic Gates](#-equivalent-circuits-for-basic-gates)
8. [Breadboard Setup and Requirements](#-breadboard-setup-and-requirements)
9. [Boolean Algebra and Simplification](#-boolean-algebra-and-simplification)
10. [Getting Started](#-getting-started)
11. [License](#-license)
12. [Conclusion](#-conclusion)

---

## 🔵 **Introduction to Digital Logic**

Digital logic is the backbone of modern electronics. This repository is designed to give hands-on experience with **logic gates**, their IC implementations, and simple circuits using diodes and transistors.

---

## 🔵 **Basic Logic Gates**

### Logic Gate Symbols & Truth Tables

<div align="center">

| **Gate**   | **IC**   | **Symbol** | **Input A** | **Input B** | **Output** |
|------------|----------|------------|-------------|-------------|------------|
| **AND**    | 74HC08   | ![AND Gate](https://via.placeholder.com/40x40?text=AND) | 0           | 0           | 0          |
|            |          |            | 0           | 1           | 0          |
|            |          |            | 1           | 0           | 0          |
|            |          |            | 1           | 1           | 1          |
| **OR**     | 74HC32   | ![OR Gate](https://via.placeholder.com/40x40?text=OR) | 0           | 0           | 0          |
|            |          |            | 0           | 1           | 1          |
|            |          |            | 1           | 0           | 1          |
|            |          |            | 1           | 1           | 1          |
| **NAND**   | 74HC00   | ![NAND Gate](https://via.placeholder.com/40x40?text=NAND) | 0           | 0           | 1          |
|            |          |            | 0           | 1           | 1          |
|            |          |            | 1           | 0           | 1          |
|            |          |            | 1           | 1           | 0          |
| **NOR**    | 74HC02   | ![NOR Gate](https://via.placeholder.com/40x40?text=NOR) | 0           | 0           | 1          |
|            |          |            | 0           | 1           | 0          |
|            |          |            | 1           | 0           | 0          |
|            |          |            | 1           | 1           | 0          |
| **XOR**    | 74HC86   | ![XOR Gate](https://via.placeholder.com/40x40?text=XOR) | 0           | 0           | 0          |
|            |          |            | 0           | 1           | 1          |
|            |          |            | 1           | 0           | 1          |
|            |          |            | 1           | 1           | 0          |
| **XNOR**   | 74HC66   | ![XNOR Gate](https://via.placeholder.com/40x40?text=XNOR) | 0           | 0           | 1          |
|            |          |            | 0           | 1           | 0          |
|            |          |            | 1           | 0           | 0          |
|            |          |            | 1           | 1           | 1          |

</div>

---

## 🟡 **Universal Gates**

<div align="center">

| **Gate**   | **IC**        | **Input A** | **Input B** | **Output** |
|------------|---------------|-------------|-------------|------------|
| **NAND**   | 74HC00       | 0           | 0           | 1          |
|            |               | 0           | 1           | 1          |
|            |               | 1           | 0           | 1          |
|            |               | 1           | 1           | 0          |
| **NOR**    | 74HC02       | 0           | 0           | 1          |
|            |               | 0           | 1           | 0          |
|            |               | 1           | 0           | 0          |
|            |               | 1           | 1           | 0          |

</div>

---

## 🟠 **Combinational Circuits**

This section covers combinational circuits, which depend only on the current inputs. **Half-Adders** and **Multiplexers** are key topics discussed here.

### Half-Adder

A **half-adder** adds two single-bit numbers and outputs a **sum** and a **carry**.

#### Circuit Diagram
```
          A ----|\
                 |  \
                 |   |---- Sum
          B ----|   /
                     |/
                    |---- Carry
```

#### Truth Table
<div align="center">

| **Input A** | **Input B** | **Sum** | **Carry** |
|-------------|-------------|---------|-----------|
|      0      |      0      |    0    |     0     |
|      0      |      1      |    1    |     0     |
|      1      |      0      |    1    |     0     |
|      1      |      1      |    0    |     1     |

</div>

---

## 🟡 **Sequential Circuits**

Sequential circuits rely on **memory** and include devices such as flip-flops and counters. This section introduces **basic flip-flops**, which form the building blocks of memory elements in digital systems.

### D Flip-Flop

A **D flip-flop** captures the value of the input (D) on the rising edge of the clock signal and holds it until the next clock edge.

#### Circuit Diagram
```
         D ----|>o----|\
                 |      |  \
                 |      |   |---- Q (Output)
          Clock--|      |   |
                        |   |
                       ----  |
                       |  |  |
                       |__|__|
                         |
                         |
                        Q' (Inverted Output)
```

#### Truth Table
<div align="center">

| **Input D** | **Clock** | **Output Q** |
|-------------|-----------|--------------|
|      0      |     ↑     |      0       |
|      1      |     ↑     |      1       |

</div>

---

## 🟢 **Common ICs: 74HC Series**

<div align="center">
<p align="center">
  <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/7400.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/7402.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/7404.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/7408.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/7432.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/7486.png" alt="AT89C51 Dot Matrix Circuit" width="30%">
</p>
</div>


The **74HC** series is a family of **high-speed CMOS** logic ICs that operate on low power and have fast switching times. Below are some widely used ICs for implementing basic and universal gates:

- **74HC00**: Quad 2-input **NAND** Gate IC.
- **74HC02**: Quad 2-input **NOR** Gate IC.
- **74HC04**: Hex **Inverter** (NOT gate) IC.
- **74HC08**: Quad 2-input **AND** Gate IC.
- **74HC32**: Quad 2-input **OR** Gate IC.
- **74HC86**: Quad 2-input **XOR** Gate IC.

Each IC contains multiple gates (typically 4 or 6), making them convenient for building small circuits on breadboards.

---

## 🟠 **Equivalent Circuits for Basic Gates**

Digital logic gates can be constructed using **diodes** and **transistors**, demonstrating their working at a fundamental level.

### 1. AND Gate (Diode-Transistor Logic)
In this design, diodes and an NPN transistor are used. The diodes allow current only if both inputs are HIGH (1), and the transistor amplifies this signal, outputting a HIGH voltage.

**Equivalent Circuit:**
- Diodes D1 and D2 block current unless both inputs are HIGH.
- Transistor amplifies the signal to create a strong output.

### 2. OR Gate (Diode Logic)
The OR gate can be made using two diodes, where the anodes are connected to the inputs, and the cathode goes to the output. If any input is HIGH, current will flow to the output.

**Equivalent Circuit:**
- Diodes D

1 and D2 conduct if either input is HIGH, resulting in a HIGH output.

### 3. NOT Gate (Transistor)
A transistor can function as a NOT gate, where the input is connected to the base. When the input is HIGH, the transistor conducts, pulling the output LOW.

---

## 🟡 **Breadboard Setup and Requirements**
<div align="center">

<img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/apparatus.png" alt="AT89C51 Dot Matrix Circuit" width="80%">
</div>

---


To set up the experiments, you will need:

### **Components**
- Breadboard
- Power supply (5V)
- ICs (e.g., 74HC00, 74HC08)
- Resistors (typically 1kΩ)
- Diodes (for equivalent circuits)
- Connecting wires

### **Procedure**
1. Insert the IC into the breadboard.
2. Connect power and ground to the appropriate pins.
3. Build the circuits according to the diagrams provided.
4. Test the circuits using a multimeter or LEDs to visualize outputs.

---

## 🔵 **Boolean Algebra and Simplification**

Understanding **Boolean algebra** is crucial for optimizing digital circuits. It allows you to simplify complex logical expressions into simpler forms that require fewer gates, ultimately reducing cost and power consumption.

### Example
For the expression:  
\[ AB + A'C + BC \]

You can apply rules like **distribution** and **absorption** to simplify it.

---

## 🚀 **Getting Started**

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/digital-logic-design.git
```

Navigate to the project directory and start your experiments!


<p align="center">
  <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/74series_same_pinout.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> 
   
   <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/adder_ckt.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> 
   
   <img src="https://github.com/gmostofabd/DLD-Labs/blob/215c69e89e64c13edd98c043d76d2a2b52d5af83/Lab_04_Binary_Adders/images/adder_proteus1.png" alt="AT89C51 Dot Matrix Circuit" width="30%"> 
   
  
</p>
  
---

## 📝 **License**

This project is licensed under the MIT License. See the LICENSE file for details.

---

## 🏁 **Conclusion**

This repository aims to provide foundational knowledge and practical experience in digital logic design. By working with various logic gates and circuits, you can build a strong understanding of how digital systems function.

