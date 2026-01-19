# Ardena Programming Language

Ardena is a **free, library-driven, and highly extensible programming language** designed for maximum flexibility. Its core philosophy is to provide a minimalist execution engine that can be infinitely expanded through external libraries, allowing developers to define, combine, and evolve functionality without hardcoded constraints.

---

## ✨ Core Principles

* **Zero Hardcoding**
  The core engine remains neutral. Almost all logic is defined and extended through external library files.

* **Infinite Extensibility**
  Multiple libraries can be combined to create complex hybrid systems without modifying the engine.

* **Minimal & Clean Syntax**
  Focuses on logic and readability rather than boilerplate.

* **Open & Community-Friendly**
  Designed to encourage community-driven libraries and core experimentation.

---

## 🚀 Project Vision

Ardena is a long-term project with two major goals:

1. **Ardena Language**
   A completely free programming language powered by a dynamic, library-based architecture.

2. **HellOS (Future Goal)**
   A native operating system designed to run directly on Ardena.

---

## 📦 Installation

### Using the Installer

The official **Ardena Installer** automatically:

* Creates required directories
* Registers Ardena in the system `PATH`
* Prepares the runtime environment

Recommended for most users.

### Manual Installation

1. Download the latest **`Ardena_Package.zip`** from the Releases page.
2. Extract it to:

   ```text
   C:\Users\<YourUser>\AppData\Local\Ardena
   ```
3. Add this directory to your system **PATH**.

---

### 🔄 Updating

If Ardena is already installed, update it via terminal:

```bash
ardena --update
```

---

## 📘 Comprehensive Usage Guide

Ardena is intentionally minimalist. Its true power comes from how libraries are defined and combined.

---

## 1️⃣ Creating Your First Script

Ardena scripts use the **`.ard`** extension.

### `main.ard`

```ard
# Variable assignment
greeting << "Hello, Ardena!"
version << 1.1

# Output to console
print(greeting)
print("Running version: " + version)
```

---

## 2️⃣ The Library System (`.alib`)

The library system is the foundation of Ardena. There are no fixed operators or behaviors—everything is defined by libraries.

Libraries are stored in the **`libs/`** directory.

---

### Step A: Creating a Library

Create `maths.alib` inside the `libs/` folder:

```ard
# Syntax: DEF [Symbol] -> Logic
# 'a' is the left operand, 'b' is the right operand

DEF [+] -> a + b
DEF [-] -> a - b
DEF [*] -> a * b
DEF [/] -> a / b

DEF [is_equal] -> a == b
DEF [is_greater] -> a > b
```

---

### Step B: Using the Library

```ard
import maths

x << 10
y << 5

result << x + y
print("Result: " + result)

if x is_greater y
    print("X is bigger than Y")
end
```

---

## 3️⃣ Combining Multiple Libraries

Ardena allows multiple libraries to work together seamlessly, enabling complex systems to be built from small components.

```ard
import maths
import strings
import filesystem

data << f_read("data.txt")

if len(data) is_equal 0
    print("File is empty!")
end
```

---

## 4️⃣ Control Structures

### Conditionals

```ard
status << 1

if status
    print("Condition met")
end
```

### Loops

```ard
counter << 1

while counter < 5
    print("Step: " + counter)
    counter << counter + 1
done
```

---

## 5️⃣ Built-in Engine Functions

| Function        | Description             | Example                      |
| --------------- | ----------------------- | ---------------------------- |
| `print(val)`    | Prints value to console | `print("Hello")`             |
| `input(msg)`    | Gets user input         | `name << input("Name: ")`    |
| `f_write(p, c)` | Writes content to file  | `f_write("log.txt", "data")` |
| `f_read(p)`     | Reads file content      | `data << f_read("log.txt")`  |
| `delete(var)`   | Deletes a variable      | `delete("temp_var")`         |

---

## 🛣 Roadmap

Below is the expanded development roadmap for Ardena. This roadmap is flexible by design and may evolve as the language and its ecosystem grow.

### ✅ Completed

* [x] **Core Engine Development**
  Minimalist execution engine with neutral logic handling and extensible foundations.

* [x] **Dynamic Library System**
  External `.alib` libraries defining operators, logic, and behavior without engine hardcoding.

* [x] **Automatic Update System**
  Built-in updater allowing seamless version upgrades via terminal.

---

### 🧪 Planned

* [ ] **Module / Package System**
  Namespaced libraries, versioning, and reusable packages.

* [ ] **CLI Tooling Improvements**
  Commands for project creation, library management, and diagnostics.

* [ ] **Language Specification & Documentation**
  Formal documentation describing syntax, execution model, and best practices.

---

### 🌌 Long-Term Vision

* [ ] **JIT / Bytecode Execution Layer**
  Optional execution modes for performance-critical applications.

* [ ] **Foreign Function Interface (FFI)**
  Ability to interface with C / C++ / other native libraries.

* [ ] **Ardena-Based Toolchain**
  Build tools, debuggers, and editors designed specifically for Ardena.

* [ ] **HellOS Integration**
  A native operating system built to run directly on Ardena as its primary language.

---

Ardena is designed to evolve organically — the roadmap reflects direction, not limitation.

## 📜 License

Ardena is an open project dedicated to the freedom of programming.

There is no formal license at this time. If you use, modify, or distribute this project, please give credit to the original author.

---

**Ardena** — *Build the language you want, not the one you are given.*
