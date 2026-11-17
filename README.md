# Environmental Monitoring and Data Analysis

This repository contains Mick's copy of the course materials for *Environmental Monitoring and Data Analysis*, a Master's course in Environmental Sciences (1st semester) at the Chair of Sensor-based Geoinformatics, University of Freiburg.

[Course website](https://uni-freiburg.de/enr-geosense)

The course takes place weekly on Fridays. Each block combines approximately two hours of teaching and two hours of practical assignment work.

## Repository structure

| Folder | Content |
|---|---|
| `assignments/` | Assignment sheets for each block |
| `scripts/` | Example scripts in R and Python |
| `jobs/` | Slurm job scripts for bwUniCluster |
| `docs/` | Documentation and templates |
| `ssh-connection/` | Guide to connecting to bwUniCluster via SSH |
| `flux4student/` | FLUXNET site explorer and weekly course data |
| `reports/` | Jupyter notebooks and generated analysis reports |

## Block 4 – FLUXNET data summary

The Block 4 report provides an overview and quality assessment of FLUXNET data.

### Requirements

Python 3.9 or newer. Install the required packages:

```bash
python -m pip install pandas numpy matplotlib seaborn geopandas scipy nbconvert
```

### Data

Place the five FLUXNET ZIP files in `data/raw/` and the metadata snapshot CSV in `data/snapshots/`.

The `data/` directory is excluded from Git and must be supplied separately.

### Run and export the report

From the repository root:

```bash
python -m nbconvert --to html --execute --embed-images --ExecutePreprocessor.timeout=600 reports/block4_data_summary.ipynb
```

This executes the notebook and generates `reports/block4_data_summary.html`, containing the analysis and embedded figures.

---

Last updated: November 2026