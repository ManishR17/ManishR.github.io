---
title: Enterprise RAG Platform (Ericsson)
layout: single
permalink: /projects/enterprise-rag-platform/
---

## Problem Statement

Ericsson engineering teams relied on thousands of technical documents including operational runbooks, incident reports, troubleshooting guides, and network procedures.

Engineers spent significant time manually searching documentation, often requiring 10–15 minutes to locate accurate information. Existing keyword search systems failed to capture semantic meaning, resulting in duplicated effort and inconsistent responses.

The objective was to build an enterprise-grade Retrieval-Augmented Generation (RAG) platform capable of delivering accurate, citation-grounded answers within seconds while supporting production-scale workloads.

---

## System Architecture

### Architecture Flow

1. Documents ingested from enterprise repositories
2. Parsing, cleaning, metadata extraction, and chunk generation
3. Embeddings generated using OpenAI embedding models
4. Chunks indexed into ChromaDB and Pinecone
5. User query embedded
6. Hybrid retrieval using semantic search and metadata filtering
7. Cross-encoder reranking
8. Context optimization
9. LLM response generation using OpenAI, Claude, or Gemini
10. Citation generation and confidence scoring

---

## Core Components

### Document Ingestion

- PDF parsing
- Office document extraction
- Metadata enrichment
- Adaptive chunking

### Retrieval Layer

- Vector search
- Hybrid retrieval
- Metadata filtering
- Cross-encoder reranking

### LLM Layer

- OpenAI
- Claude
- Gemini
- Dynamic model routing

### API Layer

- FastAPI
- REST APIs
- Authentication
- Rate limiting

### Infrastructure

- Docker
- Kubernetes
- CI/CD
- AWS
- GCP

---

## Design Decisions

### Hybrid Retrieval

Rather than relying solely on embeddings, hybrid retrieval combined semantic similarity with metadata filters and reranking to improve retrieval precision.

### Dynamic Context Selection

Relevant chunks were selected using adaptive context windows, reducing token usage while increasing answer quality.

### Multi-Model Architecture

Model routing selected the most appropriate LLM based on request complexity and cost.

---

## Tech Stack

### Languages

- Python

### LLM Frameworks

- OpenAI
- Claude
- Gemini

### Retrieval

- Pinecone
- ChromaDB
- Embeddings
- Hybrid Search

### APIs

- FastAPI

### Cloud

- AWS
- GCP

### Infrastructure

- Docker
- Kubernetes

---

## Evaluation & Safety

### Retrieval Evaluation

- Recall
- Precision
- MRR

### LLM Evaluation

- Faithfulness
- Groundedness
- Relevance

### Hallucination Prevention

- Citation Grounding
- Confidence Scoring
- Source Attribution

---

## Impact

### Business Outcomes

- Indexed 4,500+ engineering documents
- Indexed over 250K document chunks
- Reduced search time from 15 minutes to under 20 seconds
- Improved retrieval precision by 31%

### Operational Impact

- Reduced hallucinations by 45%
- Reduced inference costs by 38%
- Maintained sub-2-second latency

### Engineering Impact

- Built reusable enterprise RAG architecture
- Achieved 99.9% platform availability
