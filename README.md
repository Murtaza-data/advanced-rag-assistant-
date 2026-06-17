# 🤖 AI Document Assistant

An advanced Document Q&A app built with three versions of Retrieval Augmented Generation (RAG) — Basic RAG, Hybrid Search, and GraphRAG — plus Corrective RAG with web fallback.

## 🚀 Live Demo
**👉 [Try the app here](https://gen-ai-fundamentals-murtaza-document-assistant.streamlit.app/)**

## What It Does
Upload one or more PDFs and ask questions in plain English. The app retrieves the relevant content from your documents and generates accurate, cited answers. If the answer isn't in your documents, it falls back to a web search.

## Three RAG Versions
- **v1 — Basic RAG:** semantic similarity search (ChromaDB)
- **v2 — Hybrid Search:** semantic search + BM25 keyword search, combined
- **v3 — GraphRAG:** builds a knowledge graph (NetworkX) of entities and retrieves connected information across chunks

## Key Features
- **Corrective RAG** — grades whether retrieved chunks are relevant; if weak, rewrites the query and retries; if still weak, falls back to a web search
- **Multi-document upload** — search across several PDFs in one knowledge base
- **Metadata filtering** — restrict search to a specific document
- **Self-query routing** — in Auto mode, the LLM picks which document to search
- **Query rewriting** — vague questions are rewritten for better retrieval
- **Source citations** — every answer shows the document and page it came from
- **Hallucination prevention** — answers only from the documents; says so when the info isn't there
- **Cached knowledge base** — documents embedded once per upload (`st.cache_resource`)
- **Scanned PDF detection** — reports image-only PDFs instead of failing silently

## Tech Stack
- **LLM:** LLaMA 3.3-70b (Groq)
- **Framework:** LangChain
- **Vector DB:** ChromaDB
- **Keyword Search:** BM25
- **Knowledge Graph:** NetworkX
- **Web Search:** Tavily
- **Embeddings:** HuggingFace all-MiniLM-L6-v2
- **Frontend:** Streamlit

## Learning Notebooks
- `01_llms_embeddings_vectordb.ipynb` — LLMs, Embeddings, Vector Databases
- `02_rag.ipynb` — Retrieval Augmented Generation
- `03_langchain.ipynb` — LangChain Framework
