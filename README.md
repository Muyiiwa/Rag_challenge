# Rag_challenge
# RAG FastAPI Project

## Overview
This project demonstrates a **Retrieval-Augmented Generation (RAG)** pipeline using:

- **Sentence Transformers** (`all-MiniLM-L6-v2`) for embedding document chunks.
- **FAISS** for efficient vector search and retrieval.
- **Flan-T5 (small)** for generating answers based on retrieved context.
- **FastAPI** for serving the model via a REST API.
- **S3** for storing document chunks and precomputed FAISS index.

The system allows you to query documents and get factually-grounded answers.

---

## Features
1. **Data Preparation**:  
   - Clean and chunk documents (PDF/DOCX).  
   - Normalize text for consistent embeddings.

2. **Retrieval Component**:  
   - FAISS vector search retrieves top-k most relevant chunks.  

3. **Generation Component**:  
   - Flan-T5 generates an answer using the retrieved context.  

4. **Evaluation**:  
   - Retrieval hit-rate and faithfulness score metrics can be computed locally.  

---

## Setup & Deployment

### 1. Environment Variables
Set S3 bucket and prefix:

```bash
export BUCKET="your-s3-bucket-name"
export S3_PREFIX="your/s3/prefix"
