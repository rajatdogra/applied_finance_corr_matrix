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

## Methods

### Spectral Decomposition
Adjusts negative eigenvalues to a small positive value (ε = 10⁻⁸) and reconstructs the matrix.

### Alternating Projection
Uses Dykstra's algorithm to iteratively project onto positive semi-definite matrices with unit diagonal.
