# CS-connectivity

# Example Scripts for Compressive-Sensing-Based Parallel Connectivity Mapping

This repository provides example code for performing **compressive sensing (CS)**-based connectivity reconstruction on experimental data, within the framework of **parallel connectivity mapping**, as described in the article:

> **High-throughput synaptic connectivity mapping using in vivo two-photon holographic optogenetics and compressive sensing**  
> *Chen et al.,* *Nature Neuroscience* (2025)  
> DOI: [10.1038/s41593-025-02024-y](https://doi.org/10.1038/s41593-025-02024-y)


---

## Main Contents
The 'CS_demo.zip' file mainly includes: 

- `CS_demo_code.m`: Main script that runs the full reconstruction and visualization workflow.
- `CS demo sparse FOV.mat`: Example dataset from a sparsely connected field of view.
- `CS demo dense FOV.mat`: Example dataset from a densely connected field of view.

---

## Description

The `.mat` files contain **stimulation-triggered averages (STAs)** of the postsynaptic currents evoked under both **sequential** and **parallel** stimulation protocols. These data are used to reconstruct individual synaptic inputs using the **CVX MATLAB package** for convex optimization.

The script performs the following:

1. Loads STA data for sequential and parallel stimulation.
2. Uses CVX to solve an optimization problem that estimates synaptic inputs based on the parallel stimulation responses.
3. Compares the reconstructed connectivity to the "ground truth" obtained from single-cell stimulation.
4. Plots a summary graph and generates a confusion matrix for evaluation.

---

Additional code used in the same article—for performing and simulating CS-based mapping on model networks—is available at:  
🔗 [https://github.com/Oweiss-Lab/Compressed-Sensing-Connectivity-Mapping](https://github.com/Oweiss-Lab/Compressed-Sensing-Connectivity-Mapping)

## Requirements

- MATLAB
- [CVX](http://cvxr.com/cvx/) (for convex optimization)

---
