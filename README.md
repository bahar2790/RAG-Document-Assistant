📄 LLM-Powered PDF Research Assistant (RAG)

An end-to-end **Retrieval Augmented Generation (RAG)** application that allows users to upload a research PDF and automatically extract structured bibliographic information with supporting sources and reasoning.



Built with **LangChain + OpenAI + ChromaDB + Streamlit + Docker**.

📄 [Uygulamayı Streamlit’de Aç](https://llm-powered-pdf-research-assistant-rag.streamlit.app/)


---
<img width="1280" height="800" alt="Ekran Resmi 2026-02-09 18 10 24" src="https://github.com/user-attachments/assets/923b8a5f-fe9e-4b3d-907e-f634e73903a6" />




## 🚀 Features

✅ Upload PDF  
✅ Automatic parsing  
✅ Text chunking  
✅ OpenAI embeddings  
✅ Persistent Chroma vector database  
✅ Similarity search  
✅ Structured answers  
✅ Source citation  
✅ Reasoning transparency  
✅ Containerized setup  

---

## 🧠 How It Works

1. Upload PDF.
2. Document is loaded via `PyPDFLoader`.
3. Split into chunks.
4. Embeddings created using OpenAI.
5. Stored in persistent ChromaDB.
6. Retriever finds relevant parts.
7. `gpt-4.1-mini` generates:
   - Answer  
   - Source  
   - Reasoning  

---

## 🏗️ Tech Stack

- Python  
- Streamlit  
- LangChain  
- OpenAI  
- ChromaDB  
- Pydantic  
- Docker  

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

📂 Project Structure
.
├── app/
│   ├── dockerfile
│   ├── functions.py
│   ├── requirements.txt
│   └── streamlit_app.py
├── .env
├── .gitignore
└── data_extraction_llms.ipynb

📊 Output
The system returns a table containing:
Answer
Source chunk
Reasoning
Ensuring explainability and traceability.

💼 Use Cases
Literature review
Academic research
Medical/scientific analysis
Structured info extraction

👩‍💻 Author
Bahar Akay
Data Scientist | AI & RAG Systems
