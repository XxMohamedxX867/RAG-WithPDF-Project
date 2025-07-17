# 📄 PDF RAG Chatbot

A powerful Retrieval-Augmented Generation (RAG) chatbot built with Streamlit that allows you to upload PDF documents and have intelligent conversations about their content using Google's Gemini AI.

## 🚀 Features

- **PDF Document Processing**: Upload and process PDF files with automatic text extraction
- **Intelligent Text Chunking**: Smart document splitting with configurable chunk sizes and overlap
- **Vector Database**: ChromaDB integration for efficient document storage and retrieval
- **Google Gemini AI Integration**: Powered by Google's latest Gemini 2.5 Flash model
- **Interactive Chat Interface**: User-friendly Streamlit interface with chat history
- **Real-time Responses**: Get instant answers based on your PDF content
- **Secure API Key Management**: Secure handling of Google API credentials

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **AI/ML**: Google Gemini AI (Gemini 2.5 Flash)
- **Vector Database**: ChromaDB
- **Document Processing**: PyMuPDF
- **Framework**: LangChain
- **Embeddings**: Google Generative AI Embeddings

## 📋 Prerequisites

Before running this project, make sure you have:

- Python 3.8 or higher
- A Google AI API key (Gemini API)
- Internet connection for API calls

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/pdf-rag-chatbot.git
   cd pdf-rag-chatbot
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv env_rag
   ```

3. **Activate the virtual environment**
   
   **Windows:**
   ```bash
   env_rag\Scripts\activate
   ```
   
   **macOS/Linux:**
   ```bash
   source env_rag/bin/activate
   ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 🔑 Setup

1. **Get Google AI API Key**
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Create a new API key
   - Copy the API key for use in the application

2. **Run the application**
   ```bash
   streamlit run src/app.py
   ```

3. **Access the application**
   - Open your browser and go to `http://localhost:8501`
   - Enter your Google API key in the sidebar
   - Upload a PDF document
   - Start chatting!

## 📖 Usage

1. **Upload a PDF**: Use the file uploader to select your PDF document
2. **Enter API Key**: Provide your Google AI API key in the sidebar
3. **Ask Questions**: Type questions about the content of your PDF
4. **Get Answers**: Receive intelligent responses based on the document content

### Example Questions You Can Ask:
- "What are the main topics discussed in this document?"
- "Summarize the key findings"
- "What are the recommendations mentioned?"
- "Who are the main stakeholders?"

## 🏗️ Project Structure

```
RAG Project/
├── data/                          # Data storage
│   └── content.pdf                # Sample PDF document
├── notebooks/                     # Jupyter notebooks
│   └── main.ipynb                # Development and testing notebook
├── src/                          # Source code
│   └── app.py                    # Main Streamlit application
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

## 🔧 Configuration

The application uses the following default configurations:

- **Chunk Size**: 350 characters
- **Chunk Overlap**: 100 characters
- **Embedding Model**: `models/embedding-001`
- **LLM Model**: `models/gemini-2.5-flash`
- **Retrieval**: Top 3 most relevant chunks

You can modify these settings in the `src/app.py` file.

## 📊 How It Works

1. **Document Processing**: PDF files are loaded and text is extracted using PyMuPDF
2. **Text Chunking**: Documents are split into smaller chunks for better processing
3. **Vectorization**: Text chunks are converted to embeddings using Google's embedding model
4. **Storage**: Embeddings are stored in ChromaDB vector database
5. **Retrieval**: When a question is asked, relevant chunks are retrieved based on similarity
6. **Generation**: The LLM generates answers using the retrieved context and the user's question

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- [Streamlit](https://streamlit.io/) for the amazing web app framework
- [LangChain](https://langchain.com/) for the RAG framework
- [Google AI](https://ai.google/) for the Gemini models
- [ChromaDB](https://www.trychroma.com/) for the vector database

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/pdf-rag-chatbot/issues) page
2. Create a new issue with detailed information
3. Include error messages and steps to reproduce the problem

## 🔮 Future Enhancements

- [ ] Support for multiple file formats (DOCX, TXT, etc.)
- [ ] Batch processing capabilities
- [ ] Custom embedding models
- [ ] Advanced filtering and search options
- [ ] Export chat history
- [ ] Multi-language support
- [ ] User authentication
- [ ] Cloud deployment options

---

⭐ **Star this repository if you find it helpful!** 
