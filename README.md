# 🤖 AI Document Assistant

An advanced Document Q&A application built with three versions of Retrieval Augmented Generation (RAG) — from Basic RAG to Hybrid Search to GraphRAG.

## 🚀 Live Demo
**👉 [Try the app here](https://gen-ai-fundamentals-idimrtrqf7w7inmpbufydx.streamlit.app/)**

## What It Does
Upload any PDF and ask questions in plain English. The app finds relevant information from your document and generates accurate answers using AI. Three RAG versions are available — switch between them to see how retrieval quality improves.

## Three RAG Versions

### v1 — Basic RAG
- ChromaDB vector database for semantic similarity search
- Converts question and chunks into vectors, finds closest matches
- Simple and effective for straightforward questions

### v2 — Hybrid Search
- ChromaDB semantic search + keyword matching combined
- Semantic search finds meaning-similar chunks
- Keyword search finds exact word matches
- Combined results give better coverage than either alone

### v3 — GraphRAG
- Extracts entities and relationships from the document
- Builds a knowledge graph connecting concepts across chunks
- Retrieves connected information that semantic search would miss
- Best for large complex documents with interconnected concepts

## Tech Stack
- **LLM:** LLaMA 3.3-70b (Groq)
- **Framework:** Langchain
- **Vector Database:** ChromaDB
- **Embeddings:** HuggingFace all-MiniLM-L6-v2
- **Knowledge Graph:** NetworkX
- **Frontend:** Streamlit

## Key Findings
Tested all 3 versions on the same documents:
- Hybrid Search outperforms Basic RAG on keyword-specific queries
- GraphRAG excels on large complex documents with many interconnected concepts
- For short structured documents, Hybrid Search gives the best results

## Learning Notebooks
- `01_llms_embeddings_vectordb.ipynb` — LLMs, Embeddings, Vector Databases
- `02_rag.ipynb` — Retrieval Augmented Generation
- `03_langchain.ipynb` — Langchain Framework
