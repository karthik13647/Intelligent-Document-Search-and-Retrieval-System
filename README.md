# 🧠 Intelligent Document Search and Retrieval System

**Tech Stack:** Python · SQL · FastAPI · Hugging Face · REST API

***

## 📘 Project Overview

The Intelligent Document Search and Retrieval System is an AI-powered application that enables users to search and retrieve relevant information from diverse file types — including DOCX, PDF, and code files — in real time.
This system integrates semantic search using Hugging Face embeddings with traditional SQL keyword queries, providing faster, context-aware document retrieval.

***

## 🚀 Key Features

| Feature | Description |
| :-- | :-- |
| Multi-format Support | Extracts and processes DOCX, PDF, and code files |
| Hybrid Search System | Combines SQL keyword queries with semantic search embeddings |
| Semantic Understanding | Uses Hugging Face transformer models for context-aware retrieval |
| Structured SQL Storage | Stores parsed text and metadata in indexed relational tables |
| RESTful API Access | Exposes endpoints via FastAPI for easy integration |
| High Performance | Reduces document search time from minutes to seconds |


***

## 🧩 System Architecture

```
+-------------------+
|   File Upload     |
| (PDF, DOCX, Code) |
+--------+----------+
         |
         v
+-------------------+
| Data Extraction   |
| (Text Parsing)    |
+--------+----------+
         |
         v
+-------------------+
| SQL Database      |
| (Indexed Storage) |
+--------+----------+
         |
         v
+-------------------+
| Hybrid Search     |
| SQL + Embeddings  |
+--------+----------+
         |
         v
+-------------------+
| REST API (FastAPI)|
| JSON Responses    |
+-------------------+
```


***

## 🧠 Technical Implementation

### 1. Data Ingestion and Preprocessing

- Extract text \& metadata using Python libraries (PyPDF2, python-docx, os, re).
- Structure extracted data into SQL tables with indexes for efficient lookup.


### 2. Hybrid Search Mechanism

- **Keyword Search:** SQL LIKE and FULL-TEXT queries for direct matches.
- **Semantic Search:** Hugging Face SentenceTransformer embeddings for contextual queries.
- Both approaches are combined to rank and return most relevant results.


### 3. API Development and Deployment

- REST endpoints built with FastAPI for upload/search actions.
- Deployable locally or on Render for scalable access.

***

## 🧮 Example SQL Query

```sql
-- Keyword-based search for documents containing 'machine learning'
SELECT doc_name, content 
FROM documents 
WHERE content LIKE '%machine learning%'
ORDER BY LENGTH(content);
```


***

## 💻 Sample API Endpoints

| Method | Endpoint | Description |
| :-- | :-- | :-- |
| POST | /upload | Upload and process files (DOCX, PDF, Code) |
| GET | /search?query=keyword | Perform hybrid (SQL + semantic) search |
| GET | /documents | Retrieve all indexed documents |


***

## 📊 Results \& Impact

- Achieved 70% faster document retrieval compared to traditional keyword systems.
- Reduced average query response time from minutes to seconds.
- Enabled context-aware document matching, improving user accessibility.

***

## 🛠️ Technologies Used

- **Programming:** Python
- **Framework:** FastAPI
- **Database:** SQL (SQLite/MySQL)
- **AI Model:** Hugging Face Sentence Transformers
- **Libraries:** Pandas, PyPDF2, python-docx, SQLAlchemy
- **Deployment:** Render / Localhost

***

## 📄 Future Enhancements

- Add authentication and user roles for access control.
- Integrate vector databases (FAISS or Pinecone) for large-scale semantic retrieval.
- Build a frontend interface with React or Streamlit.
- Support multilingual document search.

***

## ⚡️ Code Setup

```bash
# Clone the repository
git clone https://github.com/karthik13647/intelligent-doc-search.git
cd intelligent-doc-search

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the FastAPI server
uvicorn main:app --reload
```


***

## 📬 Contact

- **Author:** Karthik Batta
- **Email:** [karthikbatta6503@gmail.com](mailto:karthikbatta6503@gmail.com)
- **LinkedIn:** [Karthik Batta](https://www.linkedin.com/in/karthik-b-475484259/)
- **GitHub:** [karthik13647](https://github.com/karthik13647)

***

This README.md is ready for use on GitHub, ATS systems, and portfolios.

