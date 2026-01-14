# Percolation Simulation

This project implements a simulation of the classic **percolation problem**, modeling how connectivity emerges in an N×N grid as sites are incrementally opened. The system determines whether a path of open sites connects the top row to the bottom row, indicating percolation.

The project was built using the **Union–Find (Disjoint Sets)** data structure to efficiently model dynamic connectivity as sites are opened.

## Key Concepts
- Union–Find (Weighted Quick Union with Path Compression)
- Graph connectivity and grid modeling
- Algorithmic efficiency and constant-time operations
- Preventing backwash using multiple union–find structures

## Implementation Overview
- Each site in the grid is mapped to a 1D index and tracked as open or blocked.
- A virtual **top node** and **bottom node** are used to detect percolation.
- Two Union–Find instances are maintained:
  - One to detect percolation
  - One to determine whether a site is *full* while avoiding the backwash problem
- All operations run in near-constant time using efficient union–find operations.

## API
The core functionality is implemented in `Percolation.java`, which supports:
- Opening a site
- Checking if a site is open or full
- Counting open sites
- Determining whether the system percolates

## Example Use Cases
- Modeling physical systems such as fluid flow through porous materials
- Studying probabilistic connectivity thresholds
- Demonstrating efficient dynamic connectivity algorithms

## Technologies
- Java
- Princeton `algs4` library (`WeightedQuickUnionUF`)

---

This project was developed as part of a data structures curriculum and demonstrates practical application of union–find to a real-world modeling problem.
