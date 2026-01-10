# Cyclist Census

Computer vision research for automated cyclist counting and demographic analysis from urban CCTV footage - methodology, findings, and implementation links


## Overview

This research project presents an end-to-end computer vision pipeline for automated cyclist census generation from urban CCTV footage. The system combines state-of-the-art object detection (YOLO/RFDETR), multi-object tracking (ByteTrack), and deep learning-based classification (EfficientNet/ResNet) to produce detailed cyclist mobility data including gender demographics and bike lane compliance metrics.

Developed to support urban transportation planning and policy decisions, the pipeline processes hours of video footage to generate temporal count data that would be prohibitively expensive to collect manually. The system handles challenging real-world conditions including variable lighting, occlusions, and high traffic density typical of urban intersections.

Key capabilities include directional counting across multiple lanes, real-time gender classification with temporal aggregation, automated bike lane compliance tracking, and checkpoint-based processing designed for resource-constrained environments (Google Colab free tier). The complete methodology spans dataset preparation, model training, hyperparameter optimization, and production deployment.

## Sample Results

![Sample Output](figs/examples/annotated_frame_sample.png)
*Real-time cyclist detection, tracking, and demographic classification with directional counting*

<br>

## Research Context

### Institution

[![Universidad de Buenos Aires](figs/logos/uba_logo.png)](https://www.uba.ar/)

**Universidad de Buenos Aires (University of Buenos Aires)**

This project was completed as the capstone project for the [Graduate Specialization in Artificial Intelligence](https://lse-posgrados.fi.uba.ar/posgrados/especializaciones/ceia) at the School of Engineering, University of Buenos Aires. The specialization serves as the first-year intermediate degree toward the [Master's in Artificial Intelligence](https://lse-posgrados.fi.uba.ar/posgrados/maestrias/mia) at the same institution. The project was submitted for approval and grading in October 2025.

### Collaboration

[![Ente de la Movilidad de Rosario](figs/logos/emr_logo.png)](https://emr.gov.ar/)

**Ente de la Movilidad de Rosario (Rosario Mobility Authority)**

This research was conducted in collaboration with the Rosario Mobility Authority, where the author worked as a Transportation Data Scientist from November 2022 to August 2024 before pursuing graduate studies abroad. The Ente de la Movilidad is an autonomous decentralized agency responsible for comprehensive urban mobility management across all transportation modes, including mass transit, individual and special transport services, non-motorized transport, and private vehicle use. The organization is characterized by its technical expertise and multidisciplinary approach to addressing mobility challenges through evidence-based, sustainability-focused policies.

### Project Motivation

The Rosario Mobility Authority conducts manual cyclist censuses at strategic locations throughout the city. Field workers observe traffic flow at selected intersections during 15-minute intervals, recording counts on paper forms. Data collection includes vehicle counts by category (cars, buses, motorcycles, bicycles, scooters), infrastructure compliance (bike lane vs. roadway usage), bicycle type (personal vs. public bike-share), and demographic characteristics (gender, age group) of cyclists.

These censuses are essential for urban mobility decision-making, providing systematic data to evaluate infrastructure performance, identify high-traffic zones for prioritized improvements, and design evidence-based public policies. Consistent periodic collection enables temporal analysis to monitor transportation system evolution, identify trends, and evaluate intervention impacts over time.

However, the manual methodology presents significant limitations:

- **Resource intensive**: Requires substantial human resources through temporary census workers or reassignment of qualified technical staff to tasks that underutilize their expertise
- **Verification challenges**: Difficult to validate anomalous or inconsistent data post-collection without the ability to review the original scene
- **Human error**: Subject to recording mistakes and subjective interpretation variability, particularly in demographic classification
- **Safety constraints**: Urban security concerns prevent data collection in certain areas or times of day, limiting spatial and temporal coverage

This context motivates the exploration of technological alternatives to automate cyclist censuses using existing infrastructure—specifically, the city's CCTV surveillance camera network. Reliable, accurate, and frequent cyclist mobility data is fundamental for planning adequate infrastructure, improving road safety, evaluating public policies, and promoting sustainable transportation. Computer vision-based automation represents a concrete opportunity to modernize data collection systems and advance toward more intelligent urban mobility management.
