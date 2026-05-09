# NYC Motor Vehicle Collisions — Data Science Tutorial
### CMSC 320: Introduction to Data Science | Spring 2026 | University of Maryland

**Authors:** Miskay Zelalem, Dinna Yeshitlla, Emmanuel Michael, Emmanuel Adedeji, Daniel Odetoye

**Live tutorial:** https://eadedeji8.github.io/320_Group_Project/

---

## Overview

This repository hosts our final tutorial for the NYC Motor Vehicle Collisions (Crashes) dataset published by the NYPD on [NYC Open Data](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95). The tutorial walks through the full data science pipeline — acquisition and cleaning of ~2.25M crash records, exploratory data analysis across boroughs and time of day, a Welch's t-test on night-vs-day crash severity, and a binary classifier (Logistic Regression baseline + Random Forest) that predicts whether a crash will result in at least one injury given borough, hour, contributing factor, and vehicle type. The end-to-end story connects spatial / temporal patterns in NYC traffic to concrete policy implications for the city's [Vision Zero](https://www.nyc.gov/site/visionzero/index.page) initiative.

---

## Dataset

- **Source:** [NYC Open Data — Motor Vehicle Collisions (Crashes)](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)
- **Reported by:** New York Police Department (NYPD), via form MV-104AN
- **Size:** 2,252,143 rows × 29 columns; cleaned working set is 1,564,912 × 12
- **Features used:** crash date/time, borough, latitude/longitude, contributing factor (vehicle 1), vehicle type (vehicle 1), persons injured/killed counts

The CSV is gitignored because of size — see the notebook for the loader call.

---

## Files in this repo

| File | Purpose |
|---|---|
| `crashes.ipynb` | The single self-contained tutorial notebook (Sections I–VI + Sources). |
| `crashes.html` | Static export of `crashes.ipynb` — what GitHub Pages serves. Regenerate with `jupyter nbconvert --to html crashes.ipynb` after any edit. |
| `Final Project Assignment-2-2.pdf` | The assignment rubric. |
| `confusion_matrices.png`, `roc_curves.png`, `feature_importance.png`, `classification_report.png` | Saved by `plt.savefig()` calls in Section V; embedded by the HTML export. |
| `README.md` | This file. |

---
