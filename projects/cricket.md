---
title: Intelligent Cricket Batting Analysis System
layout: single
permalink: /projects/cricket/
---

## Overview

This project is a **Cognitive AI–driven virtual batting coach** that combines real-time computer vision, biomechanical reasoning, and closed-loop feedback to improve cricket batting technique.

Rather than relying on opaque deep learning models, the system **perceives human posture, reasons over biomechanical constraints, and delivers explainable corrective feedback in real time**, closely mirroring how an experienced human coach observes and teaches.

---

## Problem Statement

Cricket coaching today faces three core limitations:

- Feedback is largely **subjective and coach-dependent**
- Solo practice lacks **real-time corrective guidance**
- Existing video tools provide **delayed, non-explainable insights**

**Objective:**  
Build a **real-time Cognitive AI system** that observes batting posture, reasons about biomechanical correctness, and provides **immediate, interpretable coaching feedback** using only a standard camera.

---

## Cognitive AI Framing

The system follows a classic **perception–reasoning–action loop**, a foundational Cognitive AI paradigm.

### Cognitive Loop
1. **Perception** – Visual sensing via pose estimation
2. **Understanding** – Biomechanical feature representation
3. **Reasoning** – Constraint-based posture evaluation
4. **Decision** – Error detection and correction selection
5. **Action** – Real-time visual coaching feedback
6. **Learning** – Adaptive scoring across practice sessions

This transforms raw video into **context-aware coaching intelligence**.

---

## System Architecture

### Architecture Flow
1. Live video ingestion from camera
2. Real-time pose estimation and landmark tracking
3. Biomechanical feature computation (angles, symmetry, balance)
4. Cognitive reasoning layer evaluates posture quality
5. Corrective feedback rendered on live video stream

### Core Components
- **Visual Perception Layer**
- **Biomechanical Representation Layer**
- **Cognitive Reasoning Engine**
- **Feedback & Scoring System**
- **Real-Time Visualization Interface**

---

## Key Design Decisions

### Pose-Centric, Explainable AI
- Used pose estimation instead of end-to-end video classification
- Enabled **joint-level interpretability**
- Supported explicit reasoning over batting mechanics

### Constraint-Based Cognitive Reasoning
- Rule-based evaluation grounded in cricket biomechanics
- Player-aware tolerance ranges for natural variation
- Fully explainable decisions (no black-box inference)

### Closed-Loop Feedback System
- Immediate feedback strengthens **motor learning**
- Prevents reinforcement of incorrect posture
- Mimics human coach intervention timing

---

## Training Data

### Training Data – Pose & Motion Perception (Set 1)


![Training Data](/assets/TrainDataImage.png)


- Batting videos captured across multiple stances and shot types
- Pose landmarks extracted using real-time pose estimation
- Normalized joint coordinates to handle scale and camera variance
- Annotated biomechanical correctness patterns

### Training Data – Biomechanical Reasoning Features (Set 2)


![TrainingData1](/assests/Traindataimage2.png)


- Joint angles (knees, hips, shoulders, elbows, spine)
- Balance and center-of-mass estimation
- Detection of common technical flaws (head movement, elbow collapse)
- Feature vectors used for posture scoring and consistency tracking

---

## Implementation Details

### Technology Stack (Accurate & Strong)

**Perception & Computer Vision**
- OpenCV (real-time frame acquisition and processing)
- MediaPipe Pose (high-fidelity skeletal landmark extraction)

**Biomechanical Modeling**
- Joint-angle and kinematic feature computation
- Symmetry, balance, and alignment metrics
- Temporal smoothing for motion stability

**Cognitive Reasoning Engine**
- Constraint-based posture validation
- Rule-driven error classification
- Confidence-aware feedback gating

**Backend & Runtime**
- Python
- Streamlit for real-time visualization and UI
- Modular pipeline architecture for extensibility

**Performance & Optimization**
- Low-latency inference pipeline
- Frame skipping for real-time responsiveness
- Stable performance on consumer-grade hardware

---

## Evaluation & Safety

### Evaluation Strategy
- Pose detection reliability across camera angles
- End-to-end latency benchmarking
- Robustness to lighting and background variation

### Safety & Reliability
- Confidence thresholds to suppress uncertain feedback
- Graceful degradation under low pose visibility
- Visual confidence indicators for user trust

---

## Results & Output


![Results](/assets/outputIssues.png)


- Real-time posture correction overlays
- Biomechanical quality scores displayed live
- Immediate corrective cues during batting motion
- Improved posture awareness and consistency

---

## Impact

### Athlete Impact
- Objective, coach-like feedback during solo practice
- Faster correction of biomechanical flaws
- Reinforced motor learning through real-time cues

### Technical Impact
- End-to-end **Cognitive AI system**
- Real-time perception + symbolic reasoning pipeline
- Explainable AI applied to human skill acquisition


