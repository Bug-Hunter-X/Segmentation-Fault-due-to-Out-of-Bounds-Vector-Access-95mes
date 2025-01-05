# C++ Segmentation Fault Bug

This repository demonstrates a common C++ bug that leads to a segmentation fault: accessing an element in a `std::vector` beyond its bounds.

The `bug.cpp` file contains the erroneous code. The `bugSolution.cpp` file shows how to fix the issue.

## Bug Description
The original code iterates through a vector using a `for` loop, but the loop condition `i <= vec.size()` is incorrect.  It should be `i < vec.size()` to avoid accessing the element at index `vec.size()`, which is one past the last valid element.  Attempting to access this invalid memory location results in undefined behavior, most commonly a segmentation fault.

## Solution
The corrected code in `bugSolution.cpp` uses the proper loop condition `i < vec.size()` to prevent the out-of-bounds access.  This ensures that only valid elements of the vector are accessed.