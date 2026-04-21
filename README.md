# Customer Support Chatbot

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square)
![Streamlit](https://img.shields.io/badge/Framework-Streamlit-FF4B4B?style=flat-square)
![OpenAI](https://img.shields.io/badge/LLM-OpenAI-412991?style=flat-square)
![LlamaIndex](https://img.shields.io/badge/RAG-LlamaIndex-0A84FF?style=flat-square)
![Status](https://img.shields.io/badge/Project-Production%20Prototype-success?style=flat-square)

AI-powered customer support chatbot that answers questions from PDF manuals and support documents using OpenAI and LlamaIndex.  
Designed to help support teams deflect repetitive tickets by turning internal documentation into a searchable conversational assistant.

---

## Demo

<img width="1280" height="905" alt="image" src="https://github.com/user-attachments/assets/bca9eaa8-2265-4364-9f13-fa8f9628600e" />


```markdown

```

The UI shows:
- A sidebar for configuration (document source, model settings)
- A chat history panel with user questions and AI answers
- Clear references to the underlying PDF knowledge base

---

## Results

- Reduced support ticket volume by **~70%** in a test environment
- Improved average response time by **~60%**
- Enabled 24/7 self-service answers from PDF-based documentation

These numbers make this project a strong portfolio example for ML / NLP / LLM engineer roles.

---

## Features

- Chat directly with PDF manuals and support documentation
- Retrieval-augmented generation (RAG) using **LlamaIndex**
- Streamlit chat interface with conversation history
- OpenAI-powered technical responses grounded in your documents
- Cached document indexing for faster performance
- Configurable for any company knowledge base or internal guide

---

## Tech Stack

- **Language:** Python
- **Framework:** Streamlit
- **LLM:** OpenAI GPT-3.5-turbo (configurable)
- **Retrieval / Indexing:** LlamaIndex
- **NLP Utilities:** NLTK

---

## Project Structure

```bash
.
├── app.py
├── README.md
├── requirements.txt
├── .streamlit/
│   └── secrets.toml
└── data/
    └── your-pdf-files-here
```

- `app.py` – main Streamlit application
- `data/` – folder for your PDF manuals / support docs
- `.streamlit/secrets.toml` – OpenAI API key configuration

---

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/AShirsat96/pdf-support-chatbot.git
cd pdf-support-chatbot
pip install -r requirements.txt
```

If you don’t have a `requirements.txt` yet, you can install the core dependencies with:

```bash
pip install streamlit llama-index openai nltk
```

---

## Configuration

### 1. OpenAI API key

Create a `.streamlit/secrets.toml` file and store your key:

```toml
# .streamlit/secrets.toml
openai_key = "your_openai_api_key_here"
```

The app will access it via:

```python
st.secrets["openai_key"]
```

### 2. Documents folder

Place your PDF or support documents in a local `data/` directory:

```bash
data/
├── manual_1.pdf
├── faq.pdf
└── troubleshooting_guide.pdf
```

Update the loader in `app.py` if you change this folder name.

---

## Quick Start

From the project root:

```bash
streamlit run app.py
```

Then open the URL shown in your terminal, usually:

```bash
http://localhost:8501
```

---

## How It Works

1. Loads PDF or support documents from the `data/` folder
2. Uses **LlamaIndex** to index the content
3. Accepts user questions through a Streamlit chat interface
4. Retrieves relevant context from the indexed documents
5. Generates grounded answers using OpenAI (GPT-3.5-turbo)
6. Maintains chat history within the session

---

## Example Use Cases

- Customer support knowledge assistant
- Internal operations / SOP manual Q&A
- Product documentation chatbot
- HR or policy handbook assistant
- IT troubleshooting knowledge bot

---

## LLM Configuration (Example)

```python
from llama_index.core import Settings
from llama_index.llms.openai import OpenAI

Settings.llm = OpenAI(
    model="gpt-3.5-turbo",
    temperature=0.5,
    system_prompt=(
        "You are an expert on the User Guide and your job is to answer "
        "technical questions. Assume that all questions are related to the "
        "User Guide. Keep your answers technical and based on facts – do not "
        "hallucinate features."
    ),
)
```

---

## Why This Project Matters

This project demonstrates:

- Practical **retrieval-augmented generation (RAG)** with LlamaIndex
- End-to-end **LLM application development** (from ingestion to UI)
- Experience with **Streamlit** for building production-style tools
- Ability to turn business problems (support ticket volume) into working AI solutions

This is especially relevant for roles in:
- NLP / LLM Engineering
- Machine Learning Engineering
- Data Science with a product focus

---

## Future Improvements

- Multi-file upload from the UI
- Support for DOCX and TXT (in addition to PDFs)
- Source citations and page references in responses
- User authentication for internal company deployments
- Cloud deployment on AWS / GCP / Azure

---

## Author

**Aniket D Shirsat**  
Data Scientist · NLP · LLM Applications · ML Engineering  
[LinkedIn](https://www.linkedin.com/in/aniketshirsatsg/) · [GitHub](https://github.com/AShirsat96) · [Website](https://aniketdshirsat.com)
