# **End-to-End RAG App using AWS Bedrock, LangChain & Streamlit**

This project demonstrates how to build a complete **Retrieval-Augmented Generation (RAG)** system using:

* **AWS Bedrock** for LLMs & embeddings
* **LangChain** for orchestration and retrieval pipelines
* **Streamlit** for a clean, interactive UI

The application allows users to **upload documents**, **create embeddings**, **store vectors**, and **query them with Bedrock models** — enabling accurate, context-aware answers.

---

## 🚀 **Features**

### 🔹 **1. Document Ingestion**

* Upload PDFs, text files, or multiple documents.
* Extracts and preprocesses text automatically.

### 🔹 **2. Vector Embeddings with AWS Bedrock**

* Uses Bedrock embedding models to generate document embeddings.
* Stores vectors in an in-memory or external vector database (depending on your setup).

### 🔹 **3. RAG Pipeline using LangChain**

* Implements retrieval chains.
* Fetches relevant chunks based on user queries.
* Sends context + query to an AWS Bedrock LLM for grounded answers.

### 🔹 **4. Streamlit Frontend**

* Clean and interactive UI.
* Upload docs, run queries, inspect responses.
* Real-time outputs and debugging sidebar.

---

## 🛠️ **Tech Stack**

| Component                 | Technology                       |
| ------------------------- | -------------------------------- |
| LLM & Embeddings          | **AWS Bedrock**                  |
| Retrieval & Orchestration | **LangChain**                    |
| UI                        | **Streamlit**                    |
| Vector Storage            | FAISS / In-memory (configurable) |
| Backend                   | Python 3.x                       |

---

## 📂 **Project Structure**

```
📦 rag-bedrock-app
├── app.py                 # Streamlit application
├── config.py              # AWS & Bedrock configuration
├── ingestion.py           # Document loader & chunker
├── vectorstore.py         # Vector DB logic
├── rag_pipeline.py        # LangChain RAG chain
├── requirements.txt
└── README.md
```

---

## 🔧 **Setup Instructions**

### **1. Clone the repository**

```bash
git clone https://github.com/your-username/rag-bedrock-app.git
cd rag-bedrock-app
```

### **2. Install dependencies**

```bash
pip install -r requirements.txt
```

### **3. Configure AWS Credentials**

Make sure your environment has:

```
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=
```

Also ensure Bedrock access is enabled in your AWS console.

### **4. Run the Streamlit App**

```bash
streamlit run app.py
```

---

## 🧪 **How It Works**

1. User uploads documents.
2. Text is chunked and embedded using Bedrock Embedding Model.
3. Vectors stored in vector DB.
4. User enters a question.
5. Retriever fetches top-k relevant chunks using similarity search.
6. Context + query sent to Bedrock LLM.
7. Final answer is presented in the UI.

---

## 🤝 **Contributing**

Pull requests are welcome! Feel free to open issues for improvements or feature suggestions.

---

## 📜 **License**

MIT License.

---
