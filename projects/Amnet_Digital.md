---
title: Applied Machine Learning Systems (Amnet Digital)
layout: single
permalink: /projects/Amnet_Digital/
---

## Problem Statement

Business teams at Amnet Digital required **scalable, production-ready machine learning systems** to support customer segmentation, churn prediction, and recommendation use cases across marketing and customer engagement workflows.

Existing approaches were largely ad-hoc, lacked monitoring, and were not designed to handle **data drift, model degradation, or production integration**, resulting in unreliable predictions over time.

The objective was to design and deploy **end-to-end ML pipelines** that could operate reliably in production, integrate seamlessly with downstream applications, and continuously maintain model quality.

---

## System Architecture

The solution followed a **modular ML production architecture** designed for robustness and extensibility:

### Architecture Flow
1. Raw data ingested from transactional and behavioral data sources
2. Data preprocessing and feature engineering pipelines generate model-ready features
3. Supervised models trained and validated using offline evaluation workflows
4. Trained models deployed behind FastAPI-based inference services
5. Predictions consumed by downstream business applications
6. Monitoring pipelines track performance, stability, and drift
7. Retraining workflows triggered based on degradation signals

### Core Components
- **Data Processing Layer:** Cleaning, normalization, and feature extraction
- **Model Training Layer:** Classical ML, NLP, and CNN-based pipelines
- **Inference Layer:** API-based real-time prediction services
- **Monitoring Layer:** Performance metrics and drift detection

---

## Design Decisions

### Model Selection Based on Data Characteristics
Different modeling approaches were selected based on input data types and business requirements:
- **Classical ML models** for structured tabular data
- **NLP models** for text-based classification and segmentation
- **CNN-based models** for image-related classification tasks

This ensured optimal performance while maintaining interpretability where required.

### API-First Deployment Strategy
Models were exposed via **FastAPI-based inference services** to:
- Decouple model lifecycle from consuming systems
- Enable real-time and batch prediction use cases
- Simplify integration with business applications

### Monitoring as a First-Class Concern
Model accuracy alone was insufficient for production reliability.
Monitoring was built into the system to detect:
- Data distribution shifts
- Performance degradation
- Unexpected prediction behavior

---

## Implementation Details

### Tech Stack

**Languages**
- Python

**Machine Learning**
- scikit-learn
- XGBoost
- CNN-based models for computer vision tasks

**Natural Language Processing**
- TF-IDF
- Embedding-based representations

**Inference & APIs**
- FastAPI
- REST-based prediction endpoints

**Data Layer**
- SQL-based structured data stores
- Feature tables for training and inference consistency

**Monitoring & Evaluation**
- Custom performance dashboards
- Drift detection on input features and predictions

---

## Evaluation & Safety

### Model Evaluation
- Precision, recall, F1-score for classification tasks
- Offline cross-validation prior to deployment
- Online performance tracking post-deployment

### Drift & Stability Monitoring
- Feature distribution drift detection
- Prediction distribution monitoring
- Alerting on statistically significant deviations

### Deployment Safety
- Canary deployments for model updates
- Gradual rollout with rollback support
- Controlled retraining and redeployment workflows

---

## Impact

### Business Outcomes
- Improved prediction accuracy across customer segmentation and churn models
- More reliable recommendation outputs for downstream systems
- Reduced manual intervention due to automated monitoring and retraining triggers

### Operational Impact
- Stabilized ML performance in production environments
- Reduced model degradation over time
- Enabled consistent, data-driven decision-making across teams

### Engineering Impact
- Established reusable ML production patterns
- Created a foundation for future ML system expansion
- Improved collaboration between ML and application teams
