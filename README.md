# Retrieval-Augmented Generation (RAG) Chatbot for PDFs

This project implements a **PDF-based Question Answering chatbot** using LangChain, Hugging Face Transformers, and FAISS. The chatbot processes PDF documents into embeddings, stores them in a vector database, and enables interactive querying with retrieval-augmented responses.

---

## Features
- Upload and process PDF files in Google Colab.
- Split text into overlapping chunks for improved retrieval.
- Generate embeddings using Hugging Face `all-MiniLM-L6-v2`.
- Store embeddings in a FAISS vector database for similarity search.
- Query the PDF using a lightweight Hugging Face language model (`google/flan-t5-base`).
- Conversational Retrieval-Augmented Generation (RAG) with chat history and source document references.

---

## Requirements
Install all dependencies in Google Colab or a local environment:

```bash
pip install -q langchain langchain-community faiss-cpu sentence-transformers transformers torch pypdf accelerate bitsandbytes huggingface_hub

**Project Structure
Module 1: Data Preprocessing & Embeddings**

Upload PDF file into Colab.

Load and split the document into manageable chunks.

Generate sentence embeddings using Hugging Face.

Store embeddings in FAISS vector database.

**Module 2: LLM & Chatbot Setup**

Load the google/flan-t5-base model for text-to-text generation.

Wrap model with Hugging Face pipeline.

Integrate with LangChain ConversationalRetrievalChain.

Build a chatbot capable of answering queries using retrieved chunks.


**Module 3: Main Runner**


Orchestrates PDF processing, model setup, and chatbot creation.

Launches an interactive chat loop with context-aware responses.

Maintains chat history.

Displays retrieved source passages alongside answers.
