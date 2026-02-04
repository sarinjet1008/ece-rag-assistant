ECE Graduate Handbook RAG Assistant

A Retrieval-Augmented Generation (RAG) system that enables intelligent question answering over the Rutgers University Electrical & Computer Engineering (ECE) Graduate Handbook using semantic search (ChromaDB) and OpenAI language models.

Overview

This project implements a domain-specific RAG pipeline in Python that allows users to query a graduate handbook PDF and receive conversational, context-aware responses.

Instead of relying purely on an LLM’s internal knowledge, the system:

Converts handbook text into embeddings

Stores document chunks in ChromaDB

Retrieves the most relevant sections via similarity search

Sends retrieved context to OpenAI for grounded response generation

This architecture significantly reduces hallucination and improves factual accuracy.

System Architecture
Graduate Handbook PDF
        ↓
Text Extraction (LangChain PDF Loader)
        ↓
Document Chunking
        ↓
Embedding Generation (OpenAI)
        ↓
Vector Storage (ChromaDB)
        ↓
User Query
        ↓
Query Embedding
        ↓
Similarity Search (Top-K Chunks)
        ↓
Context + Query → OpenAI LLM
        ↓
Grounded Response

 Tech Stack

Python

ChromaDB (Vector Database)

LangChain (PDF loading & text splitting)

OpenAI API (Embeddings + LLM responses)

dotenv (Secure API key storage)
