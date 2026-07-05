# MDR Structural Genomics: NMR Analysis of Stress Response Proteins

![PDB 5X1X](https://img.shields.io/badge/PDB-5X1X-blue)
![Python](https://img.shields.io/badge/Python-3.8+-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

This repository contains Python scripts for the **structural characterization of stress response proteins** from multidrug-resistant (MDR) bacteria, including:

- **MRSA252** (*Staphylococcus aureus*)
- **Klebsiella pneumoniae** (ATCC 700603)  
- **Pseudomonas aeruginosa** (PAO1)

The centerpiece is the **NMR structure of Nudix hydrolase** from MRSA252, deposited as **PDB 5X1X**—the first structure of this "housekeeping" enzyme from *S. aureus*.

## Project Overview

| Feature | Details |
| :--- | :--- |
| **Target Proteins** | Nudix hydrolase, Anti-sigma-B antagonist, Hypothetical protein (UPF0355), Methyltransferase |
| **Organisms** | *S. aureus* MRSA252, *K. pneumoniae*, *P. aeruginosa* |
| **Method** | Solution NMR Spectroscopy (800 MHz) |
| **PDB ID** | [5X1X](https://doi.org/10.2210/pdb5X1X/pdb) |
| **Clones** | 60+ genes cloned for structural characterization |

## What This Repository Contains

- `structure_validation.py` — Ramachandran plot, RMSD, and secondary structure analysis for PDB 5X1X
- `chemical_shift_analysis.py` — Analysis of chemical shift perturbations from ligand binding (metal ions and nucleotides)
- `data/` — PDB files, chemical shift assignments, and peak lists
- `results/figures/` — Generated validation plots and interaction heatmaps

## Key Results

- **NMR Structure Solved**: 3 α-helices, 4 β-strands (globular fold)
- **78.5%** of residues in most favorable Ramachandran region
- **Binding identified** for metal ions (Mg²⁺, Ca²⁺, Zn²⁺) and nucleotides (AMP, ATP, GMP, CTP)
- **Active site** localized to the α1 helix

## Quick Start

```bash
# Clone this repository
git clone https://github.com/durre414622/mdr-structural-genomics.git
cd mdr-structural-genomics

# Install dependencies
pip install biopython matplotlib numpy

# Run structure validation
python structure_validation.py
