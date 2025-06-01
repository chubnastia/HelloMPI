This project implements a high-performance, parallel solver for the Lorenz system of differential equations, a fundamental model in the study of chaos theory and nonlinear dynamics. By combining block numerical methods, adaptive step control, and hybrid parallel computing via MPI (Message Passing Interface) and OpenMP, the simulation achieves high accuracy and scalability on multicore and multi-node systems. The solution process is configurable through multi-format input (JSON, YAML, CSV, TXT) and outputs detailed trajectory data for further analysis in multiple formats.

It is known for its sensitivity to initial conditions and chaotic trajectories. Solving this system accurately over time requires adaptive and numerically stable methods—especially when simulating long-term behavior or high-resolution sampling. Standard explicit solvers either lack sufficient stability or are computationally expensive for finer steps.

   Solution Approach:
This project addresses the problem using the following strategies:

1. Block-Based ODE Solver
Implements a custom block method with adjustable block size k

Supports error estimation and adaptive time step adjustment

Numerically stable and more accurate than simple Euler or Runge-Kutta methods for stiff/chaotic systems

2. Hybrid Parallel Execution
MPI distributes workload across multiple processes using MPI_Allreduce, MPI_Bcast, etc.

OpenMP enables thread-level parallelism for key loops (e.g. norm computation, block assembly)

Result: efficient utilization of both distributed and shared memory systems

3. Multi-Format I/O
Reads simulation parameters from .json, .yaml, .csv, or .txt

Writes output as .csv, .json, .yaml, and .txt for interoperability with tools like MATLAB, Python, R

4. Robust Error Handling
Uses exception classes (InvalidParameterError) to handle invalid input or malformed configurations

Built-in validation logic checks dimensional consistency and physical constraints

   Methodological Contributions:
A generalized block solver with MPI-aware task decomposition

Automatic load balancing based on process rank and problem size

Configurable adaptive step-size control, including rejection statistics and runtime metrics

Extensible I/O interface, making it suitable for integration with visualization or post-processing tools

   Performance and Scalability
Scalability: Linear scalability observed for increasing number of MPI processes, bounded by communication overhead

Accuracy: Maintains numerical precision within the user-defined tolerance (e.g. 1e-6)

Efficiency: OpenMP optimizations reduce CPU time for local vector operations and reduce MPI wait times

   Potential Applications
Chaotic system analysis and sensitivity studies

Benchmarking parallel solvers in numerical analysis

Educational demonstrations in ODEs, dynamical systems, and scientific computing

Basis for more complex multi-body or PDE solvers
