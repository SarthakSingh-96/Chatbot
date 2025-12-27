# 💬 AI-Powered Document Question-Answering Chatbot

An intelligent chatbot application that allows users to ask questions about their documents (PDFs and images) using natural language. Built with Streamlit, LangChain, and OpenAI's GPT models.

## ✨ Features

- **PDF Question-Answering**: Upload PDF documents and ask questions about their content
- **Image Text Extraction**: Extract and query text from images using OCR (Optical Character Recognition)
- **Intelligent Responses**: Powered by OpenAI's language models for accurate and contextual answers
- **Source Tracking**: View the source documents used to generate answers
- **User-Friendly Interface**: Clean and intuitive Streamlit-based UI
- **Chat History**: Maintains conversation history for better context

## 🚀 Demo

The chatbot provides two main functionalities:
1. **PDF Mode**: Upload a PDF document and ask questions about its content
2. **Image Mode**: Upload an image containing text and ask questions about it

## 🛠️ Technologies Used

- **Streamlit**: Web application framework
- **LangChain**: Framework for building LLM applications
- **OpenAI API**: GPT models for natural language processing
- **FAISS**: Vector similarity search for efficient document retrieval
- **ChromaDB**: Vector database for document embeddings
- **PyPDF2/pypdf**: PDF text extraction
- **Pytesseract**: OCR for image text extraction
- **Streamlit Chat**: Chat interface components

## 📋 Prerequisites

Before running this project, ensure you have:

- Python 3.8 or higher
- OpenAI API key ([Get one here](https://platform.openai.com/api-keys))
- Tesseract OCR installed (for image processing)
- Node.js and npm (for localtunnel deployment)

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/chatbot.git
   cd chatbot
   ```

2. **Install Python dependencies**
   ```bash
   pip install streamlit
   pip install PyPDF2
   pip install langchain
   pip install openai
   pip install tiktoken
   pip install faiss-cpu
   pip install pytesseract
   pip install chromadb
   pip install pypdf
   pip install streamlit_chat
   ```

3. **Install Tesseract OCR**
   - **Windows**: Download from [GitHub](https://github.com/UB-Mannheim/tesseract/wiki)
   - **Linux**: `sudo apt install tesseract-ocr`
   - **macOS**: `brew install tesseract`

4. **Install localtunnel (optional, for public access)**
   ```bash
   npm install -g localtunnel
   ```

## ⚙️ Configuration

1. Set your OpenAI API key as an environment variable:
   ```python
   import os
   os.environ['OPENAI_API_KEY'] = 'your-api-key-here'
   ```

   Or create a `.env` file:
   ```
   OPENAI_API_KEY=your-api-key-here
   ```

## 🚀 Usage

### Running Locally

1. **Start the Streamlit app**
   ```bash
   streamlit run app.py
   ```

2. **Access the application**
   - Open your browser and navigate to `http://localhost:8501`

### Running with Public Access (Localtunnel)

```bash
streamlit run app.py & npx localtunnel --port 8501
```

This will provide a public URL that can be accessed from anywhere.

## 📖 How to Use

### PDF Mode
1. Select "PDF" from the sidebar
2. Upload your PDF document
3. Wait for the document to be processed
4. Type your question in the text input
5. View the answer and source documents

### Image Mode
1. Select "Image" from the sidebar
2. Upload an image file (PNG, JPG, JPEG)
3. The app will extract text using OCR
4. Type your question about the image content
5. Receive answers based on the extracted text

## 📁 Project Structure

```
chatbot/
├── ChatBot_GPT.ipynb    # Jupyter notebook with setup and code
├── app.py               # Main Streamlit application
└── README.md            # Project documentation
```

## 🔒 Security Notes

- **Never commit your API keys** to version control
- Use environment variables or `.env` files for sensitive data
- Add `.env` to your `.gitignore` file

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## ⚠️ Known Limitations

- Large PDF files may take longer to process
- OCR accuracy depends on image quality
- OpenAI API usage incurs costs based on token consumption

## 🐛 Troubleshooting

**Issue**: Tesseract not found
- **Solution**: Ensure Tesseract is installed and added to your system PATH

**Issue**: OpenAI API errors
- **Solution**: Verify your API key is valid and has sufficient credits

**Issue**: Module not found errors
- **Solution**: Reinstall all dependencies using the installation commands

## 📧 Contact

For questions or support, please open an issue on GitHub.

## 🙏 Acknowledgments

- OpenAI for the GPT models
- LangChain for the excellent framework
- Streamlit for the web framework
- All open-source contributors

---

⭐ If you find this project helpful, please consider giving it a star!
