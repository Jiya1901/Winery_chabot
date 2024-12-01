![Screenshot 2024-12-01 221309](https://github.com/user-attachments/assets/ecea097d-f1b5-4f4f-9dc3-f6a92ea29ab9)
**Solution.AI - Ask Your PDF** 💬
Welcome to Solution.AI, a Streamlit-based application that allows you to interact with and ask questions about the content of a PDF file. Powered by cutting-edge AI tools, the app extracts text from a PDF, processes it into manageable chunks, and uses an LLM-powered Question Answering (QA) chain to answer user queries.
_____________________________________________________________________________________________________

**Features**
PDF Upload: Upload a PDF file and analyze its contents.
Text Extraction: Extracts text from all pages of the uploaded PDF.
Chunking: Splits text into smaller chunks for efficient processing.
Embeddings: Creates vector representations of text using OpenAI embeddings.
Knowledge Base: Constructs a FAISS-based knowledge base for similarity search.
Interactive Q&A: Allows users to input questions and get AI-generated answers.
_____________________________________________________________________________________________________


**Installation**

Clone the repository:
	git clone <repository-url>
	cd <repository-name>

Install dependencies: 
Ensure you have Python 3.8+ installed. Run:
	pip install -r requirements.txt

Set up environment variables:
Create a .env file in the root directory.
Add your OpenAI API key:
	OPENAI_API_KEY=your_api_key_here
_____________________________________________________________________________________________________

**Usage**
Run the Streamlit app:
	streamlit run app.py

Upload a PDF file when prompted in the app interface.

Enter a question in the input field and get instant answers based on the content of the PDF.
_____________________________________________________________________________________________________

**Project Structure**
.
├── app.py                # Main application script
├── requirements.txt      # Dependencies for the project
├── README.md             # Project documentation
└── .env.example          # Example environment variable file
_____________________________________________________________________________________________________

**Future Enhancements:**

Add support for multiple document uploads.
Implement advanced error handling for unsupported PDFs.
Introduce multi-language support.
Enable persistent knowledge bases for large datasets.
