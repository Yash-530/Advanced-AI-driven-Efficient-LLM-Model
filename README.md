# Medical Chatbot using Retrieval Augmented Generation (RAG)

## Introduction
This project implements a **Medical Chatbot** using **Retrieval Augmented Generation (RAG)**. It leverages **TheBloke/Llama-2-7B-Chat-GGML** model with **FAISS** for efficient information retrieval and LangChain for orchestration.

## Features
- **Conversational AI** using Llama-2-7B-Chat-GGML
- **Document-based Question Answering** with FAISS vector search
- **Retrieval Augmented Generation (RAG)** for accurate and context-aware responses
- **Chainlit UI integration** for chatbot interaction

## Technologies Used
- **LangChain** for orchestration
- **FAISS** for vector storage
- **Hugging Face Embeddings** for document representation
- **CTransformers** for running the LLM
- **Chainlit** for chatbot interface
- **Sentence Transformers** for efficient embeddings

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- pip
- Virtual environment (optional but recommended)

### Setup
1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd <repo-name>
   ```
2. Create and activate a virtual environment (optional):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Download the Llama-2-7B-Chat-GGML model:
   - Model binary: [Google Drive Link](https://drive.google.com/file/d/14FypECy_au1jgKlGZBBOtIGMA7EVd__N/view?usp=drive_link)
   - Place the model in the appropriate directory for usage.

## Usage
### Running the Chatbot
Start the chatbot using Chainlit:
```bash
chainlit run chatbot.py
```

### Querying the Bot
Once the chatbot starts, you can ask medical-related queries. The bot retrieves information from stored documents and generates accurate responses.

## Project Components
### 1. **Document Processing**
- Loads PDFs using `PyPDFLoader`.
- Extracts and embeds text using `HuggingFaceEmbeddings`.
- Stores processed embeddings in a **FAISS vector store**.

### 2. **Retrieval Augmented Generation (RAG)**
- Retrieves relevant document chunks based on user queries.
- Passes retrieved context to the **Llama-2-7B-Chat-GGML** model.
- Generates accurate and context-aware responses.

### 3. **Chatbot Interface**
- Uses **Chainlit** to create an interactive chatbot.
- Supports real-time responses with document citations.

## Code Structure
```
├── chatbot.py              # Main chatbot script
├── requirements.txt        # List of dependencies
├── vectorstore/            # Directory for FAISS vector storage
├── models/                 # Directory for storing Llama model files
└── README.md               # Project documentation
```

## Dependencies
Install the following dependencies:
```bash
pip install langchain chainlit sentence-transformers faiss-cpu ctransformers pdf2image pypdf xformers bitsandbytes accelerate transformers
```

## Future Enhancements
- **Expand Knowledge Base**: Integrate multiple document sources.
- **Enhance UI**: Improve Chainlit interface with more features.
- **Deploy as an API**: Create a REST API for broader accessibility.

## License
This project is open-source under the **MIT License**.

