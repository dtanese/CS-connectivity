# CS-connectivity
Example scripts for compressive-sensing-based parallel connectivity mapping.

This repository provides example code for performing compressive sensing (CS)-based connectivity reconstruction within the framework of parallel connectivity mapping, as described in the article  Chen et al. "High-throughput synaptic connectivity 
mapping using in vivo two-photon holographic optogenetics and  compressive sensing", published in Nature Neuroscience (2025). 

The provided scripts cover the key steps to generate the representative graphs shown in Figure 4a and 4b of the paper. All necessary experimental data are included in the zip archive.

Main Contents:

CS_demo_code.m: Main script that runs the full reconstruction and visualization workflow.

CS demo sparse FOV.mat: Example dataset from a sparsely connected field of view.

CS demo dense FOV.mat: Example dataset from a densely connected field of view.


Description

The .mat files contain stimulation-triggered averages (STAs) of the postsynaptic currents evoked under both sequential and parallel stimulation protocols. These data are used to reconstruct individual synaptic inputs using the CVX MATLAB package for convex optimization.  The script performs the following:

Loads STA data for sequential and parallel stimulation.
Uses CVX to solve an optimization problem that estimates synaptic inputs based on the parallel stimulation responses.
Compares the reconstructed connectivity to the "ground truth" obtained from single-cell stimulation.
Plots a summary graph and generates a confusion matrix for evaluation.
