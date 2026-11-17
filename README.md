# Environmental Monitoring and Data Analysis

This is Micks copy of the Course Environmentl Modeling and Data Science.

Course material for the Master's course *Environmental Monitoring and Data Analysis*
(1st semester, environmental science), Chair of Sensor-based Geoinformatics,
University of Freiburg. Lab website: <https://uni-freiburg.de/enr-geosense>

The course runs weekly on Fridays. In each block there is about two hours of teaching and
about two hours of assignment work. Everything you need for the assignments is in this repository.


## What is in this repository

| Folder | Content |
| --- | --- |
| `assignments/` | The assignment sheets, one per block |
| `scripts/` | Small example scripts in R and Python |
| `jobs/` | Slurm job scripts for bwUniCluster |
| `docs/` | Notes and templates, for example `STORAGE_TEMPLATE.md` |
| `ssh-connection/` | Guide to connect to bwUniCluster with SSH ([read it online](https://negin-katal.github.io/datascience_env_monit/ssh-connection/)) |
| `flux4student/` | FLUXNET site explorer and the weekly data used in the course ([open it online](https://negin-katal.github.io/datascience_env_monit/flux4student/)) |

Last edited Nov. 2026

## Block 4 – FLUXNET data summary

### Requirements

Python 3.9 or newer and the following packages:

```bash
python -m pip install pandas numpy matplotlib seaborn geopandas scipy nbconvert
```

### Data

Place the five FLUXNET ZIP files in `data/raw/` and the metadata snapshot CSV in `data/snapshots/`.

The data directory is excluded from Git and must be supplied separately.

### Render the report

From the repository root, run:

```bash
python -m nbconvert --to html --execute --embed-images --ExecutePreprocessor.timeout=600 reports/block4_data_summary.ipynb
```

This executes the notebook and creates:

```text
reports/block4_data_summary.html
```

The HTML report contains the executed analysis and embedded figures.