# ChatPDF: AI Powered Document QA System 📄🤖

ChatPDF is an AI-powered Question Answering (QA) system that allows users to upload PDF documents and interact with them using natural language queries. This project leverages advanced language models and retrieval techniques to provide accurate answers based on the content of the uploaded PDFs.

## 🔍 Features

- 📤 Upload PDF documents for analysis
- 🤖 Ask questions about the content of the uploaded documents
- 🔎 Retrieval-Augmented Generation (RAG) pipeline for high-quality answers
- ⚡ Fast and efficient document processing using LangChain and Hugging Face Transformers
- 🧠 Custom embedding model for better document understanding
- 🖥️ User-friendly web interface powered by Streamlit

---

## 🧰 Tech Stack

- **Frontend/UI**: Streamlit
- **Backend**: Python
- **LLM**: Hugging Face Transformers (`Qwen/Qwen1.5-7B-Chat`)
- **Vector Store**: FAISS
- **Embeddings**: `colbert` via HuggingFace
- **PDF Parsing**: PyMuPDF (`fitz`)
- **Document Chunking**: LangChain Text Splitters
- **RAG**: Custom pipeline using `langchain` and `transformers`

---

## 🛠️ Installation

1. **Clone the repository**
 ```bash
git clone https://github.com/Praneeth-srisurya/ChatPDF-AI-Powered-Document-QA-System.git
cd ChatPDF-AI-Powered-Document-QA-System
```
2.**Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3.**Install dependencies**
```bash
pip install -r requirements.txt

```
4.**Download the embedding model**
```bash
huggingface-cli login
# Accept model license
transformers-cli download facebook/colbert

```
---
## 🚦 Usage

1.**Run the app**
```bash
streamlit run app.py
```
2.**Upload a PDF and Ask Questions**
- Upload one or more academic documents (timetables, syllabi, etc.)
- Enter a question like: "When does the semester start?" or "What are the core subjects in 3rd semester?"
- The system retrieves relevant chunks and generates a precise response.
---
## 🧠 How It Works

1.PDF Upload → parsed and chunked

2.Embeddings → generated using colbert

3.FAISS → used to retrieve top-k relevant document chunks

4.LLM → answers are generated with Qwen1.5-7B-Chat using LangChain

5.Response → returned to the user via Streamlit UI

---
## 📁 Project Structure
```
├── app.py         # Streamlit app frontend
├── rag.py         # Core RAG pipeline (embedding, retrieval, generation)
├── requirements.txt
└── README.md

```
---
## 📌 Requirements

Python >= 3.9

CUDA-compatible GPU (recommended for LLM inference)

Hugging Face Token (for model access)

Internet connection (for downloading models)

---
## ✨ Acknowledgements
LangChain

Hugging Face Transformers

FAISS by Facebook AI

Streamlit

Qwen1.5-7B-Chat by Alibaba

---
## 🧑‍💻 Author

- Praneeth-Srisurya
 🔗 GitHub
---
## 🛡️ License
This project is licensed under the MIT License. See LICENSE for details.


---



