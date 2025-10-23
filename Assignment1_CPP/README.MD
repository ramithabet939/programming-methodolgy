# Assignment 1 - C++ Object-Oriented Programming

## Overview
This repository contains solutions for **Assignment 1**, demonstrating **C++ Object-Oriented Programming (OOP)** concepts such as classes, constructors, copy constructors, destructors, encapsulation, and member functions.  
The assignment includes **two separate questions**:  

1. **Employee Class**
2. **Invoice Class**

---

## Question 1 – Employee Class

### Description
Defines an `Employee` class to store employee details:
- `firstName` (string)
- `lastName` (string)
- `salary` (int)

### Key Features
- Constructor to initialize employee details (salary cannot be negative).
- Copy constructor to clone employee objects.
- Destructor outputs a message when an object is destroyed.
- Getter and setter methods for all attributes.

### Example Usage
```cpp
Employee emp1("John", "Doe", 50000);
emp1.setSalary(55000);
std::cout << emp1.getFirstName() << " earns " << emp1.getSalary() << std::endl;


## Question 2 – Invoice Class

### Description
Defines an `Invoice` class to represent a product invoice:
- `partNum` (string) – part number
- `partDsp` (string) – part description
- `qty` (int) – quantity of items
- `price` (int) – price per item

### Key Features
- Constructor initializes invoice details. Negative quantity or price is set to 0.
- Copy constructor allows cloning of invoice objects.
- Destructor outputs a message when an invoice object is destroyed.
- Getter and setter methods for all attributes.
- `getInvoiceAmount()` calculates total price (`qty * price`).
- `clone()` methods to duplicate invoice objects.

### Example Usage
```cpp
Invoice inv("A123", "Widget", 10, 25);
std::cout << "Total Invoice: " << inv.getInvoiceAmount() << std::endl;

Invoice copyInv = inv.clone();
std::cout << "Cloned Invoice Amount: " << copyInv.getInvoiceAmount() << std::endl;
Features Demonstrated

Encapsulation: All member variables are private with public getter/setter methods.

Constructors & Copy Constructors: Proper object initialization and duplication.

Destructors: Debug messages on object destruction.

OOP Principles: Create, modify, and clone invoice objects easily.
