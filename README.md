## TADF_Pizza_Troisi_Capobianco

This repository contains the Python, C and bash scripts used to perform the calculations presented in the manuscript:

> Pizza, Teodoro and Troisi, Alessandro and Capobianco, Amedeo. "Computation of Non-Radiative Rates for High-Throughput Virtual Screening: Application to Discovery of Potential TADF Molecules" *Journal of Chemical Theory and Computation*. DOI: https://doi.org/10.1021/acs.jctc.6c00881

If you use this code or data, please cite the article above.

## Repository structure

```
.
├── README.md
├── software.zip/
│   ├── check_func.py        # Python script: called by main_func.py, contains all kinds of check functions (e.g., convergence, connectivity etc.)
│   ├── move_mode_single.c   # C script: shift the coordinates of the normal mode corresponding to an imaginary frequency
│   ├── creafile              # bash script: creates SLURM files for the cluster used by the authors
│   ├── main_func.py          # Python script: main function
│   └── mylib.py               # Python script: library called by main_func.py
├── Dusch_Mat_xxx.txt          # Text file containing the Duschinsky matrices for the xxx molecule
├── Molecules_XYZ.zip/         # Molecules' XYZ files
├── removed_molecule_sample.log
└── sample.log                 # Example log files
```

## Contents description

- **software.zip**: archive containing the core scripts used to run the calculations.
  - **check_func.py**: Python script called by `main_func.py`; contains various check functions (e.g. convergence checks, connectivity checks, etc.).
  - **move_mode_single.c**: C script that shifts the coordinates along the normal mode corresponding to an imaginary frequency.
  - **creafile**: bash script that generates SLURM submission files for the cluster used by the authors.
  - **main_func.py**: Python script implementing the main workflow.
  - **mylib.py**: Python library of functions called by `main_func.py`.
- **Dusch_Mat_xxx.txt**: text file containing the Duschinsky matrix computed for the molecule "xxx" (file name reflects the specific molecule).
- **Molecules_XYZ.zip**: archive containing the XYZ coordinate files of the molecules studied.
- **sample.log**: example log file illustrating the expected output format.
- **removed_molecule_sample.log**: example log file for a molecule excluded from the screening (e.g. due to failed checks).

## Citation

Teodoro Pizza, Alessandro Troisi, Amedeo Capobianco; Computation of Nonradiative Rates for High-Throughput Virtual Screening: Application to the Discovery of Potential TADF Molecules. J. Chem. Theory Comput. 2026

```
DOI:  https://doi.org/10.1021/acs.jctc.6c00881
```
