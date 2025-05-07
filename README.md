# YT-RAG

**YT-RAG** is a compact, efficient pipeline that transforms YouTube video transcripts into an interactive Q&A experience using Retrieval-Augmented Generation (RAG). It leverages FAISS for vector-based semantic search and Llama language model for generating context-aware answers.

---

## 🔍 What It Does

- 🎥 Accepts a YouTube **Video ID** as input
- 📝 Extracts the **transcript**
- ✂️ **Chunks** and embeds transcript text using Embedding model
- 📡 Stores embeddings in a **FAISS** vector index
- ❓ Enables semantic **question answering** with RAG using the Llama 3.2 Model

---

## 🧠 RAG Pipeline Overview

The system implements a **retrieval-augmented generation (RAG)** approach:

1. **Retrieval**  
   - The transcript is split into overlapping text chunks.
   - Each chunk is converted to a vector using embedding model.
   - These vectors are stored in a **FAISS index** for fast approximate nearest-neighbor search.

2. **Augmentation**  
   - When a question is asked, relevant chunks are **retrieved** from the FAISS index based on semantic similarity.

3. **Generation**  
   - The retrieved content is passed to the **Llama 3.2 LLM**  as context to generate a final answer.

---
