# 💰 Financial Document RAG Agent using LangChain, FAISS & Groq

## 📌 Overview

Financial reports such as 10-K, 10-Q, and annual filings contain valuable business insights, but they are often lengthy, complex, and difficult to analyze manually.

This project leverages Retrieval-Augmented Generation to build an AI-powered financial document question-answering system. The application allows users to upload financial PDF reports and ask natural-language questions about revenue, net income, operating expenses, earnings per share, risk factors, business performance, and other key financial metrics.

The system converts financial PDFs into structured text, splits the content into meaningful chunks, stores embeddings in a FAISS vector database, retrieves the most relevant sections, and generates context-aware answers using a Groq-powered Llama model.

This project demonstrates an end-to-end Generative AI workflow, including document ingestion, PDF parsing, text chunking, vector embeddings, semantic search, retrieval-based question answering, and an interactive Gradio user interface.

## 🚀 Key Features

### 📄 Financial PDF Document Processing

Processes financial reports such as 10-Q, 10-K, and annual reports.

Converts complex PDF documents into structured Markdown text using Docling.

### 🧠 Retrieval-Augmented Generation

Uses RAG architecture to retrieve relevant financial context before generating answers.

Ensures responses are grounded in the uploaded document instead of relying only on the language model.

### 🔎 Semantic Search with FAISS

Creates vector embeddings using HuggingFace Sentence Transformers.

Stores and retrieves relevant document chunks using FAISS vector database.

### 🤖 LLM-Powered Question Answering

Uses Groq API with Llama model for fast and efficient response generation.

Answers financial questions in a clear and structured format.

### 🖥️ Interactive Gradio Interface

Provides a simple web-based interface for uploading financial documents.

Allows users to ask questions directly after document processing.

### 📊 Financial Analysis Use Cases

Supports questions related to:

Revenue performance
Net income
Earnings per share
Operating expenses
Product vs service sales
Year-over-year comparison
Risk factors
Business performance summary

## 🔧 Tech Stack

### Generative AI & RAG

LangChain
Groq API
Llama Model
Retrieval-Augmented Generation

### Vector Database & Embeddings

FAISS
HuggingFace Sentence Transformers
all-MiniLM-L6-v2

### Document Processing

Docling
PDF to Markdown Conversion

### User Interface

Gradio

### Programming

Python
Jupyter Notebook

## 📂 Project Workflow

### 1️⃣ Document Upload

The user uploads a financial PDF report through the Gradio interface.

### 2️⃣ PDF Conversion

The uploaded PDF is converted into Markdown text using Docling.

### 3️⃣ Text Chunking

The converted Markdown content is split into smaller sections using LangChain text splitters.

### 4️⃣ Embedding Generation

Each text chunk is converted into vector embeddings using HuggingFace Sentence Transformers.

### 5️⃣ Vector Storage

The generated embeddings are stored in a FAISS vector database for efficient similarity search.

### 6️⃣ Context Retrieval

When a user asks a question, the system retrieves the most relevant chunks from the financial document.

### 7️⃣ Answer Generation

The retrieved context is passed to the Groq Llama model to generate a document-grounded answer.

### 8️⃣ User Interaction

The final answer is displayed through the Gradio interface.

## 🧪 Example Questions

What was the company’s total revenue?

How does the current quarter revenue compare with the previous year?

What was the net income for the reporting period?

What were the earnings per share?

How much revenue came from product sales versus service sales?

What were the main operating expense categories?

What are the key risk factors mentioned in the report?

Summarize the company’s financial performance.

## 📈 Key Insights

### 📌 Faster Financial Report Analysis

The system reduces the time required to manually search through lengthy financial filings.

### 🎯 Context-Aware Answers

The RAG pipeline ensures that answers are generated based on the uploaded financial document.

### ⚡ Efficient Retrieval

FAISS enables fast semantic search across large financial reports.

### 💼 Business Relevance

This solution can support financial analysts, investors, business teams, and researchers in quickly extracting insights from financial documents.

## 🏆 Skills Demonstrated

Generative AI
Retrieval-Augmented Generation
LangChain
Vector Databases
FAISS
HuggingFace Embeddings
Groq API
LLM Application Development
Financial Document Analysis
PDF Processing
Semantic Search
Gradio App Development
Python
Prompt Engineering

## 🎯 Business Value

Financial reports are information-rich but time-consuming to analyze. This application helps users quickly extract meaningful insights from financial documents using natural-language questions.

By combining semantic search with LLM-powered answer generation, the solution improves accessibility, speeds up financial analysis, and supports better decision-making for business and investment research.

## ⚠️ Disclaimer

This project is built for educational and portfolio purposes only. It does not provide financial advice, investment recommendations, or professional financial analysis.

