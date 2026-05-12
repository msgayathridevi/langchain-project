# LangChain Fundamentals

A hands-on, notebook-driven repository for learning **LangChain** from the ground up, covering foundational concepts required to build modern **LLM-powered applications** such as chatbots, Retrieval-Augmented Generation (RAG) systems, semantic search engines, and intelligent document assistants.

This repository provides practical examples using **LangChain**, **OpenAI-compatible APIs**, **Google Gemini embeddings**, **Ollama local models**, **ChromaDB**, and **FAISS**.

**Author:** Gayathri Devi MS

---

## Overview

This project is designed as a step-by-step learning path through the LangChain ecosystem. Each Jupyter notebook focuses on one core concept and builds toward a complete understanding of how to:

* Connect and interact with Large Language Models (LLMs)
* Build reusable prompt templates
* Generate structured outputs
* Parse and transform model responses
* Chain multiple LangChain components together
* Load and process different document formats
* Split large documents into manageable chunks
* Generate embeddings for semantic understanding
* Store and retrieve vectors using FAISS and ChromaDB
* Implement advanced retrieval strategies for RAG systems

The repository is ideal for:

* Beginners learning LangChain fundamentals
* Developers building AI-powered applications
* Students exploring LLM orchestration frameworks
* Engineers prototyping local or cloud-based RAG systems

---

## Repository Structure

```text
langchain-project/
│
├── 01_llm.ipynb                  # Working with LLM providers and model invocation
├── 02_prompt_template.ipynb      # Prompt templates and prompt engineering
├── 03_structured_output.ipynb    # Typed and structured LLM responses
├── 04_output_parser.ipynb        # Parsing and formatting model outputs
├── 05_chain.ipynb                # Building LangChain pipelines/chains
├── 06_document_loader.ipynb      # Loading PDFs, CSV, JSON, Markdown, and text files
├── 07_text_splitters.ipynb       # Chunking documents for downstream processing
├── 08_embeddings.ipynb           # Generating and understanding embeddings
├── 09_vector_stores.ipynb        # Vector databases with ChromaDB and FAISS
├── 10_retrievers.ipynb           # Retrieval strategies and document search
│
├── Documents/
│   ├── Machine Learning.pdf
│   ├── Machine Learning copy.pdf
│   ├── e-commerce.csv
│   ├── sample-json-file.json
│   └── sample-markdown.md
│
├── Chroma_db/                    # Persistent Chroma vector database files
├── faiss_db/                     # FAISS index files
├── Air pollution.pdf             # Sample PDF used for experimentation
├── requirements.txt              # Python dependencies
├── .env                          # Environment variables (local only, do not commit secrets)
├── .gitignore
├── LICENSE
└── README.md
```

---

## Learning Modules

### 1. LLM Integration (`01_llm.ipynb`)

Learn how to connect LangChain with LLM providers and invoke chat models.

**Topics covered:**

* Loading API keys with `python-dotenv`
* OpenAI-compatible client configuration
* Calling hosted inference endpoints
* Prompting chat models
* Reading model responses

**Concepts:**

* Chat models
* Temperature and generation settings
* API authentication

---

### 2. Prompt Templates (`02_prompt_template.ipynb`)

Create dynamic and reusable prompts using LangChain prompt templates.

**Topics covered:**

* String prompt templates
* Variable injection
* Prompt reusability
* Parameterized prompting

**Why it matters:**
Prompt templates improve consistency and make prompt engineering scalable.

---

### 3. Structured Output (`03_structured_output.ipynb`)

Guide models to return predictable, schema-based responses.

**Topics covered:**

* `TypedDict` schemas
* Structured data generation
* Validation-friendly outputs
* JSON-like responses

**Use cases:**

* Information extraction
* Classification pipelines
* Data transformation

---

### 4. Output Parsers (`04_output_parser.ipynb`)

Transform raw model responses into clean, usable formats.

**Topics covered:**

* String output parsers
* Response normalization
* Post-processing LLM outputs

