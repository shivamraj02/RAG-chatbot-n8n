# RAG-chatbot-n8n
A Retrieval-Augmented Generation (RAG) chatbot built with n8n that answers user queries strictly from provided documents using vector embeddings and similarity search, ensuring accurate and hallucination-free responses.
# 🤖 RAG-Based AI Chatbot (n8n + LLM)

## 📌 Overview
This project is a **Retrieval-Augmented Generation (RAG) chatbot** that answers user questions **strictly from provided documents**.  
It uses vector embeddings and similarity search to avoid hallucinations and deliver accurate, document-grounded responses.

---

## 🧠 What is RAG?
RAG (Retrieval-Augmented Generation) combines:
- **Information Retrieval** (vector similarity search)
- **Text Generation** (LLM-based answers)

This ensures responses are based only on trusted documents.

---

## 🏗️ Architecture
Documents (PDF)
↓
Text Extraction & Chunking
↓
Embeddings
↓
Vector Database
↓
User Question
↓
Similarity Search

---

## ⚙️ Tech Stack
- n8n (Workflow Automation)
- OpenAI (Embeddings + Chat Model)
- Vector Database (Supabase / Pinecone / Chroma)
- PDF Parser
- Webhook API

---

## 🔁 Workflows

### 1️⃣ Document Ingestion Workflow
- Upload PDF documents
- Extract text
- Split text into chunks
- Generate embeddings
- Store vectors in database

**File:** `workflows/ingestion-workflow.json`

---

### 2️⃣ Chat / Query Workflow
- Accept user question via webhook
- Convert question to embedding
- Retrieve relevant document chunks
- Generate grounded AI response

**File:** `workflows/chat-workflow.json`

---

## 🛡️ Anti-Hallucination Prompt
You are an AI assistant.
Answer ONLY using the provided context.
If the answer is not found in the context, say:
"I don’t have that information in the documents."
Do not guess or fabricate answers.

---

## ✨ Features
- Document-based question answering
- Vector similarity search
- No hallucinations
- Scalable RAG architecture
- Resume & production ready

---

## ▶️ How to Run
1. Import workflows into n8n
2. Configure OpenAI API key
3. Set up vector database credentials
4. Run ingestion workflow once
5. Start chat workflow and query via webhook

---

## 📸 Screenshots
See `/screenshots` folder for workflow and demo images.

---

## 🚀 Future Improvements
- Source citations in answers
- Multi-document support
- WhatsApp + RAG integration
- Authentication layer

---

## 💼 Resume Statement
> Built a Retrieval-Augmented Generation (RAG) chatbot using n8n, vector embeddings, and LLMs to deliver accurate, document-grounded AI responses.

↓
LLM Answer (Grounded)
