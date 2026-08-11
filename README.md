# DocuRAG

A document-based RAG application for uploading PDFs, searching their content, and asking questions using Azure OpenAI and a local FAISS vector store.

## About

DocuRAG is a small document question-answering project built around the Retrieval-Augmented Generation (RAG) approach.

PDF files are processed, split into smaller chunks, converted into embeddings, and stored in a local FAISS index. When a question is asked, the application retrieves the most relevant chunks and uses them as context for the Azure OpenAI model.

The project also includes a simple interface for inspecting the stored chunks and vector information.

## Features

- Upload and process PDF documents
- Extract text using PyMuPDF
- Split documents into overlapping text chunks
- Generate embeddings using Azure OpenAI
- Store embeddings locally using FAISS
- Search documents using similarity search
- Filter retrieved content by document source
- Ask questions about uploaded documents
- Inspect stored chunks and embedding information
- View basic FAISS index details

## Tech Stack

- Python
- Streamlit
- LangChain
- Azure OpenAI
- FAISS
- PyMuPDF
- NumPy
- python-dotenv

## How It Works

```text
PDF
 |
 v
PyMuPDF
 |
 v
Text Extraction
 |
 v
Text Chunking
 |
 v
Azure OpenAI Embeddings
 |
 v
FAISS Vector Store
 |
 v
Similarity Search
 |
 v
Relevant Document Chunks
 |
 v
Azure OpenAI
 |
 v
Answer
