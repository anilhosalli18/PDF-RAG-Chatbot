# 📚 Multi-PDF RAG Chatbot

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://pdf-rag-chatbot-g53vwekltbrys3cknewxth.streamlit.app)

🚀 **Live Demo:** [https://pdf-rag-chatbot-g53vwekltbrys3cknewxth.streamlit.app](https://pdf-rag-chatbot-g53vwekltbrys3cknewxth.streamlit.app)

An enterprise-grade **Retrieval-Augmented Generation (RAG)** application designed to extract, index, and query information across multiple PDF documents using state-of-the-art Large Language Models (LLMs) and Vector Embeddings.

Developed by **ANIL H**.

---

## 🌟 Key Features

- 📄 **Multi-Document PDF Processing:** Upload and parse multiple PDF files simultaneously. Uses **PyMuPDFLoader** for rapid text extraction and **UnstructuredPDFLoader** OCR fallback for scanned/image-based documents.
- ⚡ **Ultra-Fast LLM Inference:** Powered by **Groq API** (`groq/compound`, `groq/compound-mini`, `qwen/qwen3.6-27b`, `openai/gpt-oss-120b`) for near-instant answers, with seamless fallback to **OpenAI GPT-3.5/4**.
- 🧠 **Vector Embeddings & Semantic Search:** Embeds document chunks using Hugging Face's `all-mpnet-base-v2` (`sentence-transformers`) and indexes them locally with **FAISS** for fast top-$K$ context retrieval.
- 🎯 **Source Citations & Debug Insights:** Every response includes verifiable source document references and transparent chunk previews.
- 🎨 **Modern Streamlit UI:** Sleek dark-mode aesthetic with interactive chat history, progress indicators, clear conversation options, and history export.
- 🔑 **Flexible API Key Management:** Supports automatic `.env` key loading, Streamlit secrets configuration, and interactive sidebar inputs.

---

## 🛠️ Tech Stack

- **Frontend & App Framework:** [Streamlit](https://streamlit.io/)
- **RAG & Orchestration:** [LangChain](https://www.langchain.com/) (LangChain Core, LangChain Community, LangChain Groq)
- **Vector Database:** [FAISS](https://github.com/facebookresearch/faiss) (Facebook AI Similarity Search)
- **Embedding Models:** [Hugging Face Transformers](https://huggingface.co/) / `sentence-transformers/all-mpnet-base-v2`
- **PDF Extraction:** PyMuPDF (`pymupdf`), PyPDF2, Unstructured
- **LLM Providers:** [Groq Cloud](https://groq.com/) & [OpenAI](https://openai.com/)

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or 3.11
- A Groq API Key ([Get one free at console.groq.com](https://console.groq.com/)) or OpenAI API Key

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/PDF_RAG_Chatbot.git
cd PDF_RAG_Chatbot
```

### 2. Create and Activate Virtual Environment

**Windows (PowerShell):**
```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
```

### 5. Launch the Application

```bash
streamlit run app.py
```

Open your browser at `http://localhost:8501`.

---

## ☁️ Deployment

### Streamlit Community Cloud (Recommended)

1. Push this repository to GitHub.
2. Visit [share.streamlit.io](https://share.streamlit.io/) and log in with GitHub.
3. Select your repository, set the main file to `app.py`.
4. Under **Advanced Settings -> Secrets**, add:
   ```toml
   GROQ_API_KEY = "your_groq_api_key_here"
   OPENAI_API_KEY = "your_openai_api_key_here"
   ```
5. Click **Deploy!**

---

## 👤 Author

**ANIL H**  
Built with LangChain, FAISS, Streamlit & Groq.
