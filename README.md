# RAG Learning Pipeline

A comprehensive implementation of a Retrieval-Augmented Generation (RAG) pipeline for processing, embedding, and querying documents.

## 📋 Project Overview

This project implements a complete RAG pipeline that processes various document formats, chunks them into manageable pieces, converts them into vector embeddings, and stores them in a vector database for efficient similarity search.

## 🔄 Pipeline Architecture

```
Data Ingestion → Data Parsing → Chunking → Embedding → Vector DB → Similarity Search
```

### Pipeline Stages

#### 1. **Data Ingestion**
Accepts multiple document formats:
- 📄 **PDF** - Portable Document Format files
- 🌐 **HTML** - Web pages and HTML documents
- 📊 **Excel** - Spreadsheets and tabular data
- 🗄️ **Database** - Direct database connections

Extracts key components:
- **Metadata** - Document properties, author, creation date
- **Content** - Main text content
- **Structure** - Document hierarchy and organization

#### 2. **Data Parsing**
Processes raw documents into structured format:
- Cleans and normalizes text
- Extracts relevant information
- Preserves document structure
- Prepares data for chunking

#### 3. **Chunking**
Splits documents into smaller, manageable pieces:
- Creates multiple chunks (Chunk 1, Chunk 2, Chunk 3, Chunk 4, ...)
- Considers context size for optimal embedding
- Maintains semantic coherence within chunks
- Preserves important context boundaries

**Key Consideration:** `hLu4s = context size` - Chunk size must fit within the embedding model's context window

#### 4. **Embedding (Text → Vectors)**
Converts text chunks into numerical vector representations:
- Transforms text into high-dimensional vectors
- Captures semantic meaning
- Enables similarity comparison
- Optimizes for context size constraints

#### 5. **Vector Database**
Stores embeddings for efficient retrieval:
- Indexes vector embeddings
- Enables fast similarity search
- Supports scalable storage
- Facilitates quick retrieval of relevant chunks

#### 6. **Similarity Search**
Retrieves relevant documents based on queries:
- Compares query vectors with stored embeddings
- Returns most relevant chunks
- Ranks results by similarity score
- Provides context for LLM generation

