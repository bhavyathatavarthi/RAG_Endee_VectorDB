# 📘 PDF RAG System using Ollama & Vector Search

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline that allows you to ask questions from a PDF document using **semantic search** and a **local LLM (Ollama)**.

The system retrieves the most relevant chunks from the PDF using vector similarity and generates answers strictly grounded in the document content.

---

## 🚀 Features

- 📄 Load and process PDF files
- ✂️ Chunk documents for better retrieval
- 🔢 Generate embeddings using Sentence Transformers
- 🧠 Semantic search using a vector index
- 🤖 Local LLM inference using **Ollama (Gemma / LLaMA)**
- ❌ No OpenAI / cloud dependency
- ✅ Answers grounded only in PDF context

---

## 🧠 Architecture
User Question
↓
Sentence Embeddings
↓
Vector Database (Semantic Search)
↓
Top-k Relevant PDF Chunks
↓
Ollama LLM
↓
Final Answer (from PDF only)


---

## 📦 Tech Stack

- **Python**
- **LangChain**
- **Sentence-Transformers**
- **Ollama**
- **Vector Database** (Endee / FAISS / similar)

---


---

## ⚙️ Setup Instructions

### Install dependencies

```bash
pip install -r requirements.txt
```

### Start Ollama

```bash
ollama pull gemma3:4b
ollama serve
```

