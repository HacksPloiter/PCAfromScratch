# PCA Scratch Implementation

## Overview
This notebook is a PCA implementation from scratch written using NumPy. It walks through the core PCA steps on a very small 2-feature dataset to make the math easy to follow.

## Objective
- PCA implementation without using sklearn.
- See how eigenvalues and eigenvectors produce principal components.
- Confirm PCA by rebuilding the original data.

## Workflow

### Data
- A small dataset with 15 samples and 2 features is created manually.
- Data is transposed so each row is one sample.

### Standardization
- Mean and standard deviation are computed from the full matrix.
- Data is standardized using a single global mean and std.

### PCA steps
- Covariance matrix is computed from standardized data.
- Eigenvalues and eigenvectors are calculated.
- Eigenvalues are sorted and eigenvectors reordered.
- Data is projected to PC1 and PC2.

### Reconstruction
- Standardized data is reconstructed using both components.
- Original scale is restored using the stored mean and std.
- Restored values are compared with the original matrix.

### Helper functions
- `mypca` groups PCA steps into a single function.
- `restoremat` tries to rebuild the original data from PCA output.

## Takeaways
- PCA is just linear algebra applied in the right order.
- Eigenvector sorting matters for correct components.
- Rebuilding the data is a good way to verify PCA logic.

## Notes
- The notebook focuses on clarity over generality.
- Calculations are kept explicit instead of abstracted.
- The dataset is intentionally small to make each step traceable.