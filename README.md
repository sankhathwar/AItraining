# AI Training

This repository contains my daily AI assignments and projects.

## Repository Structure

```text
AI/
├── Day1/
│   └── mini-rag-chatbot/
│       ├── Mini_RAG_Chatbot.ipynb
│       ├── README.md
│       ├── requirements.txt
│       ├── sample_data/
│       │   └── sample.pdf
│       └── screenshots/
│           ├── snapshot1.png
│           └── snapshot2.png
│
├── Day2/
│   └── semantic-search-faiss/
│       ├── semantic_search.ipynb
│       ├── requirements.txt
│       ├── theory_answers.md
|
└── README.md
```

## Day 1

### Mini RAG Chatbot

A Retrieval-Augmented Generation (RAG) chatbot built using:

- Google Gemini API
- Gemini Embeddings (`gemini-embedding-001`)
- Gemini 3.6 Flash
- FAISS Vector Database
- PyPDF
- Python

### Features

- PDF text extraction
- Text chunking
- Embedding generation
- Vector database indexing
- Semantic search
- Context retrieval
- LLM-based question answering
- Conversational chatbot with chat history


## Day 2

### Semantic Search Engine with FAISS

A mini semantic search engine built using Sentence Transformers and FAISS, demonstrating how production Retrieval-Augmented Generation (RAG) systems perform efficient semantic retrieval.

### Technologies Used
- Python
- Sentence Transformers
- all-MiniLM-L6-v2
- FAISS (IndexFlatL2)
- NumPy

### Features
- Generate sentence embeddings using all-MiniLM-L6-v2
- Build a FAISS vector index
- Normalize embeddings for cosine similarity search
- Perform Top-3 semantic similarity search
- Interactive command-line search interface
- Theory notes explaining FAISS indexing and Approximate Nearest Neighbour (ANN) search
