# Krylov Subspace Methods using Arnoldi Orthogonalization

## Overview
Krylov subspace methods are iterative techniques for solving large sparse linear systems of the form \( Ax = b \). These methods construct a sequence of approximations by projecting the solution onto a Krylov subspace \( K_m(A, r_0) = \text{span} \{ r_0, Ar_0, A^2r_0, \dots, A^{m-1}r_0 \} \), where \( r_0 \) is the initial residual. The Arnoldi process is used to generate an orthonormal basis for this subspace, leading to more stable numerical computations.

Two widely used Krylov methods are:
- **Full Orthogonalization Method (FOM)**: Solves \( Ax = b \) by minimizing the residual within the Krylov subspace, using the Arnoldi process.
- **Generalized Minimal Residual Method (GMRES)**: Minimizes the residual norm at each iteration, leading to robust convergence properties, especially for non-symmetric systems.

This repository contains implementations of these methods and their restarted versions, along with example results demonstrating their behavior on test problems.

## Contents
- `gmres.py` - Implementation of the GMRES method
- `fom.py` - Implementation of the Full Orthogonalization Method (FOM)
- `restarted_gmres.py` - GMRES with restart
- `restarted_fom.py` - FOM with restart
- `example_results/` - Sample results from running the methods on test problems
- `README.md` - This file

