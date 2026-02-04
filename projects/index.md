---
layout: page
title: "Projects"
permalink: /projects/
---

This page documents **end-to-end systems** I’ve designed and built, with
emphasis on architecture, trade-offs, and production constraints.

---
<hr style="margin: 2em 0;">
## <a id="elitecontent"></a> EliteContent – Full-Stack Generative AI Platform

### Overview
EliteContent is a comprehensive Generative AI platform I built from the ground up, enabling users to generate high-quality resumes, documents, emails, and research content powered by advanced AI techniques including RAG and multi-agent refinement.
### Problem Statement
Content generation tools often produce generic, context-poor outputs that require significant manual editing. Users need AI-generated content that is grounded in relevant context, maintains quality standards, and can be customized to specific use cases.
Solution Architecture

### Full-Stack Development
I developed the complete platform using Angular for a responsive, intuitive frontend and FastAPI for a high-performance backend API layer. The architecture separates concerns cleanly, enabling independent scaling and rapid iteration.

### RAG Pipeline Implementation
I implemented Retrieval-Augmented Generation pipelines using ChromaDB as the vector store. When users request content generation, the system retrieves semantically relevant context from stored documents, grounding LLM responses in factual, personalized information rather than relying solely on the model's parametric knowledge.

### MCP-Based Context Control
I integrated Model Context Protocol (MCP) to give fine-grained control over what context is provided to the LLM at inference time. This ensures generated content stays focused, relevant, and aligned with user intent.
Production-Ready API Design
I built scalable APIs with enterprise-grade features:

### Caching: Reduced latency and costs for repeated queries
Rate Limiting: Protected against abuse and ensured fair usage
Authentication: Secured endpoints with token-based auth
Multi-Agent Quality Refinement: Implemented agent workflows where specialized agents review and improve generated content before delivery

### Key Features

AI-powered resume generation with context from user profiles
Document and email drafting with customizable tone and style
Research content synthesis from multiple sources
Quality assurance through multi-agent review pipelines

### Technologies
Angular FastAPI Python ChromaDB RAG MCP LLMs Vector Search REST APIs
---
<hr style="margin: 2em 0;">
## <a id="cricket"></a> Intelligent Cricket Batting Analysis System

### Overview
I created an AI-powered cricket coaching assistant that combines computer vision and cognitive feedback models to help batsmen improve their technique through real-time, personalized coaching cues.

### Problem Statement
Traditional cricket coaching relies on subjective observation and delayed feedback. Batsmen often struggle to identify and correct subtle technical flaws in their stance, grip, backlift, or shot execution without expert guidance—which isn't always accessible or affordable.
Solution Architecture

### Computer Vision Pipeline
I built a vision system that captures and analyzes batting motions in real-time. The system detects key body landmarks, tracks bat position and movement, and compares the observed mechanics against ideal batting technique models.

### Biomechanical Deviation Detection
The core intelligence lies in mapping observed movements to a biomechanical model of correct batting technique. The system identifies deviations—whether in stance width, backlift angle, head position, or follow-through—and quantifies how far each parameter strays from optimal form.

### Adaptive Reinforcement Logic
Rather than providing generic feedback, I implemented adaptive reinforcement algorithms that accelerate motor learning:

#### Personalized Coaching Cues: Feedback is tailored to each user's specific weaknesses and learning style
Progressive Difficulty: The system adjusts expectations as the user improves
Real-Time Corrections: Immediate feedback helps users build muscle memory faster than delayed review

#### Cognitive Feedback Models
I integrated cognitive science principles into the feedback loop, ensuring corrections are delivered in ways that maximize retention and skill transfer—using cues that are actionable, specific, and appropriately timed.
Key Features

Real-time batting motion capture and analysis
Automated detection of technical flaws
Personalized coaching recommendations
Progress tracking and improvement metrics
Adaptive difficulty based on skill level

### Technologies
Python Computer Vision OpenCV Deep Learning CNNs Pose Estimation Reinforcement Learning
---
<hr style="margin: 2em 0;">
## <a id="enterprise-genai"></a> Enterprise Generative AI Systems

