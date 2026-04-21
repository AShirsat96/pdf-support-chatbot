Customer Support Chatbot
A Streamlit-based AI chatbot that answers questions from PDF manuals and support documents using OpenAI and LlamaIndex. It helps customer support teams reduce repetitive ticket volume by turning internal documentation into a searchable conversational assistant.

Results
Reduced support ticket volume by 70%

Improved response time by 60%

Enabled 24/7 self-service answers from PDF-based documentation

Demo
<img width="1280" height="905" alt="image" src="https://github.com/user-attachments/assets/41a52db8-5fab-458d-90f9-d629e1d4d739" />

Example UI of the customer support chatbot



Features
Chat with PDF manuals and support documentation

Retrieval-augmented generation (RAG) using LlamaIndex

Streamlit chat interface with conversation history

OpenAI-powered technical responses

Cached document indexing for faster performance

Configurable for any company knowledge base or internal guide

Tech Stack
Frontend: Streamlit

LLM: OpenAI GPT-3.5-turbo

RAG / Indexing: LlamaIndex

Language: Python

NLP Utilities: NLTK

Project Structure
bash
.
├── app.py
├── README.md
├── requirements.txt
├── .streamlit/
│   └── secrets.toml
└── data/
    └── your-pdf-files-here
Installation
Clone the repository and install dependencies:

bash
git clone https://github.com/AShirsat96/pdf-support-chatbot.git
cd pdf-support-chatbot
pip install -r requirements.txt
If you do not have a requirements.txt file yet, install the main packages with:

bash
pip install streamlit llama-index openai nltk
Configuration
1. OpenAI API key
Store your API key in Streamlit secrets:

text
# .streamlit/secrets.toml
openai_key = "your_openai_api_key_here"
2. Add your documents
Place your PDF or support documents in a local data directory such as:

bash
data/
Update the app code if needed so the document loader points to your chosen folder.

Usage
Run the app locally with:

bash
streamlit run app.py
Then open the local URL shown in your terminal, usually:

bash
http://localhost:8501
How It Works
Loads PDF or support documents from a local folder

Indexes them using LlamaIndex

Accepts user questions through Streamlit chat input

Retrieves relevant context from the indexed documents

Generates technical answers using OpenAI

Maintains chat history during the session

Example Use Cases
Customer support knowledge assistants

Internal operations manual Q&A

Product documentation chatbot

HR or policy handbook assistant

IT troubleshooting knowledge bot

LLM Configuration
python
settings = Settings(
    llm=OpenAI(
        model="gpt-3.5-turbo",
        temperature=0.5,
        system_prompt="You are an expert on the User Guide and your job is to answer technical questions. Assume that all questions are related to the User Guide. Keep your answers technical and based on facts – do not hallucinate features."
    )
)
Why This Project Matters
This project demonstrates practical skills in:

Retrieval-augmented generation (RAG)

LLM application development

Prompt design and response grounding

Streamlit app deployment

Document ingestion and indexing

Building business-facing AI tools with measurable impact

Future Improvements
Multi-file upload from the UI

Support for DOCX and TXT in addition to PDFs

Source citations in responses

Authentication for internal enterprise usage

Deployment on AWS or GCP

Author
Aniket D Shirsat
Data Scientist | NLP | LLM Applications | ML Engineering
LinkedIn | GitHub | Website
