## 📘 Overview

This repository contains the full implementation and documentation for **COEN 244 Assignment 2**, which focuses on **object-oriented programming in C++**, emphasizing **class design, inheritance, composition, and polymorphism** through two main problems:

1. **Employee Management System (Problem 1)**
2. **Geometric Shape Hierarchy (Problem 2)**

The assignment demonstrates:
- Proper class design and inheritance  
- Parameter validation and exception handling  
- Use of `stringstream` for formatted string output  
- Implementation of copy constructors and friend functions  
- Unit testing and console-based output verification  
- Design diagrams and reasoning for reusability through inheritance  

---

## 🧩 Problem 1 — Employee Class Hierarchy

### 🔹 Objective
Extend and implement classes from textbook examples:
- `CommissionEmployee`
- `BasePlusCommissionEmployee`

### 🔹 Tasks
| Task | Description |
|------|--------------|
| **1.1** | Add a copy constructor to `CommissionEmployee`. |
| **1.2** | Add a copy constructor to `BasePlusCommissionEmployee` (header). |
| **1.3** | Implement `BasePlusCommissionEmployee.cpp`. |
| **1.4** | Compile and test using provided `testDriver.cpp`. |
| **1.5** | Add new test function for copy constructor testing. |
| **1.6** | Define and implement `friend bool checkGrossSales(...)` in `CommissionEmployee`. |
| **1.7** | Extend test function to validate `checkGrossSales`. |
| **1.8** | Discuss inheritance behavior in your report. |

### 🔹 Key Features
- Exception handling using `invalid_argument`  
- Formatted output via `stringstream`  
- Validation of gross sales and commission rates  
- Comprehensive unit testing through driver program  

---

## 🧮 Problem 2 — Polygon and Shape Design

### 🔹 Objective
Design and implement a reusable class hierarchy for geometric shapes:
- `Point`
- `Polygon`
- `Quadrilateral`
- `Parallelogram`
- *(and optionally)* `Trapezoid`, `Rhombus`, `Rectangle`, `Square`

### 🔹 Tasks
| Task | Description |
|------|--------------|
| **2.1** | Create a UML/design diagram showing relationships and access specifiers. |
| **2.2** | Implement `Point`, `Polygon`, `Quadrilateral`, and `Parallelogram` classes with constructors and destructors. |
| **2.3** | Write `testDriver.cpp` containing unit tests for each class. |
| **2.4** | Write a report discussing your design choices and code reuse via inheritance. |

### 🔹 Test Cases
- **Polygon:** Calculate area using point coordinates  
- **Quadrilateral:** Verify four-point shape and area  
- **Parallelogram:** Compute sides, acute angles, and area  

### 🔹 Tools
Use [GeoGebra](https://www.geogebra.org/calculator) to visualize shapes and verify coordinates.

---

## 🧪 Testing and Execution

### 🔧 Compilation
```bash
g++ *.cpp -o Assignment2
