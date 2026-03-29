# 📄 Talk-To-PDF

Talk-To-PDF is a RAG-based document assistant designed to perform context-aware question answering over multiple PDF files. It extracts and chunks document content, retrieves relevant information using vector similarity search, and generates grounded responses via a conversational AI model, ensuring answers remain aligned with the source documents.

---

## 🚀 Features

- **Batch PDF Processing** – Upload and handle multiple PDF files simultaneously  
- **Text Extraction & Segmentation** – Pulls text from documents and breaks it into manageable chunks for better retrieval  
- **Embedding-Based Search** – Uses vector embeddings and similarity matching to fetch relevant context  
- **AI-Powered Conversations** – Powered by Google Gemini for natural language interaction  
- **User-Friendly Chat UI** – Clean and intuitive interface built with Streamlit  

---

## 🏗️ Project Structure
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


---

## ⚙️ Technologies Used

This project is built using the following technologies:

- **Python** – Backend logic  
- **Streamlit** – Web interface  
- **LangChain** – AI pipeline construction  
- **Google Gemini API** – Embeddings and LLM responses  
- **FAISS** – Vector database and similarity search  
- **PyPDF2** – PDF text extraction  
- **python-dotenv** – Secure API key management  

---

## 🧠 How It Works

### 1. PDF Upload
Users upload PDF files through the Streamlit interface.

### 2. Text Extraction
Text is extracted from each page using PyPDF2.

### 3. Text Chunking
The extracted text is split into smaller chunks using LangChain’s text splitter.

### 4. Embeddings Creation
Each chunk is converted into vector embeddings using Google Gemini.

### 5. Vector Storage
Embeddings are stored in FAISS for fast similarity search.

### 6. User Query
When a user asks a question, the system searches for relevant chunks.

### 7. Answer Generation
Gemini LLM generates a response based on the retrieved context.
