# Correlation Matrix Adjustment Methods

Solutions for Applied Finance homework on finding the nearest estimate of correlation matrices.

## Overview

This project implements two methods for adjusting non-positive definite correlation matrices:
1. **Spectral Decomposition Method** - Eigenvalue adjustment approach
2. **Alternating Projection Method** - Dykstra's iterative algorithm

## Files

- `exercise_1_data_analysis.ipynb` - Data analysis and correlation matrix estimation for 3 datasets
- `exercise_2_functions.ipynb` - Implementation of adjustment functions
- `Data_HW-20251128/` - Excel data files (set_1.xlsx, set_2.xlsx, set_3.xlsx)

## Requirements

```
numpy
pandas
scipy
matplotlib
seaborn
openpyxl
```

## Usage

Both notebooks are self-contained and can be run independently:
- `exercise_1_data_analysis.ipynb` - Analyzes 3 datasets and determines if adjustment is needed
- `exercise_2_functions.ipynb` - Tests the adjustment functions on example matrices

## Results Summary

### Exercise 1: Data Analysis
- **Set 1**: Needs adjustment (negative eigenvalue detected)
- **Set 2**: No adjustment needed (all eigenvalues positive)
- **Set 3**: Needs adjustment (near-zero eigenvalue from perfect correlations)

Both adjustment methods successfully corrected the non-positive definite matrices. Alternating Projection typically provides closer approximation to the original matrix (smaller Frobenius distance).

### Exercise 2: Function Implementation
Both functions correctly adjust the test correlation matrix:
- **Spectral Decomposition**: Faster, simpler implementation
- **Alternating Projection**: More accurate, converges in ~10-20 iterations

All adjusted matrices are positive semi-definite with unit diagonal elements.

## Methods

### Spectral Decomposition
Adjusts negative eigenvalues to a small positive value (ε = 10⁻⁸) and reconstructs the matrix.

### Alternating Projection
Uses Dykstra's algorithm to iteratively project onto positive semi-definite matrices with unit diagonal.
