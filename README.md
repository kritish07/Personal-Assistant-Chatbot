# Personal Assistant Chatbot

### Introduction
The Personal Assistant Chatbot project is designed to provide a quick and efficient way to learn about a person's professional background by answering questions based on their resume. The system leverages advanced AI technologies to parse, understand, and respond to inquiries about the content of a resume.

### Prerequisites
To use this project, you will need: An OpenAI API key.

### Goal
The goal of this project is to create an easy and efficient way for anyone to learn about skills, experience, and other professional details from a resume without having to read through the entire document.

### Dependencies
The following Python packages are required for this project:

- **langchain:** A framework for building applications with large language models.
- **openai:** OpenAI's API for interacting with GPT models.
- **PyPDF2:** A library for working with PDF files.
- **faiss-cpu:** Facebook AI Similarity Search library for efficient similarity search.
- **tiktoken:** A library for handling tokenization with OpenAI models.
- **langchain-openai:** Integration between LangChain and OpenAI.
- **langchain_community:** Additional community-contributed components for LangChain.

### Benefits
- **Save Time:** Quickly get the information you need without searching through pages of text.
- **Easy Access:** Ask questions in plain language, just like conversing with a friend.

### How It Works
#### Key Components
- **TextLoader:** Extracts text from the resume.
- **RecursiveCharacterTextSplitter:** Breaks down large chunks of text into manageable pieces.
- **OpenAI Embeddings:** Converts text into embeddings that capture the essence of the sentences.
- **FAISS:** Acts as a search engine to find relevant parts of the resume based on the question.
- **RetrievalQA Chain:** Uses the retrieved resume sections to answer the user's questions.

#### Process
1. **Load the Resume:** The TextLoader extracts text from the provided resume document.
2. **Text Splitting:** The RecursiveCharacterTextSplitter divides the text into chunks of 800 characters with an overlap of 100 characters to ensure context continuity.
3. **Embedding Creation:** OpenAI's embedding model converts these text chunks into vector embeddings.
4. **FAISS Indexing:** The embeddings are stored in a FAISS index to enable fast and efficient search.
5. **Question Answering:** The RetrievalQA chain takes the user’s question, retrieves relevant text chunks from the FAISS index, and generates a response.

### Room for Improvement
- **Pre-trained Models:** Explore using different pre-trained models from OpenAI to potentially improve understanding of the resume content.
- **File Formats:** Expand the system to handle other file formats beyond text documents, such as PDFs or Word documents.

### Conclusion
The Personal Assistant Chatbot project showcases the power of AI in creating a user-friendly way to access information. By leveraging LangChain libraries, the project successfully builds a functional Q&A system for a professional profile. With further development and customization, this approach can be adapted to various scenarios where easy access to information is essential.

### Contributing
Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue.

### License
This project is licensed under a custom license: LICENSE that restricts commercial use, distribution, patent or trademark use of the code. You are free to use the code for private, non-commercial purposes only.

### Acknowledgements
Special thanks to the developers of LangChain, OpenAI, and FAISS for their powerful tools and libraries.
