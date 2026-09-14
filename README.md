# RAG-Based Question Answering with LlamaIndex, Qdrant & Reranking

## Project Overview

This project demonstrates an end-to-end Retrieval-Augmented Generation (RAG) pipeline for question answering over a knowledge base.

The system combines semantic vector retrieval, cross-encoder reranking, and a local Hugging Face language model to generate answers grounded in retrieved document content.

## Problem Statement

Traditional keyword-based search may retrieve documents that contain related words but are not necessarily the most relevant to a user's question.

This project addresses the problem by using semantic embeddings to retrieve relevant content, followed by cross-encoder reranking to improve the relevance of retrieved sections before generating the final answer.

## Objectives

- Build an end-to-end RAG pipeline
- Load and process knowledge-base documents
- Generate semantic vector embeddings
- Store embeddings in Qdrant
- Retrieve relevant document sections using semantic similarity
- Apply cross-encoder reranking
- Generate context-grounded answers using a local LLM
- Evaluate retrieval performance on test queries

## RAG Workflow

```text
Documents
    ↓
Document Loading
    ↓
Chunking / Section Preparation
    ↓
Sentence Embeddings
    ↓
Qdrant Vector Store
    ↓
Semantic Retrieval
    ↓
Cross-Encoder Reranking
    ↓
Relevant Context
    ↓
TinyLlama LLM
    ↓
Final Answer