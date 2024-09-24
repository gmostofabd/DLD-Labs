# 🟢 **Digital Logic Design: Basic Experiments**

Welcome to the **Digital Logic Design** repository! This collection contains experiments focusing on the basics of digital logic gates using 74 series ICs, equivalent circuits, and practical implementations using a breadboard.

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

Logic gates are the fundamental building blocks of digital circuits. These special electronic devices perform logical operations on binary inputs, which are represented by 0s and 1s. By following predefined rules, they generate a binary output, which can also be a 0 or 1.

Digital logic is the backbone of modern electronics. This repository is designed to give hands-on experience with **logic gates**, their IC implementations, and simple circuits using diodes and transistors.

---

## 🔵 **Basic Logic Gates**

Basic logic gates commonly used in digital systems include **AND**, **OR**, and **NOT** gates. These gates form the foundation for performing various operations and implementing complex digital circuits. The 74 series ICs are used for experiments with two-input gates.

### 1. **AND Gate (74HC08)**

- **Truth Table:**

  | **Input A** | **Input B** | **Output (Y)** |
  |-------------|-------------|----------------|
  | 0           | 0           | 0              |
  | 0           | 1           | 0              |
  | 1           | 0           | 0              |
  | 1           | 1           | 1              |

- **Symbol:**

  <div align="center">
    <img src="https://via.placeholder.com/40x40?text=AND" alt="AND Gate Symbol" />
  </div>

---

### 2. **OR Gate (74HC32)**

- **Truth Table:**

  | **Input A** | **Input B** | **Output (Y)** |
  |-------------|-------------|----------------|
  | 0           | 0           | 0              |
  | 0           | 1           | 1              |
  | 1           | 0           | 1              |
  | 1           | 1           | 1              |

- **Symbol:**

  <div align="center">
    <img src="https://via.placeholder.com/40x40?text=OR" alt="OR Gate Symbol" />
  </div>

---

### 3. **NOT Gate (74HC04)**

- **Truth Table:**

  | **Input A** | **Output (Y)** |
  |-------------|----------------|
  | 0           | 1              |
  | 1           | 0              |

- **Symbol:**

  <div align="center">
    <img src="https://via.placeholder.com/40x40?text=NOT" alt="NOT Gate Symbol" />
  </div>

---

## 🟡 **Universal Gates**

Universal gates like **NAND** and **NOR** can be used to build any other gate or circuit.

### 1. **NAND Gate (74HC00)**

- **Truth Table:**

  | **Input A** | **Input B** | **Output (Y)** |
  |-------------|-------------|----------------|
  | 0           | 0           | 1              |
  | 0           | 1           | 1              |
  | 1           | 0           | 1              |
  | 1           | 1           | 0              |

- **Symbol:**

  <div align="center">
    <img src="https://via.placeholder.com/40x40?text=NAND" alt="NAND Gate Symbol" />
  </div>

---

### 2. **NOR Gate (74HC02)**

- **Truth Table:**

  | **Input A** | **Input B** | **Output (Y)** |
  |-------------|-------------|----------------|
  | 0           | 0           | 1              |
  | 0           | 1           | 0              |
  | 1           | 0           | 0              |
  | 1           | 1           | 0              |

- **Symbol:**

  <div align="center">
    <img src="https://via.placeholder.com/40x40?text=NOR" alt="NOR Gate Symbol" />
  </div>

---

## 🟠 **Equivalent Circuits for Basic Gates**

Digital logic gates can be constructed using **diodes** and **transistors**, demonstrating their working at a fundamental level.

### 1. AND Gate (Diode-Transistor Logic)

- **Equivalent Circuit:**

  <div align="center">
    <img src="https://via.placeholder.com/100x100?text=AND+Circuit" alt="AND Gate Circuit" />
  </div>

- Diodes allow current only if both inputs are HIGH, and the transistor amplifies this signal to give a HIGH output.

---

### 2. OR Gate (Diode Logic)

- **Equivalent Circuit:**

  <div align="center">
    <img src="https://via.placeholder.com/100x100?text=OR+Circuit" alt="OR Gate Circuit" />
  </div>

- Diodes allow current to flow if any input is HIGH, producing a HIGH output.

---

## 🟠 **Combinational Circuits**

### Half-Adder

- A **half-adder** adds two single-bit numbers and outputs a **sum** and a **carry**.

- **Circuit Diagram:**

  ```
            A ----|\
                   |  \
                   |   |---- Sum
            B ----|   /
                   |/
                  |---- Carry
  ```

- **Truth Table:**

  | **Input A** | **Input B** | **Sum** | **Carry** |
  |-------------|-------------|---------|-----------|
  | 0           | 0           | 0       | 0         |
  | 0           | 1           | 1       | 0         |
  | 1           | 0           | 1       | 0         |
  | 1           | 1           | 0       | 1         |

---

## 🟡 **Sequential Circuits**

### D Flip-Flop

- A **D flip-flop** captures the value of the input (D) on the rising edge of the clock signal and holds it until the next clock edge.

- **Circuit Diagram:**

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

---

## 🟢 **Common ICs: 74HC Series**

The **74HC** series is a family of **high-speed CMOS** logic ICs that operate on low power and have fast switching times. Below are some widely used ICs for implementing basic and universal gates:

- **74HC00**: Quad 2-input **NAND** Gate IC.
- **74HC02**: Quad 2-input **NOR** Gate IC.
- **74HC04**: Hex **Inverter** (NOT gate) IC.
- **74HC08**: Quad 2-input **AND** Gate IC.
- **74HC32**: Quad 2-input **OR** Gate IC.

---

## 🟡 **Breadboard Setup and Requirements**

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

Understanding **Boolean algebra** is crucial

 for optimizing digital circuits. Simplifying complex logical expressions reduces the number of gates required.

---

## 🚀 **Getting Started**

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/digital-logic-design.git
```

---

## 📝 **License**

This project is licensed under the MIT License. See the LICENSE file for details.

---

## 🏁 **Conclusion**

This repository provides a comprehensive guide to understanding and experimenting with basic digital logic using the 74HC series ICs. The use of real ICs, breadboard setups, and Boolean algebra ensures a practical learning approach, making it easier to apply this knowledge to larger digital systems.
