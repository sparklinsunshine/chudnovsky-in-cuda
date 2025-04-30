# chudnovsky-in-cuda

 This project demonstrates the incredible speedup achievable by leveraging GPU acceleration for high-performance computing tasks.

## About the Chudnovsky Algorithm

The Chudnovsky algorithm is a fast method for calculating the digits of π (pi) with high precision. It is based on a rapidly converging series derived from complex mathematical formulas involving factorials, powers, and constants. This algorithm is widely used in computational mathematics and is particularly suitable for parallelization due to its iterative nature.

## Files

- `cuda_hpc_ahp.ipynb`: A comprehensive Jupyter Notebook that walks you through the implementation of the Chudnovsky algorithm in CUDA. It includes setup instructions, code execution steps, and performance comparisons between CPU and GPU computations.

## Code Explanation

The `cuda_hpc_ahp.ipynb` file contains the following key components:

1. **Environment Setup**:
   - Commands to check GPU availability (`!nvidia-smi`) and CUDA version (`!nvcc --version`).
   - Installation of the CUDA compiler if required.

2. **CUDA Implementation**:
   - A CUDA C++ program (`chudnovsky.cu`) is written to compute the terms of the Chudnovsky series on both CPU and GPU.
   - The program defines:
     - `factorial_device`: A device function to compute factorials on the GPU.
     - `chudnovsky_gpu`: A kernel function to compute terms of the series in parallel on the GPU.
     - `factorial_cpu` and `chudnovsky_cpu`: Equivalent functions for CPU computation.

3. **Performance Comparison**:
   - The program measures the time taken for computation on both CPU and GPU.
   - Outputs the first few terms computed by both methods for verification.
   - Calculates the speedup achieved by using the GPU.

4. **Compilation and Execution**:
   - The CUDA program is compiled using `nvcc`.
   - The compiled binary is executed to display the results.

## Highlights

- **High Performance Computing**: Witness the efficiency of CUDA for computationally intensive tasks.
- **Educational Resource**: Perfect for students and enthusiasts exploring GPU programming.
- **Real-World Application**: Learn how mathematical algorithms can be optimized for modern hardware.

