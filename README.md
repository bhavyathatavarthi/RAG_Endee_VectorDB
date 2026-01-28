# 📘 PDF RAG System using ENDEE Vector DataBase
This project implements a Retrieval-Augmented Generation (RAG) system that enables users to ask natural language questions over PDF documents. The system converts document content into vector embeddings and stores them in the Endee vector database for efficient semantic search. When a user submits a query, the most relevant document chunks are retrieved using vector similarity and passed to a local Large Language Model (LLM) via Ollama to generate accurate, context-grounded answers. The entire pipeline runs locally without any cloud dependency, demonstrating a practical and production-oriented AI retrieval system.

## Problem Statement
Large documents such as PDFs contain valuable information, but extracting precise answers from them is time-consuming and inefficient using traditional keyword-based search. Standard search methods fail to capture semantic meaning, leading to irrelevant or incomplete results.This project addresses these challenges by using vector embeddings and semantic search with Endee, combined with a local LLM, to enable accurate, private, and efficient question answering directly from unstructured documents.

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

## Technical Approach
1. PDF documents are loaded and split into smaller overlapping text chunks for efficient retrieval.
2. Each chunk is converted into a semantic embedding using a Sentence Transformer model.
3. Embeddings are stored and indexed in the Endee vector database along with relevant metadata.
4. User queries are embedded using the same model and matched against stored vectors using similarity search.
5. The top relevant chunks are retrieved and passed as context to a local LLM via Ollama.
6. The LLM generates answers strictly based on the retrieved context, ensuring accurate and grounded responses.

## 📦 Tech Stack

- **Python**
- **LangChain**
- **Sentence-Transformers**
- **Ollama**
- **Vector Database** (Endee)

---


---

## ⚙️ Setup Instructions

### Clone the repository
```bash
git clone https://github.com/bhavyathatavarthi/RAG_Endee_VectorDB
cd RAG_Endee_VectorDB
```
### Create a Virtual environment
```bash
python -m venv venv
source venv/bin/activate
Windows : venv/Scripts/activate
```
### Install dependencies
```bash
pip install -r requirements.txt
```

### Start Ollama

```bash
ollama pull gemma3:4b
ollama serve
```

