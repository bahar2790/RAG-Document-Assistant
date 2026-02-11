📄 LLM-Powered PDF Research Assistant (RAG)
An end-to-end Retrieval Augmented Generation (RAG) system that automatically extracts structured academic information from research papers.
Users upload a PDF and the system processes the document, retrieves the most relevant evidence, and generates reliable, explainable outputs such as title, authors, publication year, and summary.
Built with LangChain + OpenAI + ChromaDB + Streamlit + Docker.

📄 [📄 Open the App on Streamlit](https://rag-document-assistant-bahar.streamlit.app/)

<img width="1536" height="1024" alt="image2" src="https://github.com/user-attachments/assets/47cc37a4-6da9-4029-a923-2ce1d2aad13b" />

---
🚀 Features

✅ Upload research PDFs

✅ Automatic document parsing

✅ Intelligent text chunking

✅ OpenAI embeddings

✅ Persistent Chroma vector database

✅ Retrieval of relevant evidence

✅ Structured information extraction

✅ Source-grounded outputs

✅ Transparent reasoning

✅ Container-ready deployment

🧠 How It Works

A PDF document is uploaded.
The file is loaded using PyPDFLoader.
Text is split into semantic chunks.
OpenAI embeddings are created.
Chunks are stored in ChromaDB.
A predefined extraction prompt runs on the retriever.
The LLM generates:
Title
Authors
Publication date
Summary
Supporting source passages
This ensures answers are traceable and verifiable.

🏗️ Tech Stack

Python
Streamlit
LangChain
OpenAI
ChromaDB
Pydantic
Docker


---

## ▶️ Run Locally (Without Docker)

```bash
pip install -r app/requirements.txt
streamlit run app/streamlit_app.py

🐳 Run With Docker
Build image
docker build -t pdf-rag ./app

Run container
docker run -p 8501:8501 pdf-rag

Open in browser:
http://localhost:8501

🔑 API Key
Users provide their OpenAI API key at runtime from the interface.
Keys are never stored.
.
├── app/
│   ├── dockerfile
│   ├── functions.py
│   ├── requirements.txt
│   └── streamlit_app.py
├── data/
│   └── sample.pdf
├── .gitignore
└── data_extraction_llms.ipynb


📊 Output
The system produces structured, explainable results including:
Extracted information
Source text chunks
Model reasoning
Designed for trust, transparency, and auditability.

💼 Use Cases
Literature review automation
Academic research assistance
Scientific document analysis
Metadata extraction from PDFs

👩‍💻 Author
Bahar Akay
Data Scientist | AI & RAG Systems
