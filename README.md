# GNN-for-Graphs

Planar Graph Permutation & Conditional GNN

Overview

This project explores generating graphs with chromatic number 7 or 8 or 9
using planar graphs, vertex permutations, and a conditional GNN-GAN.

Notebooks

1. Planar Graph Permutation

Planar Graph Permutation for Chromatic 7-8–9 Generation and Balanced Dataset Augmentation.ipynb

Takes planar graph (L_1) as input.

Randomly permutes 10 vertices.

Computes Computes (L1) ∪ π(L1)

Keeps samples with chromatic number 8 or 9.

Creates a balanced augmented dataset of about 5,000 samples.

Main outputs: - planar_permutation_results_final.csv -
augmented_5000_planar_permutation_results.csv

2. Conditional GNN-GAN

GAN — L1 Matrix + Random Noise → New Graph.ipynb

Uses (L_1) adjacency matrices and random noise as input.

Trains a conditional GNN-GAN to generate new graphs.

Tests the generated graph, its permutation, and their union.

Checks planarity and chromatic number.

Supports large-scale generation and filtering for chromatic number
8 or 9.

Main outputs: - Conditional_GNN_GAN_ALL_GENERATED.csv -
Conditional_GNN_GAN_50000_VERIFIED.csv -
Conditional_GNN_GAN_50000_CHI8_CHI9.csv

Workflow

Planar Graphs
     ↓
Vertex Permutation
     ↓
χ = 8 / 9 Samples
     ↓
5,000-Sample Dataset
     ↓
Conditional GNN-GAN
     ↓
Generated Graphs
     ↓
Planarity & Chromatic Verification
     ↓
χ = 8 / 9 Graphs

Technologies

Python

PyTorch

NetworkX

NumPy / Pandas

C++

Boost Graph Library

Google Colab

Objective

To investigate whether conditional graph generation can produce new
graph structures whose union with a vertex-permuted copy achieves high
chromatic numbers, particularly χ = 7 or 8 or 9.

Note: Vertex labels are maintained using 1-based indexing in the
project outputs.
