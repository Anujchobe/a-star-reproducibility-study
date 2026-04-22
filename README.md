# A* Reproducibility Study: Heuristic Sensitivity and Practical Performance Tradeoffs

This repository contains the final capstone project for CS5100 – Foundations of Artificial Intelligence at Northeastern University.

## Project Overview

This project reproduces and evaluates the key claims of the original A* paper:

**Hart, Nilsson, Raphael (1968)**  
*A Formal Basis for the Heuristic Determination of Minimum Cost Paths*

The study compares:

- Uniform Cost Search (UCS)
- Standard A* Search
- Weighted A* Search

using procedurally generated Gridworld environments.

## Objectives

- Validate that A* preserves optimality with an admissible heuristic
- Measure reduction in search effort compared to UCS
- Analyze heuristic sensitivity using Weighted A*
- Compare behavior across increasing environment difficulty

## Algorithms

### Uniform Cost Search
Uses path cost only:

f(n) = g(n)

### A* Search

f(n) = g(n) + h(n)

### Weighted A*

f(n) = g(n) + εh(n)

where ε > 1

## Experimental Environments

| Grid Size | Obstacle Density | Difficulty |
|----------|------------------|-----------|
| 15x15 | 0.10 | Easy |
| 20x20 | 0.20 | Medium |
| 30x30 | 0.25 | Hard |

## Metrics Collected

- Path Cost
- Nodes Expanded
- Runtime
- Peak Frontier Size
- Solved Instances

## Results Summary

Main findings:

- A* consistently matched UCS path quality
- A* reduced node expansions and runtime
- Weighted A* was faster but sometimes less optimal
- Tradeoff becomes stronger in harder environments

## Repository Structure

```text
Chobe_Capstone.ipynb         # Main Google Colab notebook
results_15x15_d010.csv      # Easy benchmark results
results_20x20_d020.csv      # Medium benchmark results
results_30x30_d025.csv      # Hard benchmark results
Final_Report.pdf            # Final written report
