# Incorrect Deep Comparison of Objects and Arrays in PHP

This repository demonstrates a common error in PHP when performing deep comparisons of objects, specifically involving the incorrect handling of array comparisons. The provided code implements a recursive function to compare objects and values; however, it does not correctly handle array comparisons, leading to inaccurate comparison results.

The `bug.php` file contains the flawed code, showcasing the error.  The `bugSolution.php` file provides the corrected implementation.

## Bug Description

The original function fails to recursively compare arrays which causes the function to return incorrect results when comparing objects that contain arrays as properties. This leads to unexpected `false` results in scenarios where the array contents are the same but the arrays themselves are different objects.

## Solution

The solution involves modifying the recursive function to properly check for arrays using `is_array()` and then iterating through the elements of the arrays. This ensures that all elements within the arrays are also compared recursively.