### Overview
As a Senior ML & Gen AI Engineer at one of the world's largest financial institutions, I lead the design and deployment of enterprise-scale Generative AI systems that power intelligent, context-aware capabilities across critical business workflows.
Key Responsibilities & Achievements

### Enterprise Generative AI Architecture
I architect and deploy production-grade Generative AI systems that leverage Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), and Model Context Protocol (MCP). These systems deliver secure, governed AI capabilities that meet the stringent compliance and security requirements of the financial services industry.

### Advanced LLM Workflow Implementation
I design and implement sophisticated LLM workflows that go beyond simple prompt-response patterns. This includes building prompt orchestration systems for complex multi-step reasoning, implementing prompt versioning for reproducibility and A/B testing, developing comprehensive evaluation frameworks to measure model quality, and integrating bias detection and safety guardrails to ensure responsible AI deployment.

### Real-Time ML Infrastructure
I architect low-latency ML data flows that seamlessly integrate multiple data sources and systems—including event streams for real-time data ingestion, document stores for unstructured content, vector databases for semantic search, and managed LLM platforms for inference. This infrastructure enables AI-driven interactions that respond in real-time to user needs.

### Cloud-Native ML Operations
I deploy and operate production ML services on AWS and Kubernetes, implementing autoscaling policies to handle variable workloads, observability stacks for monitoring and debugging, and reliability patterns that ensure high availability for enterprise workloads.

### Cross-Functional Leadership
I partner closely with engineering, data, and business teams to communicate architectural decisions, evaluate trade-offs, and drive adoption of shared AI platforms across the organization. I delivered a reference architecture for production-grade, governed Generative AI systems that now serves as a blueprint for AI initiatives across the enterprise.

### Technologies
Python LLMs RAG MCP AWS Kubernetes Vector Databases Prompt Engineering MLOps

---
<hr style="margin: 2em 0;">
## <a id="applied-ml"></a> Applied Machine Learning Systems 

### Overview
As a Machine Learning Engineer, I built and deployed end-to-end ML solutions for classification, recommendation, and NLP use cases—owning the full lifecycle from data preprocessing and feature engineering to model training, deployment, and monitoring.

### Key Responsibilities & Achievements
#### End-to-End ML Pipeline Development
I designed and implemented complete machine learning pipelines that transformed raw data into production-ready predictions. This involved building robust data preprocessing workflows, engineering discriminative features, training and tuning models, and deploying inference services that integrated seamlessly with existing systems.
Model Development & Optimization
I developed and optimized a wide range of ML models tailored to specific business problems:

##### Classification Models: Logistic Regression, Random Forest, and XGBoost for customer segmentation and churn prediction
##### Deep Learning: Convolutional Neural Networks (CNNs) for image classification tasks
##### NLP Solutions: TF-IDF and embedding-based models for text classification and semantic similarity scoring
##### Recommendation Systems: Collaborative and content-based filtering for personalized recommendations

### Production ML Services
I exposed trained models via FastAPI-based REST APIs, enabling real-time inference for downstream applications. I collaborated closely with data engineering teams to ensure reliable data pipelines fed consistent, high-quality data to production models.
MLOps & Model Governance
I implemented foundational MLOps practices to maintain model health in production, including experiment tracking to compare model iterations, model versioning for reproducibility and rollback capabilities, CI/CD pipelines for automated testing and deployment, and monitoring dashboards to detect data drift and performance degradation.

### Technologies
Python Scikit-learn XGBoost TensorFlow PyTorch FastAPI SQL Pandas NumPy CNNs NLP
---
<hr style="margin: 2em 0;">
## <a id="evaluation"></a> LLM Evaluation & Safety

### Problem
LLM output quality is difficult to measure and control in production.

### Evaluation Strategy
- Automated checks for low-quality outputs
- Preference signals from users
- Human-in-the-loop review
- Continuous feedback loops

### Why This Matters
Evaluation is the primary lever for improving
LLM reliability, alignment, and trust.
