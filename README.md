# 📚 Retrieval-Augmented Generation (RAG) – Generative AI Lab Project

This repository contains my implementation of a **Retrieval-Augmented Generation (RAG)** pipeline, developed as part of the *Generative AI Lab (Course 94-844)* at **Carnegie Mellon University**. The goal is to combine **custom document retrieval** with **LLM-based response generation** — giving large language models the ability to respond with grounded, contextual knowledge.

---

## 🔍 What is RAG?

RAG combines:
- **Document Embedding** → using models like `sentence-transformers`
- **Vector Indexing** → storing document chunks in Pinecone
- **Contextual Retrieval** → querying the vector store for relevant content
- **LLM Augmentation** → passing the retrieved chunks to an LLM like OpenAI’s GPT-4 for contextual responses

This lets you build LLM-powered tools that can *“read” your data* and return relevant, accurate results.

---

## 📂 Repository Structure
├── hw2-rag.ipynb              # Main Jupyter notebook
├── HW2-RAG.pdf                # Project documentation and instructions
├── requirements.txt           # All Python dependencies
├── /docs                      # [Optional] Evaluation results or writeups
└── README.md
---

## ⚙️ How to Run This Project

### ✅ Prerequisites

- Python 3.10 or later (recommended: 3.12+)
- Jupyter Notebook / VS Code
- API keys for:
  - [OpenAI](https://openai.com/)
  - [Pinecone](https://www.pinecone.io/)
  - [HuggingFace](https://huggingface.co/)

---

### 💻 Local Setup Instructions

1. **Clone the Repo**

```bash
git clone https://github.com/your-username/rag-project.git
cd rag-project
2. **Create a Virtual Environment**
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
3.	**Install Dependencies**
pip install -r requirements.txt
4. **Add Environment Variables**
Create a .env file or define the following in your notebook:
OPENAI_API_KEY=your_openai_key
PINECONE_API_KEY=your_pinecone_key
HUGGINGFACE_API_KEY=your_huggingface_token
5.	**Run the Notebook**
jupyter notebook hw2-rag.ipynb

Follow the notebook instructions to:
	•	Upload a document (e.g., CMU Handbook PDF)
	•	Chunk it into sections
	•	Embed with sentence-transformers
	•	Store in Pinecone
	•	Query and generate LLM responses

📈 Sample Use Cases
	•	Internal company document Q&A
	•	Policy retrieval for HR/legal teams
	•	Research assistants that cite sources
	•	AI agents with long-term memory
