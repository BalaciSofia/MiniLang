# MiniLang

This project is a **Toy Language Interpreter** implemented in Java, developed incrementally in 3 months.

The interpreter executes a simple custom language featuring variables, expressions, control flow, file operations, heap management, concurrency, and type checking.

---
### Language Support

* Variable declarations (`int`, `bool`, `string`, references)
* Arithmetic expressions (`+`, `-`, `*`, `/`)
* Logical expressions (`and`, `or`)
* Relational expressions (`<`, `<=`, `==`, `!=`, `>`, `>=`)
* Conditional statements (`if-then-else`)
* Looping (`while`)
* Print statements
* No-op statements (`nop`)

### Program Execution Model

Each program is executed using a **Program State**, composed of:
* **Execution Stack** – controls execution flow
* **Symbol Table** – stores variable bindings
* **Output List** – stores printed values
* **File Table** – manages opened files
* **Heap Table** – handles dynamic memory allocation

### File Operations

* Open file (`openRFile`)
* Read from file (`readFile`)
* Close file (`closeRFile`)

Files are managed through a dedicated **FileTable**, mapping filenames to file descriptors .

### Heap Memory Management

* Reference types (`RefType`)
* Heap allocation (`new`)
* Heap read (`rH`)
* Heap write (`wH`)
* Garbage collection

The heap is implemented as a dynamic memory structure with address-based access .

### Concurrency

* Multi-threaded execution via `fork`
* Multiple program states running in parallel
* Shared heap, output, and file table
* Thread-safe execution using `ExecutorService`

Concurrency support is introduced by allowing the interpreter to manage multiple execution contexts simultaneously .

### Static Type Checking

* Prevents invalid programs before execution
* Ensures type safety for:
  * Assignments
  * Expressions
  * Control flow statements

Type checking is performed before program execution begins .

### Console Interface

* Menu-based system
* Run predefined example programs
* Step-by-step execution logging

### GUI (JavaFX)

* Program selection window
* Live visualization of:

  * Execution stack
  * Symbol table
  * Heap
  * Output
  * File table
* Step-by-step execution via button

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

2. Compile the project:

   ```bash
   javac Main.java
   ```

3. Run:

   ```bash
   java Main
   ```

4. (Optional) Launch GUI version:

   ```bash
   java MainGUI
   ```
