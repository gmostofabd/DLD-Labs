# 🟢 **Digital Logic Design: Basic Experiments**

Welcome to the **Digital Logic Design** repository! This collection contains experiments focusing on the basics of digital logic gates using common ICs, equivalent circuits, and practical implementation using a breadboard.

## 🌟 **Contents**

1. [Introduction to Digital Logic](#introduction-to-digital-logic)
2. [Basic Logic Gates](#basic-logic-gates)
3. [Universal Gates](#universal-gates)
4. [Combinational Circuits](#combinational-circuits)
   - [Half-Adder](#half-adder)
5. [Sequential Circuits](#sequential-circuits)
   - [D Flip-Flop](#d-flip-flop)
6. [Common ICs: 74HC Series](#common-ics-74hc-series)
7. [Equivalent Circuits for Basic Gates](#equivalent-circuits-for-basic-gates)
8. [Breadboard Setup and Requirements](#breadboard-setup-and-requirements)
9. [Boolean Algebra and Simplification](#boolean-algebra-and-simplification)
10. [Getting Started](#getting-started)
11. [License](#license)

---

## 🔵 **Introduction to Digital Logic**

Digital logic is the backbone of modern electronics. This repository is designed to give hands-on experience with **logic gates**, their IC implementations, and simple circuits using diodes and transistors.

---

## 🔵 **Basic Logic Gates**

### Logic Gate Symbols & Truth Tables

| **Gate**   | **Symbol**                        | **Truth Table**                                                |
|------------|-----------------------------------|----------------------------------------------------------------|
| **AND**    | 
```
      A ----|\
             | AND |---- Output
      B ----|/
```
| Input A | Input B | Output <br> 0 | 0 | 0 <br> 0 | 1 | 0 <br> 1 | 0 | 0 <br> 1 | 1 | 1 |
| **OR**     | 
```
      A ----|\
             | OR  |---- Output
      B ----|/
```
| Input A | Input B | Output <br> 0 | 0 | 0 <br> 0 | 1 | 1 <br> 1 | 0 | 1 <br> 1 | 1 | 1 |
| **NOT**    | 
```
      A ----|>o---- Output
```
| Input  | Output <br> 0 | 1 <br> 1 | 0                              |

### Keywords: AND, OR, NOT, Truth Table

---

## 🟡 **Universal Gates**

| **Gate**   | **IC**        | **Truth Table**                                               |
|------------|---------------|---------------------------------------------------------------|
| **NAND**   | 74HC00        | A | B | A NAND B <br> 0 | 0 | 1 <br> 0 | 1 | 1 <br> 1 | 0 | 1 <br> 1 | 1 | 0 |
| **NOR**    | 74HC02        | A | B | A NOR B <br> 0 | 0 | 1 <br> 0 | 1 | 0 <br> 1 | 0 | 0 <br> 1 | 1 | 0 |
| **XOR**    | 74HC86        | A | B | A XOR B <br> 0 | 0 | 0 <br> 0 | 1 | 1 <br> 1 | 0 | 1 <br> 1 | 1 | 0 |

### Keywords: NAND, NOR, XOR, Truth Table

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
| Input A | Input B | Sum | Carry |
|---------|---------|-----|-------|
|    0    |    0    |  0  |   0   |
|    0    |    1    |  1  |   0   |
|    1    |    0    |  1  |   0   |
|    1    |    1    |  0  |   1   |

### Keywords: Half-Adder, Sum, Carry

---




### Keywords: Half-Adder, Sum, Carry

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
| Input D | Clock | Output Q |
|---------|-------|----------|
|    0    |   ↑   |    0     |
|    1    |   ↑   |    1     |

### Keywords: D Flip-Flop, Memory, Clock

---


### Keywords: D Flip-Flop, Memory

---

## 🟢 **Common ICs: 74HC Series**

The **74HC** series is a family of **high-speed CMOS** logic ICs that operate on low power and have fast switching times. Below are some widely used ICs for implementing basic and universal gates:

- **74HC00**: Quad 2-input **NAND** Gate IC.
- **74HC02**: Quad 2-input **NOR** Gate IC.
- **74HC04**: Hex **Inverter** (NOT gate) IC.
- **74HC08**: Quad 2-input **AND** Gate IC.
- **74HC32**: Quad 2-input **OR** Gate IC.
- **74HC86**: Quad 2-input **XOR** Gate IC.

Each IC contains multiple gates (typically 4 or 6), making them convenient for building small circuits on breadboards.

### Keywords: 74HC00, 74HC02, 74HC04, 74HC08, 74HC32, 74HC86

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
- Diodes D1 and D2 ensure that if either input is HIGH, the output will be HIGH.

### 3. NOT Gate (Transistor Logic)
A single NPN transistor can be used to create a NOT gate. When the input is HIGH, the transistor conducts, grounding the output to LOW.

**Equivalent Circuit:**
- When input is HIGH, the transistor switches ON, creating a LOW output (inverted signal).

These circuits illustrate how digital gates can be simplified into fundamental components, giving insights into their internal structure.

### Keywords: Diodes, Transistors, Equivalent Circuit

---

## 🟣 **Breadboard Setup and Requirements**

To investigate the behavior of these gates, you will need the following:

### Basic Requirements:
- **Breadboard**: Essential for prototyping circuits without soldering, allowing for quick and flexible assembly.
- **Power Supply**: Typically, a 5V DC power supply to power the 74HC ICs.
- **Jumper Wires**: For connecting ICs, power, and input/output signals on the breadboard.
- **LEDs**: To visualize the outputs of the logic gates.
- **Resistors**: To limit current to the LEDs and ensure proper logic levels.
- **Switches**: For manually inputting HIGH or LOW signals into the gates.

### Breadboard Layout:
1. Place the **74HC IC** at the center of the breadboard.
2. Connect **Vcc (pin 14)** and **GND (pin 7)** to power and ground, respectively.
3. Use **push buttons** or switches for inputs (connected to the IC’s input pins).
4. Attach **LEDs** to the outputs to display the results of the gate operations.

By setting up your breadboard this way, you can easily explore how different gates work by observing the LEDs.

### Keywords: Breadboard, Power Supply, Circuit Assembly

---

## 🟣 **Boolean Algebra and Simplification**

Boolean algebra is the mathematical foundation for digital logic circuits. This section demonstrates how to simplify complex logic expressions using **Boolean identities** and **Karnaugh maps (K-maps)**.

### Karnaugh Map Example

A **Karnaugh Map** is a visual tool for simplifying Boolean expressions. Here's an example for the expression \( A'B + AB' \).

#### Karnaugh Map
```
      AB
      00  01  11  10
   +-----------------
  0|  0   1   0   1   (A')
  1|  0   0   1   0   (A)
```

#### Simplified Expression
The simplified expression derived from the K-map is:
\[ A'B + AB' \]

### Keywords: Karnaugh Map, Simplification, Boolean Algebra

---

