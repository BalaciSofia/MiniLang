# MiniLang

## Overview

MiniLang is a Java-based interpreter for a custom programming language, developed over 2 months.

The project focuses on program execution at runtime, implementing a full execution engine with memory management, concurrency, and static type checking.

Programs are constructed directly as Abstract Syntax Trees (ASTs) (no parser), allowing focus on execution logic and system design.(parser in making)

---

## Language Features

* Variable declarations (`int`, `bool`, `string`, references)
* Arithmetic expressions (`+`, `-`, `*`, `/`)
* Logical expressions (`and`, `or`, `not`)
* Relational expressions (`<`, `<=`, `==`, `!=`, `>`, `>=`)

### Control Flow

* `if-then-else`
* `switch`
* Loops: `while`, `for`, `repeat`

### Concurrency

* `fork` (multi-threaded execution)
* `sleep`, `wait`
* other concurrency features for this project can be found  [here](https://github.com/BalaciSofia/MiniLang-Concurrency)
  
### File Operations

* `openRFile`
* `readFile`
* `closeRFile`

### Heap Memory

* Allocation: `new`
* Read: `rH`
* Write: `wH`
* Garbage collection

### Other

* `print`
* `nop`

---

## Execution Model

Each program runs using a Program State composed of:

* Execution Stack – controls execution flow
* Symbol Table – stores variables and values
* Output List – stores printed results
* File Table – manages opened files
* Heap Table – handles dynamic memory

---

## Interfaces

### Console Interface

* Menu-driven program execution
* Step-by-step execution with logging

### GUI (JavaFX)

* Program selection
* Visualization of:

  * Execution stack
  * Symbol table
  * Heap
  * Output
  * File table
* Step-by-step execution control

---

## How to Run

### Requirements

* Java JDK 8+
* JavaFX (for GUI)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/BalaciSofia/MiniLang.git
   cd MiniLang
   ```

2. Compile:

   ```bash
   javac Main.java
   ```

3. Run:

   ```bash
   java Main
   ```

4. Run GUI:

   ```bash
   java MainGUI
   ```

---