**Benefits:**
Essential for integrating LLMs into production applications.

---

### 5. Chains (`05_chain.ipynb`)

Combine prompts, models, and parsers into reusable LangChain workflows.

**Topics covered:**

* Simple chains
* Runnable pipelines
* Component composition
* Input/output flow management

**Example pipeline:**

```text
Input → Prompt Template → LLM → Output Parser → Final Response
```

---

### 6. Document Loaders (`06_document_loader.ipynb`)

Load and process documents from multiple formats.

**Supported formats:**

* PDF (`pypdf`)
* CSV
* JSON
* Markdown
* Plain text
* Unstructured documents

**Applications:**

* Knowledge base creation
* Enterprise document search
* RAG ingestion pipelines

---

### 7. Text Splitters (`07_text_splitters.ipynb`)

Split large documents into smaller chunks for embedding and retrieval.

**Topics covered:**

* Character text splitting
* Chunk size tuning
* Chunk overlap strategies

**Why chunking matters:**
Improves retrieval precision and reduces context loss.

---

### 8. Embeddings (`08_embeddings.ipynb`)

Convert text into dense vector representations.

**Topics covered:**

* Embedding fundamentals
* High-dimensional vector spaces
* Semantic similarity
* Google Gemini embeddings

**Highlights:**

* Understanding embedding dimensions
* Comparing vector quality
* Preparing data for vector databases

---

### 9. Vector Stores (`09_vector_stores.ipynb`)

Store and search embeddings efficiently.

**Technologies used:**

* **ChromaDB** for persistent local vector storage
* **FAISS** for fast similarity search

**Topics covered:**

* Creating vector indexes
* Saving/loading databases
* Similarity search
* Metadata filtering

---

### 10. Retrievers (`10_retrievers.ipynb`)

Explore retrieval strategies beyond basic similarity search.

**Topics covered:**

* Semantic retrieval
* Maximum Marginal Relevance (MMR)
* Score-based ranking
* BM25 keyword retrieval
* Hybrid retrieval concepts

**Why retrievers matter:**
They significantly improve the quality of RAG systems by selecting better context.

---

## Technologies Used

### Core Frameworks

* LangChain
* LangChain Community
* LangChain Classic
* LangChain OpenAI
* LangChain Ollama
* LangChain Google GenAI

### Model Providers

* OpenAI-compatible APIs
* Ollama (local models)
* Google Gemini

### Vector Databases

* FAISS
* ChromaDB

### Document Processing

* PyPDF
* Unstructured
* jq

### Utilities

* Python Dotenv
* Grandalf
* Rank-BM25

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/msgayathridevi/langchain-fundamentals.git
cd langchain-project
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**macOS/Linux**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_api_key_here
GOOGLE_API_KEY=your_google_api_key_here
DEEPSEEK_API_KEY_PRO=your_provider_key_here
```

Never commit secret keys to GitHub.

---

## How to Use

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebooks sequentially:

1. `01_llm.ipynb`
2. `02_prompt_template.ipynb`
3. `03_structured_output.ipynb`
4. `04_output_parser.ipynb`
5. `05_chain.ipynb`
6. `06_document_loader.ipynb`
7. `07_text_splitters.ipynb`
8. `08_embeddings.ipynb`
9. `09_vector_stores.ipynb`
10. `10_retrievers.ipynb`

This order provides a progressive learning path from fundamentals to advanced retrieval workflows.

---

## Key Learning Outcomes

By completing this repository, you will understand how to:

* Build LangChain-powered applications
* Engineer effective prompts
* Parse and structure LLM outputs
* Process real-world documents
* Generate and compare embeddings
* Build semantic search systems
* Store vectors in FAISS and ChromaDB
* Implement advanced retrieval strategies
* Prepare for Retrieval-Augmented Generation (RAG) projects

---

## License

This project is distributed under the terms of the included `LICENSE` file.

---

## Author

**Gayathri Devi MS**

LangChain enthusiast focused on practical, hands-on AI engineering and developer education.
