# Comparative Analysis of Sorting Algorithms

## Overview

This project presents a comparative study of multiple sorting algorithms implemented in C++. The objective was to evaluate the practical performance of different sorting techniques by measuring their execution times on various datasets and comparing their theoretical time complexities.

The project was developed for **CSCI 215 – Data Structures and Algorithms** at the American University of Ras Al Khaimah (AURAK).

The study compares six sorting implementations:

1. Original Insertion Sort
2. Improved Insertion Sort
3. Quick Sort (First Element Pivot)
4. Quick Sort V2A (Middle Element Pivot)
5. Quick Sort V2B (Last Element Pivot)
6. Counting Sort

---

## Objectives

* Implement multiple sorting algorithms from scratch.
* Compare execution times on large datasets.
* Analyze best-case, average-case, and worst-case performance.
* Investigate the effect of pivot selection in Quick Sort.
* Evaluate optimization techniques in traditional sorting algorithms.
* Determine the most efficient algorithm for different input conditions.

---

## Technologies Used

* C++
* Visual Studio 2022
* STL Libraries
* Chrono Library
* File Handling
* Dynamic Memory Allocation

---

## Dataset

Three datasets were used for testing:

### Random Dataset

* Randomly generated integers
* Represents average-case conditions

### Sorted Dataset

* Elements already arranged in ascending order
* Used to evaluate best-case and worst-case scenarios

### Reverse Sorted Dataset

* Elements arranged in descending order
* Common worst-case input for many sorting algorithms

---

## Algorithms Implemented

### 1. Original Insertion Sort

A simple comparison-based sorting algorithm that builds a sorted portion of the array one element at a time.

**Complexity:**

* Best Case: O(n)
* Average Case: O(n²)
* Worst Case: O(n²)

---

### 2. Improved Insertion Sort

An optimized version of insertion sort that introduces a flag to detect already sorted arrays and terminate early.

**Complexity:**

* Best Case: O(n)
* Average Case: O(n²)
* Worst Case: O(n²)

---

### 3. Quick Sort (First Pivot)

Uses the first element as the pivot during partitioning.

**Complexity:**

* Best Case: O(n log n)
* Average Case: O(n log n)
* Worst Case: O(n²)

---

### 4. Quick Sort V2A (Middle Pivot)

Uses the middle element as the pivot to reduce partition imbalance.

**Complexity:**

* Best Case: O(n log n)
* Average Case: O(n log n)
* Worst Case: O(n²)

---

### 5. Quick Sort V2B (Last Pivot)

Uses the last element as the pivot.

**Complexity:**

* Best Case: O(n log n)
* Average Case: O(n log n)
* Worst Case: O(n²)

---

### 6. Counting Sort

A non-comparison sorting algorithm that counts occurrences of each element.

**Complexity:**

* Best Case: O(n + k)
* Average Case: O(n + k)
* Worst Case: O(n + k)

where k is the range of input values.

---

## Key Features

* Reads datasets directly from text files.
* Supports multiple sorting algorithm selections.
* Measures execution time using the C++ Chrono library.
* Compares algorithm efficiency across different data distributions.
* Evaluates the impact of optimization techniques.
* Demonstrates practical implementation of recursion and partitioning strategies.

---

## Performance Results

| Algorithm                 | Random Data | Sorted Data | Reverse Sorted Data |
| ------------------------- | ----------- | ----------- | ------------------- |
| Insertion Sort            | 0.040454 s  | 0.000033 s  | 0.064636 s          |
| Improved Insertion Sort   | 0.0000005 s | 0.0000007 s | 0.070393 s          |
| Quick Sort (First Pivot)  | 0.003492 s  | 0.041888 s  | 0.039445 s          |
| Quick Sort (Middle Pivot) | 0.001959 s  | 0.000304 s  | 0.000539 s          |
| Quick Sort (Last Pivot)   | 0.036736 s  | 0.176788 s  | 0.121030 s          |
| Counting Sort             | 0.001672 s  | 0.000297 s  | 0.000500 s          |

---

## Key Findings

### Quick Sort Pivot Selection Matters

Choosing the middle element as the pivot significantly improved Quick Sort performance by producing more balanced partitions.

### Counting Sort Was Highly Efficient

Counting Sort consistently performed well due to its linear time complexity, especially when the input range was manageable.

### Improved Insertion Sort Excelled on Sorted Data

The optimization allowing early termination greatly reduced unnecessary iterations when arrays were already sorted.

### Worst-Case Behavior Was Observed

Quick Sort implementations using the first or last element as the pivot performed poorly on already sorted datasets due to unbalanced partitioning.

---

## Challenges Encountered

### Time Measurement Precision

Initial implementation using the C time library produced inaccurate measurements for very fast executions. This issue was resolved by using the Chrono high-resolution clock.

### Stack Overflow in Quick Sort

Using the first or last element as a pivot on sorted datasets caused deep recursion and stack overflow errors. The issue was mitigated by increasing the stack reserve size in Visual Studio.

### File Handling Issues

Reading datasets from external text files initially caused file path errors. A dedicated file-reading function was implemented to improve reliability and maintainability.

---

## Learning Outcomes

Through this project, I gained practical experience in:

* Sorting Algorithms
* Algorithm Optimization
* Time Complexity Analysis
* Recursion
* File Handling in C++
* Dynamic Memory Management
* Performance Benchmarking
* Experimental Analysis
* Data Structures and Algorithms

---



---

## Team Members
* Jannat Waqass
* Fatima Farooq
* Hana Rahiman
* Israa Awad

---

## Course Information

**Course:** CSCI 215 – Data Structures and Algorithms

---

## License

This project is intended for academic and educational purposes.
