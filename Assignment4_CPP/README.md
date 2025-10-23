

---

## 📘 Overview

This repository contains the complete implementation and report for **COEN 244 Assignment 4**, which focuses on **File I/O**, **Templates**, **Operator Overloading**, and **Inheritance** in C++.

The assignment consists of two main problems:

1. **File I/O and Data Sharding**  
2. **Template Tensor and Inheritance**

It builds upon concepts introduced in Assignment 3, adding:
- File handling using `fstream` and `stringstream`
- Data segmentation (sharding)
- Class templates and operator templates
- Inheritance with generic types
- Loading IoT dataset shards into tensors

---

## 🧾 Problem 1 — File I/O and Data Sharding

### 🔹 Objective
Write a program (`DataSharding.cpp`) that reads and partitions the **RT-IoT 2022** dataset into multiple data shard files, each containing a fixed number of samples.

### 🔹 Dataset Reference
B. S. and R. Nagapadma, *“RT-IoT 2022,” UCI Machine Learning Repository, 2023.*  
[Online]. Available: [https://doi.org/10.24432/C5P338](https://doi.org/10.24432/C5P338)

### 🔹 Tasks
| Task | Description |
|------|--------------|
| **1** | Create `DataSharding.cpp` that partitions the RT-IoT 2022 dataset into multiple shards. |
| | Each shard must contain a header line (column titles) and a user-specified number of data samples. |
| | The program should prompt for: ① number of samples per shard, and ② output directory path. |
| | Each shard file should be named `shard_<index>.txt` (e.g., `shard_0.txt`, `shard_1.txt`, etc.). |
| | Include screenshots of console inputs and the directory showing generated shard files. |

### 🔹 Deliverables
- Source code of `DataSharding.cpp`  
- Screenshot of terminal inputs and program output  
- Screenshot of target directory showing generated shard files  

---

## 🧮 Problem 2 — Templates, Operator Overloading, and Inheritance

### 🔹 Objective
Implement a **template-based tensor system** that supports multiple data types (`string`, `double`, etc.), using operator overloading and class inheritance.

### 🔹 Tasks
| Task | Description |
|------|--------------|
| **2.1** | Create a template class `RankOneTensorType<T>` derived from `BaseTensor`. This class represents a one-dimensional tensor of generic type `T`. |
| | Implement all required operator overloads as function templates: |
| | `++`, `+` (tensor + tensor), `+` (tensor + scalar), `=`, `>>`, `<<`, and `[ ]`. |
| | Operators should handle invalid dimensions or indices using `invalid_argument`. |
| | Write a test driver to verify functionality using both `string` and `double` tensors. |
| **2.2** | Create class `IoTDataTensor` derived from `RankOneTensorType<string>`. |
| | Implement the following methods: |
| | • `double getValue(int row, int col)` – returns a numeric value from the data sample. |
| | • `string getCategory(int col)` – returns the column title. |
| | • `void loadData()` – reads data from the shard files created in Problem 1, storing: |
| | &nbsp;&nbsp;• `std::vector<string> iot_category` → column titles |
| | &nbsp;&nbsp;• `std::vector<RankOneTensorType<string>> iot_data` → sample rows |
| | Write a test driver that loads shard data and prints selected column values. |

### 🔹 Unit Tests
| Function | Purpose |
|-----------|----------|
| `testTensorType()` | Tests template class with both string and double tensors |
| `testIoTDataTensor()` | Loads shard files and retrieves category/value pairs |
| `testIncrementOperatorRankOne()` | Tests `++` operator for rank-1 tensor |
| `testAddOperatorRankOne()` | Tests addition of two rank-1 tensors |
| `testAssignmentOperatorRankOne()` | Tests `=` operator with validation |
| `testCoutStreamOperatorRankOne()` | Tests `<<` output stream operator |
| `testCinStreamOperatorRankOne()` | Tests `>>` input stream operator |
| `testIndexOperatorRankOne()` | Tests index operator `[ ]` with boundary checking |

### 🔹 Deliverables
- Source code for all classes (`BaseTensor.h/.cpp`, `RankOneTensorType.h/.cpp`, `IoTDataTensor.h/.cpp`, `testDriver.cpp`)  
- Console output screenshots for all test functions  

---

## 🧪 Compilation & Execution

### 🔧 Compile
```bash
g++ *.cpp -o Assignment4
