# RAG-Based Chatbot with LangChain and Streamlit

This project implements a Retrieval-Augmented Generation (RAG) chatbot using LangChain, Google's Generative AI (Gemini), and Streamlit. The chatbot can process PDF documents and answer questions based on their content.

## Features

- 📄 PDF document processing and chunking
- 🔍 Semantic search using Google's Generative AI embeddings
- 💬 Interactive chat interface with Streamlit
- 📚 Source document tracking and citation
- 🔄 Dynamic document management (add/remove documents)
- 🎯 Accurate responses based on document content

## Prerequisites

- Python 3.8 or higher
- Google API key for Generative AI
- Required Python packages (see requirements.txt)

## Setup

1. Clone the repository:
```bash
git clone [your-repository-url]
cd RAG-Chat
```

2. Create and activate a virtual environment:
```bash
python -m venv .venv
# On Windows
.venv\Scripts\activate
# On Unix or MacOS
source .venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root and add your Google API key:
```
GOOGLE_API_KEY=your_api_key_here
```

## Running the Application

1. Start the Streamlit app:
```bash
streamlit run app.py
```

2. Open your web browser and navigate to the URL shown in the terminal (typically http://localhost:8501)

3. Upload PDF documents using the sidebar

4. Process the documents by clicking "Process Uploaded Documents"

5. Start chatting with the bot!

## Project Structure

- `app.py` - Main Streamlit application
- `config.py` - Configuration settings
- `document_processor.py` - PDF loading and text chunking
- `rag_chain.py` - RAG pipeline implementation
- `vector_store.py` - Vector store management
- `requirements.txt` - Project dependencies
- `sample_responses.txt` - Example questions and responses

## Usage

1. Upload PDF documents using the sidebar
2. Process the documents to create embeddings
3. Ask questions in the chat interface
4. View source documents for each response
5. Manage documents (add/remove) as needed

## Notes

- The chatbot uses Google's Generative AI (Gemini) for both embeddings and text generation
- Documents are stored in a local ChromaDB vector store
- All processing is done locally after initial document upload
- Source citations are provided for each response
