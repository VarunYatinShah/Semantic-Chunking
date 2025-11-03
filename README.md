# Semantic-Chunking
Overview

This repository explores semantic chunking, a context-aware approach to dividing large text documents into meaningful segments.
The project examines how semantic chunking compares with standard (fixed-size) chunking in terms of chunk properties and performance within a Retrieval-Augmented Generation (RAG) pipeline.

🎯 Objective

Traditional chunking splits text at arbitrary points — typically by character or token count — without considering the meaning or structure of the content.
While this is simple and efficient, it can disrupt context and coherence across chunk boundaries.

Semantic chunking, on the other hand, attempts to preserve semantic continuity by splitting text where topic or meaning naturally shifts.
This project aims to study:

How semantic chunking differs from normal chunking in chunk size and length distribution

How it impacts retrieval quality (i.e., how well chunks match user queries)

How it influences RAG answer quality, by maintaining more coherent context windows for large language models

⚙️ Implementation

The repository includes implementations of both chunking methods and tools for comparison.

1. Normal Chunking

Splits the text into equal-sized parts based on token or character count.
This approach ignores content meaning and is useful as a simple baseline.

2. Semantic Chunking

Uses sentence boundaries, embeddings, or similarity scores to find natural breakpoints.
Chunks are formed based on semantic shifts rather than fixed lengths, preserving context across sentences and paragraphs.

![download (23)](https://github.com/user-attachments/assets/71789f56-56f9-4960-b3d7-737bf78b04db)

3. Evaluation

After both chunking methods are applied:

Chunks are used in retrieval tasks to evaluate how well relevant information is retrieved.

The retrieved chunks are fed into a RAG system to analyze answer quality and contextual relevance.

🧠 What This Project Examines

The differences in chunk characteristics between semantic and normal chunking

The impact on retrieval relevance within a vector-based search system

The effect on RAG response quality, where maintaining coherent context improves answer precision

🧰 Technologies Used

Python 3.9+

Sentence Transformers / OpenAI embeddings for semantic analysis

NumPy, Pandas for data handling

Matplotlib for visualization

Any LLM API (e.g., groq) for RAG evaluation
