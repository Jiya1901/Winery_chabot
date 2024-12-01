# VineWise 🍇 - Vineyard Tourism Chatbot

Welcome to **VineWise**, an AI-powered chatbot designed to answer your queries related to vineyard tourism! Using advanced Retrieval-Augmented Generation (RAG) and language models, VineWise provides accurate and context-aware answers based on PDF documents you upload.

---

## Features
- **PDF Document Analysis**: Automatically loads and splits text from PDF documents stored in the `data` folder.
- **Dynamic Query Processing**: Answers user questions in real-time using a custom RAG pipeline.
- **Embeddings with Ollama**: Creates vector embeddings for efficient document search.
- **Gradio Interface**: Intuitive web-based chat interface for user interaction.
- **LLM Integration**: Leverages Groq's large language models for generating responses.

---

## Installation

### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone <repository-url>
cd <repository-directory>

### 2. Install Dependencies
Install the required Python packages:
```bash
pip install groq langchain langchain-core langchain-groq qdrant-client pypdf gradio
pip install langchain-community
pip install -U langchain-ollama
pip install chromadb

### 3. Pull Necessary Models
```bash
!ollama pull nomic-embed-text

### 4. Set Environment Variables
Add your groq_api_key in the env.py file:
```python
groq_api_key = "your_groq_api_key"

---

##Usage
### 1. Prepare Your PDFs
Place your vineyard-related PDF documents in the data folder.
### 2. Run the Application
Launch the chatbot interface using:
```bash
python app.py
### 3. Interact with VineWise
Open the generated Gradio link in your browser and start asking questions about vineyard tourism.

---

##Key Components
### 
