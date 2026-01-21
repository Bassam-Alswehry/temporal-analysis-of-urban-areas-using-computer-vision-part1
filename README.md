# Temporal Analysis of Urban Areas Using Computer Vision – Part 1

This project explores **temporal urban change detection** using classical computer vision techniques.
The goal is to measure and rank visual changes in urban areas across different years using street-level imagery.

This repository represents **Part 1** of a multi-stage project focused on *Temporal Intelligence* for urban environments.

---

## Project Objective
- Detect **visual changes over time** in urban scenes
- Reduce false positives caused by lighting and camera shifts
- Produce **interpretable change scores** instead of black-box predictions

---

## Core Methodology
The system compares a **baseline image (2014)** against later years using:

- **Edge Change Detection** (Canny + absolute difference)
- **Structural Similarity Approximation (SSIM-like metric)**
- **Dynamic weighting strategy** based on:
  - Brightness difference
  - Image sharpness
- **Image alignment (ECC)** to correct camera viewpoint shifts
- **Center ROI cropping** to focus on stable spatial regions
