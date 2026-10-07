# RAG Implementation Using LangChain

## Overview

Retrieval-Augmented Generation (RAG) is a technique that combines information retrieval with Large Language Models (LLMs) to generate accurate and context-aware responses.

This project implements a basic RAG system using **Python, LangChain, Google Gemini, Gemini Embeddings, and ChromaDB**. The system loads information from a PDF document, splits the content into smaller chunks, converts the chunks into embeddings, stores them in a vector database, retrieves relevant information, and generates answers based on the retrieved context.

---

## Problem Statement

Large Language Models may not always have access to specific or domain-related information contained in external documents.

The objective of this project is to build a Retrieval-Augmented Generation system that can retrieve relevant information from a PDF document and use that information to generate context-based answers.

---

## Project Objectives

- Understand the concept of Retrieval-Augmented Generation (RAG).
- Load and process PDF documents.
- Split documents into smaller text chunks.
- Generate embeddings for documents and queries.
- Store document embeddings in a vector database.
- Retrieve relevant information using semantic search.
- Generate context-aware answers using Google Gemini.
- Understand the complete RAG pipeline using LangChain.

---

## Tools and Technologies

- Python
- LangChain
- Google Gemini
- Gemini Embedding Model
- ChromaDB
- NumPy
- tiktoken
- PyPDF
- Jupyter Notebook

---

## Data Processing

The following document processing steps were performed:

- Loaded the PDF document.
- Extracted text from the document.
- Checked document metadata.
- Split the document into smaller chunks.
- Used a chunk size of 500 characters.
- Used a chunk overlap of 50 characters.
- Prepared the chunks for embedding generation.

---

## Text Embedding

**Gemini Embedding 001** is used to convert text into numerical vector representations.

Embeddings were generated for:

- User questions
- Document content
- Document chunks

Cosine similarity was also calculated to measure the semantic similarity between a question and a document.

---

## Vector Database

**ChromaDB** is used as the vector store.

The document chunks and their embeddings are stored in ChromaDB, allowing the system to efficiently search for relevant information.

---

## Retrieval

The RAG system uses a retriever to identify the most relevant document chunks for a given question.

For example:

Question:When was tax first introduced in India?

        ↓

Retriever

        ↓

Relevant document chunk

        ↓

Retrieved context

## Generation

The retrieved information is passed to the **Google Gemini Large Language Model (LLM)** to generate the final response.

A prompt template is used to ensure that the model generates an answer based only on the relevant context retrieved from the document.

The generation process includes retrieving relevant information, combining it with the user's question, and passing it to the Gemini model to generate a context-aware response.

---

## RAG Workflow

The complete RAG workflow consists of the following steps:

- The **PDF document** is loaded using `PyPDFLoader`.
- The extracted content is divided into smaller chunks using `RecursiveCharacterTextSplitter`.
- **Gemini Embeddings** are generated for the document chunks.
- The embeddings are stored in **ChromaDB**.
- A retriever searches the vector database for relevant information.
- The retrieved information is provided as context to the **Google Gemini LLM**.
- Gemini generates the final answer based on the retrieved context.

The complete workflow is:

PDF Document
      ↓
Document Loading
      ↓
Text Splitting
      ↓
Text Chunks
      ↓
Gemini Embeddings
      ↓
ChromaDB
      ↓
Retriever
      ↓
Relevant Context
      ↓
Prompt Template
      ↓
Google Gemini
      ↓
Final Answer
## Key Concepts Demonstrated

- **Retrieval-Augmented Generation (RAG)**
- **Large Language Models (LLMs)**
- **Google Gemini**
- **Gemini Embeddings**
- **Text Embeddings**
- **Semantic Search**
- **Cosine Similarity**
- **PDF Document Processing**
- **Document Loading**
- **Text Splitting**
- **Vector Databases**
- **ChromaDB**
- **Prompt Templates**
- **LangChain**
- **Context-Based Generation**

---

## Conclusion

- It successfully demonstrates the implementation of a basic **Retrieval-Augmented Generation (RAG) system** using **Python, LangChain, Google Gemini, Gemini Embeddings, and ChromaDB**.

- The system processes an **Income Tax PDF document**, extracts the content, divides it into smaller chunks, generates embeddings, and stores the embeddings in a vector database.

- When a user asks a question, the system retrieves the most relevant information from the document and provides it as context to the **Google Gemini LLM**. Gemini then generates a context-aware response based on the retrieved information.

- This project provides practical understanding of how **document processing, embeddings, semantic search, vector databases, retrieval, and Large Language Models** work together to build a RAG application.

---

## Future Enhancements

- Support for **multiple PDF documents**.
- Development of a **conversational RAG chatbot**.
- Addition of **source citations** to generated answers.
- Implementation of **advanced retrieval techniques**.
- Addition of **document re-ranking**.
- Development of a **Streamlit-based user interface**.
- Integration of **FastAPI** for API deployment.
- Addition of **RAG evaluation metrics**.
- Implementation of **conversation history**.
- Deployment of the RAG application as a **web application**.


## Author

**Sarshini E**

Aspiring Data Analyst | Python | SQL | Data Visualization | Machine Learning





