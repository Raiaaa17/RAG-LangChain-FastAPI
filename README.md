# RAG Chatbot with FastAPI and Streamlit

A Retrieval-Augmented Generation (RAG) chatbot that combines the power of LangChain, FastAPI, and Streamlit to provide intelligent responses based on your documents.

## Features

- **Document Upload**: Upload PDF, DOCX, or HTML documents
- **Chat Interface**: Interactive chat interface with conversation history
- **Multiple Models**: Switch between different LLM models (GPT-4o, GPT-4o-mini)
- **Document Management**: View and delete uploaded documents
- **Session Management**: Maintains conversation context using session IDs

## Tech Stack

- **Backend**: FastAPI
- **Frontend**: Streamlit
- **LLM**: OpenAI (via LangChain)
- **Vector Database**: ChromaDB
- **Document Processing**: LangChain Document Loaders

## Prerequisites

- Python 3.8+
- OpenAI API key
- pip (Python package manager)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Raiaaa17/RAG-LangChain-FastAPI.git
   cd RAG-LangChain-FastAPI
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up your environment variables:
   Create a `.env` file in the root directory and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your-api-key-here
   ```

## Running the Application

1. Start the FastAPI backend:
   ```bash
   uvicorn main:app --reload
   ```

2. In a new terminal, start the Streamlit frontend:
   ```bash
   streamlit run streamlit_app.py
   ```

3. Open your browser and navigate to `http://localhost:8501`

## Usage

1. **Upload Documents**: Use the sidebar to upload your documents
2. **Chat**: Type your question in the chat input and press Enter
3. **Switch Models**: Use the dropdown in the sidebar to switch between different LLM models
4. **Manage Documents**: View or delete uploaded documents using the sidebar

## API Endpoints

- `POST /chat`: Process chat messages
- `POST /upload-doc`: Upload a document
- `GET /list-docs`: List all uploaded documents
- `POST /delete-doc`: Delete a document

## Project Structure

```
.
├── api_utils.py       # API client utilities
├── chat_interface.py  # Streamlit chat interface
├── chroma_utils.py    # ChromaDB utilities
├── db_utils.py        # Database utilities
├── langchain_utils.py # LangChain utilities
├── main.py            # FastAPI application
├── pydantic_models.py # Pydantic models
├── requirements.txt   # Python dependencies
├── sidebar.py         # Streamlit sidebar
└── streamlit_app.py   # Main Streamlit application
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- [LangChain](https://python.langchain.com/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [Streamlit](https://streamlit.io/)
- [ChromaDB](https://www.trychroma.com/)
