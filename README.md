![Screenshot 2024-11-10 222012](https://github.com/user-attachments/assets/34c78fce-d587-4e82-bdaa-33b0f2c1e2e4)
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
```

### 2. Install Dependencies
Install the required Python packages:
```bash
pip install groq langchain langchain-core langchain-groq qdrant-client pypdf gradio
pip install langchain-community
pip install -U langchain-ollama
pip install chromadb
```

### 3. Pull Necessary Models
```bash
!ollama pull nomic-embed-text
```

### 4. Set Environment Variables
Add your groq_api_key in the env.py file:
```python
groq_api_key = "your_groq_api_key"
```
---

##Usage
### 1. Prepare Your PDFs
Place your vineyard-related PDF documents in the data folder.
### 2. Run the Application
Launch the chatbot interface using:
```bash
python app.py
```
### 3. Interact with VineWise
Open the generated Gradio link in your browser and start asking questions about vineyard tourism.

---

##Key Components
### **1. RAG Pipleline**
- **Document Loader**: Loads and processes PDF documents using PyPDFDirectoryLoader.
- **Text Splitter**: Splits documents into manageable chunks with overlap for context preservation.
- **Vector Store**: Stores document embeddings in a Chroma vector database for efficient similarity search.
- **RAG Prompt**: Custom prompt template for context-aware question answering.
### **2. Gradio Interface**
Provides a user-friendly chat interface to ask questions dynamically and view responses with response times.
### **3. Groq LLM**
Uses the mixtral-8x7b-32768 model for high-quality and precise responses.

---

##**Project Structure**
```bash
.
├── data/                        # Folder for input PDF documents
├── app.py                       # Main application script
├── env.py                       # Environment variable file for API keys
├── requirements.txt             # Dependencies list
├── README.md                    # Project documentation
└── other supporting files
```

---

## **Dependencies**

The project requires the following Python libraries and tools:

### Core Dependencies

| Package                         | Version (if specified)       | Description                                                              |
|---------------------------------|------------------------------|--------------------------------------------------------------------------|
| `groq`                          | Latest                       | Provides integration with Groq models for LLM processing.                |
| `langchain`                     | Latest                       | Framework for building language model applications.                      |
| `langchain-core`                | Latest                       | Core components of the LangChain library.                                |
| `langchain-groq`                | Latest                       | LangChain integration with Groq models.                                  |
| `qdrant-client`                 | Latest                       | Client library for Qdrant vector database integration.                   |
| `pypdf`                         | Latest                       | Library for reading and parsing PDF documents.                           |
| `gradio`                        | Latest                       | Easy-to-use web UI for machine learning applications.                    |
| `langchain-community`           | Latest                       | Community-supported modules for LangChain.                               |
| `langchain-ollama`              | Latest                       | Integration of Ollama models with LangChain.                             |
| `chromadb`                      | Latest                       | Embedding-based vector database for managing and retrieving document embeddings. |

### Additional Tools

| Tool                            | Description                                                      |
|---------------------------------|------------------------------------------------------------------|
| `ollama`                        | Model manager for pulling models like `nomic-embed-text`.        |

### Environment
- Python 3.9 or higher
- API keys:
  - `groq_api_key`: Required for Groq LLM integration. Add to `env.py`.

---

## **Future Enhancements**
- Support for multi-file uploads.
- Add persistent storage for knowledge bases.
- Extend the chatbot to handle non-PDF file formats.
- Introduce multilingual support.
