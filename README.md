# 📚 Multi-Format Document Chat App with LangChain & Streamlit

## 📌 **Project Overview**
Welcome to the **Multi-Format Document Chat App**! This intelligent Streamlit application enables users to upload and chat with documents of various formats including PDF, Word, Excel, PowerPoint, Text, HTML, and CSV. It leverages LangChain, HuggingFace embeddings, and ChromaDB to perform document parsing, semantic search, and natural language querying — all from your browser.

---

## 📂 **Supported File Formats**

| Format     | Extensions                | Loader Used                      |
|------------|---------------------------|----------------------------------|
| 📄 PDF     | `.pdf`                    | `PyPDFLoader`                    |
| 📝 Word    | `.docx`, `.doc`           | `Docx2txtLoader`                 |
| 📊 PPT     | `.pptx`, `.ppt`           | `UnstructuredPowerPointLoader`   |
| 📈 Excel   | `.xlsx`, `.xls`           | `UnstructuredExcelLoader`        |
| 📋 Text    | `.txt`                    | `TextLoader`                     |
| 🌐 HTML    | `.html`                   | `Raw HTML Parser`                |
| 📊 CSV     | `.csv`                    | `pandas` CSV to string parser    |

---

## 🔍 **Core Features**

- 📤 Upload documents of multiple types  
- 🧠 Extract, clean, and chunk document content automatically  
- 📦 Generate vector embeddings using HuggingFace transformers  
- 🧠 Store and retrieve chunks with ChromaDB for semantic Q&A  
- 💬 Ask questions about document content using a LLM  
- 📊 View real-time insights about your document library in the sidebar  
- 🗂️ Reuse, delete, or reload previous documents seamlessly

---

## 🛠️ **Technologies Used**

- **LangChain** – For document loading, chunking, and chaining
- **HuggingFace Embeddings** – Sentence-transformers for vectorization
- **ChromaDB** – Lightweight, local vector database
- **Together AI (LLaMA 3)** – Powerful open-source LLM interface
- **Streamlit** – Fast web UI with chat and file upload components
- **dotenv, pandas, OpenCV, hashlib, JSON** – Supporting utilities

---

## 🧠 **How It Works**

1. 📂 Upload any supported document (PDF, Word, PPT, Excel, etc.)
2. 🧹 The app parses content using LangChain-compatible loaders
3. 📎 Text is split into chunks and embedded using HuggingFace models
4. 🧠 Embeddings are stored in a local ChromaDB vector store
5. 💬 When you ask a question, LangChain retrieves relevant chunks and queries a Together AI-powered LLM (e.g., LLaMA 3)
6. 🔁 Chat history is maintained for seamless conversation

---

## 📁 **Directory Structure**
project-root/
├── app.py # Main Streamlit application
├── document_metadata.json # Metadata map for uploaded documents
├── document_databases/ # Vector DB folders per document
├── .env # Your API keys
