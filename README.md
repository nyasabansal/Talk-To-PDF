# Talk-To-PDF
It is a RAG-based document assistant designed to perform context-aware question answering over multiple PDF files. It extracts and chunks document content, retrieves relevant information using vector similarity search, and generates grounded responses via a conversational AI model, ensuring answers remain aligned with the source documents.
**Features**
Multi-PDF Upload – Upload and process multiple PDF documents at once
Text Extraction & Chunking – Extracts and segments document text for efficient retrieval
Vector-Based Retrieval – Uses embeddings and similarity search to fetch relevant context
Conversational AI – Powered by Google Gemini for natural language interaction
Interactive Chat Interface – Simple and intuitive Streamlit-based UI

**Project Structure**

[ User Uploads PDF ]
            │
            ▼
[ PDF Input via Streamlit UI ]
            │
            ▼
[ Text Extraction ]
(PyPDF2 extracts text page by page)
            │
            ▼
[ Text Chunking ]
(LangChain Text Splitter divides into smaller chunks)
            │
            ▼
[ Embedding Generation ]
(Google Gemini converts text → vector embeddings)
            │
            ▼
[ Vector Storage ]
(FAISS stores embeddings for similarity search)
            │
────────────┼────────────────────────────
            │
            ▼
     [ User Query Input ]
            │
            ▼
[ Query Embedding ]
(Convert query into vector using Gemini)
            │
            ▼
[ Similarity Search ]
(FAISS retrieves most relevant chunks)
            │
            ▼
[ Context Retrieval ]
(Top matching text chunks selected)
            │
            ▼
[ Answer Generation ]
(Gemini LLM generates response using context)
            │
            ▼
[ Final Answer Displayed to User ]

⚙️**Technologies Used**
“This project is built using the following technologies:
Python – for backend logic
Streamlit – for creating the web interface
LangChain – to build the AI pipeline
Google Gemini API – for embeddings and LLM responses
FAISS – for vector database and similarity search
PyPDF2 – for extracting text from PDFs
dotenv – for managing API keys securely
These tools together help in building a complete AI-powered system.”

🧠 **How It Works**

**PDF Upload**
User uploads PDF files using Streamlit
**Text Extraction**
Using PyPDF2, text is extracted from each page
**Text Chunking**
The text is split into smaller chunks using LangChain’s text splitter
**Embeddings Creation**
Each chunk is converted into vector embeddings using Google Gemini
**Vector Storage**
These embeddings are stored in FAISS for fast retrieval
**User Query**
When a user asks a question, the system searches for relevant chunks
**Answer Generation**
Gemini LLM generates a response based on the retrieved context
