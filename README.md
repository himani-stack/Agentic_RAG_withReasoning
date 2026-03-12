# Agentic RAG System with Reasoning

An **Agentic Retrieval-Augmented Generation (RAG) application** that enables users to query dynamically added web knowledge sources while visualizing the AI agent’s **step-by-step reasoning process** in real time.

This project integrates **LLM reasoning, semantic search, and vector databases** to build an interactive AI assistant capable of retrieving relevant knowledge and generating contextual answers with **source citations**.

---

# Features

## Interactive Knowledge Base Management

- Dynamically add **web URLs** as knowledge sources
- Default preloaded article: **MCP vs A2A Protocol**
- Persistent vector storage using **LanceDB**
- Prevents duplicate document ingestion using **session state tracking**

---

## Transparent Reasoning Process

- Displays the **agent’s reasoning steps in real time**
- Side-by-side visualization of:
  - reasoning process
  - final generated answer
- Helps users understand how the AI arrives at conclusions

---

## Advanced RAG Capabilities

- **Semantic vector search** using OpenAI embeddings
- Efficient document retrieval from the knowledge base
- **Source attribution and citations** for generated answers

---

# Tech Stack

- **Frontend:** Streamlit  
- **Agent Framework:** Agno v2.0  
- **Language Model:** Gemini 2.5 Flash  
- **Embeddings:** OpenAI Embeddings  
- **Vector Database:** LanceDB  
- **Language:** Python  

---

# Architecture Overview

The system follows a **Retrieval-Augmented Generation pipeline**.

### 1 Document Ingestion
URLs are loaded using Agno’s Knowledge class and the content is chunked.

### 2 Embedding Generation
Text chunks are converted into vector embeddings using OpenAI.

### 3 Vector Storage
Embeddings are stored in **LanceDB** for efficient retrieval.

### 4 Semantic Retrieval
User queries are embedded and the system retrieves the most relevant content.

### 5 Agent Reasoning
ReasoningTools enable the agent to perform **step-by-step analysis**.

### 6 Answer Generation
Gemini 2.5 Flash generates the final response with **citations and context awareness**.

---

# Prerequisites

You need the following API keys.

## Google API Key

1 Go to  
https://aistudio.google.com/apikey

2 Create a new API key.

---

## OpenAI API Key

1 Go to  
https://platform.openai.com/

2 Generate a new API key.

---

# Installation

Clone the repository.

```bash
git clone https://github.com/YOUR_USERNAME/agentic-rag-reasoning.git
cd agentic-rag-reasoning
```

Install dependencies.

```bash
pip install -r requirements.txt
```

---

# Run the Application

Start the Streamlit app.

```bash
streamlit run rag_reasoning_agent.py
```

---

# Application Workflow

1 Start the application  
2 Enter **Google API key**  
3 Enter **OpenAI API key**  
4 Default knowledge source loads automatically  
5 Add additional URLs to extend the knowledge base  
6 Ask questions in the input field  
7 View **reasoning process on the left panel**  
8 View **final answer with citations on the right panel**

---

# Project Structure

```
agentic-rag-reasoning
│
├── rag_reasoning_agent.py
├── requirements.txt
├── README.md
└── data/
```

---

# Future Improvements

- Support for **PDF uploads**
- Multi-agent communication
- Improved reasoning visualization
- Support for additional vector databases
- User authentication

---

# License

MIT License

---

# Acknowledgements

- Agno Framework
- Google Gemini
- OpenAI
- LanceDB
- Streamlit
