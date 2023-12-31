# Parallel Programming with OpenMP - ECE 565 Fall 2023 Assignment #4

## Overview

This assignment for ECE-565 Performance Optmization & Parallelism (Fall 2023) focuses on parallel programming using OpenMP. It involves two sub-problems: parallelizing existing code for histogram generation and algebraic multigrid solver microkernel, and conducting performance experiments. This README outlines the project structure and requirements.

## Project Structure

### Problem 1: Histogram
- **Objective:** Parallelize the `histogram()` function in C using OpenMP.
- **Tasks:**
  1. Implement an array of locks (`histo_locks.c`).
  2. Use atomic operations (`histo_atomic.c`).
  3. Develop a creative solution without locks or atomic operations (`histo_creative.c`).
- **Performance Analysis:** Measure execution time with 2, 4, and 8 threads; compare against the sequential version.

### Problem 2: Algebraic Multigrid (AMG) Microkernel
- **Objective:** Parallelize key computations in AMG solver using OpenMP.
- **Components:**
  1. Compressed Sparse Row (CSR) matrix vector multiplication.
  2. AMG mesh relaxation.
  3. Vector operation (`a * X + Y`).
- **Performance Improvement:** Aim to enhance performance compared to baseline sequential code.
- **Report:** Describe code changes, OpenMP directives, and summarize performance improvements.

## Development & Testing Environment

- Personal VM or server machine (kraken.egr.duke.edu or leviathan.egr.duke.edu).
- Final performance experiments on an 8-core VM provisioned through Duke VCM.

## Key Challenges

- Ensuring code correctness in parallel code.
- Timing-dependent bugs common in parallel programming.
- Significant design effort required despite the moderate size of the code.

## Compilation & Execution

### Compiling with OpenMP
- Use the gcc compiler: `gcc -O3 -fopenmp -o <outputfile> <source_file>`

### Running the Program
- Set the number of threads and execute: `OMP_NUM_THREADS=4 ./test > result.out`

## Final Results

**report.pdf: Detailed writeup of the parallelization strategy, code changes, and performance analysis.

## Contributions

This project was completed as part of an academic assignment with requirments provided requirments.pdf. Contributions were made solely by Koushik Annareddy Sreenath, adhering to the project guidelines and requirements set by the course ECE-565 Performance Optmization & Parallelism. 


## License

This project is part of the ECE 565 course and is subject to university guidelines and policies regarding academic integrity and use.

## Acknowledgments

- Thanks to Brian Rogers and the course staff for providing guidance and support throughout the project.
