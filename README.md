
# MAT-350 Project 2: SVD Image Compression and Rank-k Approximations

**Author:** Justin Paul Guida  
**Course:** MAT-350 - Applied Linear Algebra  
**Date:** October 16, 2025  

---

## Overview

This repository contains the MATLAB implementation and supporting documentation for **Project 2**, focused on applying **Singular Value Decomposition (SVD)** to compute rank-k approximations of matrices and images.  
The project demonstrates how dimensionality reduction can be used for both matrix approximation and **image compression**, highlighting the trade-off between storage efficiency and image quality.

Both `.m` and `.mlx` versions of the project are included:

- The `.m` file provides executable code suitable for GitHub and reproducibility.  
- The `.mlx` file provides an interactive live script with formatted explanations and results.  
- A `.pdf` export of the live script is also included for easy viewing.

---

## Objectives

1. Compute low-rank matrix approximations using SVD.  
2. Measure approximation quality using the Root Mean Square Error (RMSE).  
3. Apply rank-k SVD approximations to a grayscale image for compression.  
4. Analyze the relationship between compression ratio (CR), rank, and image quality.  
5. Compare approximations at multiple compression ratios (e.g., CR = 10, 25, 75) and recommend an optimal balance.

---

## Files

| File | Description |
|------|--------------|
| `mat350-svd-compression.mlx` | MATLAB Live Script with formatted text, figures, and explanations. |
| `mat350_svd_compression.m` | Standard MATLAB script version, suitable for direct execution. |
| `mat350-svd-compression.pdf` | PDF export of the live script for viewing without MATLAB. |
| `MAT 350 Project Two MATLAB Image.mat` | Image dataset used for compression analysis. |

---

## Methods

The project uses the **Singular Value Decomposition**:

\[
A = U \Sigma V^T
\]

and constructs approximations of the form:

\[
A_k = U(:,1:k) \Sigma(1:k,1:k) V(:,1:k)^T
\]

for various values of \(k\).

### Key Steps

1. Compute SVD using MATLAB’s `svd()` function.  
2. Generate rank-1 and rank-2 approximations of a sample matrix.  
3. Compute RMSE between \(A\) and \(A_k\) to evaluate accuracy.  
4. Apply the same process to an image to achieve controlled compression ratios.  
5. Compare image reconstructions and RMSE across multiple \(k\) values.  

---

## Results Summary

- Low-rank approximations preserve the dominant structure of \(A\) while discarding small singular values.  
- As rank increases, RMSE decreases and the reconstructed image quality improves.  
- A moderate compression ratio (**CR ≈ 15**) provides the best trade-off between file size and visual clarity.  

---

## How to Run

1. Open MATLAB.  
2. Set the working directory to the project folder:
   ```matlab
   cd path_to_folder/mat350_svd_compression

	3.	Run the script:

mat350_svd_compression


	4.	The program displays:
	•	Intermediate RMSE calculations
	•	Original and compressed images for multiple CR values

Ensure the file MAT 350 Project Two MATLAB Image.mat is in the same folder as the script.

⸻

Dependencies
	•	MATLAB R2023a or later
	•	Image Processing Toolbox (for imshow)

⸻

Educational Purpose

This repository demonstrates how linear algebra concepts, specifically SVD and orthogonal decomposition, translate into practical applications such as data compression and dimensionality reduction.
It serves as both an academic submission and a reference example for students learning applied linear algebra with MATLAB.

---
