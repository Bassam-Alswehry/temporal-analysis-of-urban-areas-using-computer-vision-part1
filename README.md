# Temporal Analysis of Urban Areas Using Computer Vision – Part 1

This project explores temporal urban change detection using classical computer vision techniques. The goal is to measure and rank visual changes in urban areas across different years using satellite imagery.

This repository represents Part 1 of a multi-stage project focused on **Temporal Intelligence for urban environments**, combining computer vision with backend system integration.

---

## Project Objective

- Detect visual changes over time in urban scenes  
- Reduce false positives caused by lighting and environmental variations  
- Produce interpretable change scores instead of black-box predictions  
- Build a foundation for a system that supports data-driven decision making  

---

## Core Methodology

The system compares a baseline image (2014) against later years using:

- Edge Change Detection (Canny + absolute difference)  
- Structural Similarity Approximation (SSIM-like metric)  
- Dynamic weighting strategy based on:
  - Brightness difference  
  - Image sharpness  
- Image alignment (ECC) to correct viewpoint shifts  
- Center ROI cropping to focus on stable spatial regions  

---

## System Architecture (Extension)

To move beyond analysis, a simple backend system was integrated:

- Built a basic REST API using FastAPI  
- Implemented endpoints to simulate request/response flow  
- Stored processed results in MongoDB as JSON-like documents  
- Exported results to JSON file for portability and reuse  

### System Flow

Client → FastAPI → Backend Processing → MongoDB → Response

---

## Key Outputs

- Change score (0–1) representing structural variation  
- Ranked comparisons across locations and years  
- Visualizations (bar charts, heatmaps)  
- JSON and CSV outputs for further analysis  

---

## Technologies Used

- Python  
- OpenCV  
- NumPy / Pandas  
- Matplotlib  
- FastAPI  
- MongoDB  

---

## Future Work

- Convert analysis into real-time API (POST /analyze)  
- Deploy system on cloud with public access  
- Add automation layer for decision-making workflows  
- Build dashboard for interactive exploration  
