---
layout: note
title: Computational Chemistry & Molecular Modeling
description: Key concepts in quantum mechanics, molecular mechanics, and computational tools.
category: college
course: BACHY105
date: 2026-11-20
tags: [chemistry, computational, molecular-modeling]
pdf: /assets/pdf/example_pdf.pdf
tex: /assets/tex/computational-chemistry.tex
---

## Overview

Computational chemistry utilizes computer simulation to solve chemical problems, calculate molecular structures, and predict physical properties.

### Key Approaches

1. **Molecular Mechanics (MM):**
   - Treats atoms as balls and bonds as springs (force field methods).
   - Fast and computationally inexpensive; ideal for large biomolecules.
   - Does not account for electronic transitions or bond formation/breaking.

2. **Electronic Structure Methods (Quantum Mechanics):**
   - **Ab Initio:** Solves the Schrödinger equation from first principles (Hartree-Fock, Post-HF methods like MP2, CCSD).
   - **Density Functional Theory (DFT):** Calculates electron density rather than multi-electron wavefunctions (e.g., B3LYP functional). Excellent balance of accuracy and computational cost.
   - **Semi-Empirical Methods:** Uses empirical parameters to approximate complex integrals (AM1, PM3).

### Practical Applications

- Drug discovery and protein-ligand docking.
- Transition state analysis and reaction kinetics.
- Spectroscopic property prediction (IR, NMR, UV-Vis).
