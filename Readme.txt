# 📈 News Research Tool

An intelligent news research application that extracts, processes, and answers questions from multiple news articles using state-of-the-art language models and vector search technology.

## 🌟 Features

- Multi-URL processing (up to 3 articles)
- Intelligent text splitting and chunking
- Semantic embeddings using OpenAI
- FAISS vector store for similarity search
- Q&A interface with source attribution
- Source tracking with article references

## 🏗️ Architecture

User Input (URLs) → Load Articles → Text Splitting → Embeddings → FAISS Vector Store → User Question → Answer with Sources

## 🛠️ Tech Stack

- Frontend: Streamlit
- LLM: OpenAI GPT (LangChain)
- Embeddings: OpenAIEmbeddings
- Vector Store: FAISS
- Document Processing: UnstructuredURLLoader
- Text Splitting: RecursiveCharacterTextSplitter

## 📋 Prerequisites

- Python 3.11 or higher
- OpenAI API key

## 🚀 Installation

1. Clone the repository
2. Create virtual environment
3. Install dependencies: pip install -r requirements.txt
4. Create .env file with OPENAI_API_KEY=your_key

## 💻 Usage

Run the application: streamlit run main.py

## How to use

1. Enter up to 3 news article URLs in the sidebar
2. Click "Process URLs" to load and index the articles
3. Enter your question in the text input field
4. View the answer with source references

## Example Questions

- What are the key points discussed in these articles?
- Summarize the main findings
- What do the articles say about [specific topic]?
- Compare the perspectives from different sources
- What are the latest updates mentioned?
- Who are the key people or organizations discussed?
- What are the potential implications or outcomes?
- How do these articles relate to each other?

## 📁 Project Structure

news-research-tool/
├── main.py
├── requirements.txt
├── .env
├── .gitignore
├── README.md
└── faiss_index/

## ⚙️ Configuration

Parameters adjustable in main.py:
- chunk_size: 1000
- temperature: 0.9
- max_tokens: 500

## 🐛 Troubleshooting

ImportError: unstructured package not found
Solution: pip install unstructured

ImportError: faiss package not found
Solution: pip install faiss-cpu

OpenAI API key error
Solution: Ensure .env file contains valid API key

No vector store found
Solution: Process URLs before asking questions

## 🔒 Security Notes

- Never commit .env file or API keys
- .gitignore excludes sensitive files
- Use environment variables for configuration

## 📝 License

MIT License