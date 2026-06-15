# 📄 Financial Document RAG Agent

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-000000?style=flat-square)
![FAISS](https://img.shields.io/badge/FAISS-009688?style=flat-square)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**AI-powered Q&A over financial documents** — semantic retrieval across 10-Ks, earnings reports, and analyst PDFs using LangChain, FAISS vector search, and Groq inference.

</div>

---

## What It Does

A Retrieval-Augmented Generation (RAG) system purpose-built for financial documents. Upload a 10-K, earnings transcript, or analyst report and ask natural language questions — the system retrieves the exact relevant passages and synthesizes precise answers with source citations.

**No hallucinations on document content** — every answer is grounded in retrieved chunks from the actual document.

---

## Key Results

- Sub-second retrieval across 100+ page financial documents
- Accurate extraction of numerical data (revenue figures, margins, YoY comparisons)
- Source-cited answers — every response shows which page/section it came from
- Gradio UI — usable without any coding

---

## RAG Pipeline Architecture

```
PDF / Financial Document
        │
        ▼
   Docling Parser
  (structured text extraction)
        │
        ▼
  Text Chunking (LangChain)
  (chunk size: 512 tokens, 50 overlap)
        │
        ▼
  HuggingFace Embeddings
  (sentence-transformers/all-MiniLM-L6-v2)
        │
        ▼
  FAISS Vector Index (local, persistent)
        │
   ┌────┴────┐
   │  Query  │ ← User Question
   └────┬────┘
        ▼
  Similarity Search (top-k=5)
        │
        ▼
  Groq LLM (Llama 3) + Retrieved Context
        │
        ▼
  Answer + Source Citations (Gradio UI)
```

---

## Tech Stack

| Component | Tool |
|---|---|
| Document Parsing | Docling |
| Chunking & Retrieval Chain | LangChain |
| Embeddings | HuggingFace Transformers (`all-MiniLM-L6-v2`) |
| Vector Store | FAISS |
| LLM | Groq (Llama 3 70B) |
| UI | Gradio |
| Language | Python 3.10+ |

---

## Setup & Run

```bash
# 1. Clone the repo
git clone https://github.com/Tarun110/Financial-Document-RAG-Agent.git
cd Financial-Document-RAG-Agent

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set your API key
export GROQ_API_KEY=your_key_here

# 4. Launch the app
python app.py
# Opens Gradio UI at http://localhost:7860
```

---

## Usage

1. Upload a financial PDF (10-K, earnings report, etc.)
2. Wait ~10 seconds for indexing
3. Ask questions in natural language:
   - *"What was the revenue growth YoY?"*
   - *"What are the main risk factors mentioned?"*
   - *"Summarize the outlook for next quarter."*

---

## Project Structure

```
Financial-Document-RAG-Agent/
├── rag_pipeline.py        # Core RAG logic
├── embeddings.py          # HuggingFace embedding setup
├── vector_store.py        # FAISS index management
├── app.py                 # Gradio UI
├── requirements.txt
└── sample_docs/           # Example financial PDFs
```

---

## Author

**Tarun Sai Reddy Kummetha** — [LinkedIn](https://www.linkedin.com/in/tarun-sai-reddy-k-3182b2237) · [Portfolio](https://tarun110.github.io/tarunreddy.github.io/)
