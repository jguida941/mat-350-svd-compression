
# MAT-350 Project 2: SVD Image Compression and Rank-k Approximations

**Author:** Justin Paul Guida  
**Course:** MAT-350 – Applied Linear Algebra  
**Date:** October 16, 2025  


## Overview
This repository contains the MATLAB implementation and documentation for **Project 2**, which applies **Singular Value Decomposition (SVD)** to compute rank-k approximations of matrices and images.  
It demonstrates how dimensionality reduction can be used for both **matrix approximation** and **image compression**, balancing storage efficiency and image quality.

Both `.m` and `.mlx` versions of the project are included:

- `.m`: Executable MATLAB script suitable for reproducibility  
- `.mlx`: Interactive Live Script with explanations and formatted results  
- `.pdf`: Exported report version for viewing without MATLAB  



## Objectives
1. Compute low-rank matrix approximations using SVD  
2. Measure approximation quality using Root Mean Square Error (RMSE)  
3. Apply rank-k SVD approximations to a grayscale image for compression  
4. Analyze the relationship between compression ratio (CR), rank, and image quality  
5. Compare approximations at CR = 10, 25, and 75 and identify the optimal balance  



## Files
| File | Description |
|------|--------------|
| `mat350-svd-compression.mlx` | MATLAB Live Script with formatted text, figures, and explanations |
| `mat350_svd_compression.m` | Standard MATLAB script version, suitable for direct execution |
| `mat350-svd-compression.pdf` | PDF export of the Live Script for viewing without MATLAB |
| `MAT 350 Project Two MATLAB Image.mat` | Image dataset used for compression analysis |



## Methods
The project uses the **Singular Value Decomposition (SVD)**

\[
A = U \Sigma V^T
\]

and constructs approximations of the form

\[
A_k = U(:,1:k)\Sigma(1:k,1:k)V(:,1:k)^T
\]

for various values of k.

### Implementation Steps
1. Compute SVD with MATLAB’s `svd()` function  
2. Construct rank-1 and rank-2 matrix approximations  
3. Compute RMSE between *A* and *Aₖ*  
4. Apply SVD to a grayscale image for compression  
5. Compare reconstructed images at different *k* values  


## Results Summary
- Low-rank approximations preserve the main structure of *A* while discarding smaller singular values  
- Increasing rank decreases RMSE and improves image quality  
- A compression ratio of **CR ≈ 15** offers the best trade-off between file size and clarity  



## How to Run
1. Open MATLAB  
2. Navigate to the project directory:
   ```matlab
   cd path_to_folder/mat350_svd_compression

	3.	Run the script: mat350_svd_compression


	4.	The program will:
	•	Display RMSE calculations
	•	Show original and compressed images at multiple CR values

Ensure MAT 350 Project Two MATLAB Image.mat is in the same folder as the script.


## Dependencies
	•	MATLAB R2023a or later
	•	Image Processing Toolbox (for imshow)



## Educational Purpose

This repository demonstrates how linear algebra concepts, particularly SVD and orthogonal decomposition, apply to real-world problems such as data compression and dimensionality reduction.
It serves as both an academic submission and a teaching reference for students studying applied linear algebra with MATLAB.
