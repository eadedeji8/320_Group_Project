# NYC Motor Vehicle Collisions — Data Science Tutorial
### CMSC 320: Introduction to Data Science | Spring 2026 | University of Maryland

**Authors:** Miskay Zelalem, Dinna Yeshitlla, Emmanuel Michael, Emmanuel Adedeji, Daniel Odetoye

**Live tutorial:** _TBD — `https://<username>.github.io/<repo>/crashes.html` once GitHub Pages is enabled (see [Publishing](#publishing) below)._

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

## Publishing

This tutorial is intended to be served via GitHub Pages. The publishing checklist is in the chat output that produced the merged notebook; the short version:

1. Create a `<username>.github.io` GitHub repo (or use an existing one).
2. Run the notebook end-to-end once locally so cell outputs and PNGs are populated.
3. Regenerate `crashes.html` via `jupyter nbconvert --to html crashes.ipynb`.
4. Push `crashes.ipynb`, `crashes.html`, the four `*.png` files, and `README.md`.
5. Enable Pages from the `main` branch root in repo settings.
6. Replace the `Live tutorial` URL above with the actual Pages URL.
