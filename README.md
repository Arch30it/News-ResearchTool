# News Research Tool 📈

This application serves as a robust tool for semantic analysis of news articles by allowing users to input URLs that direct to specific content. Leveraging OpenAI's language models, the application processes and analyzes the retrieved text to enable insightful exploration and question-answering on the subject matter. It employs FAISS (Facebook AI Similarity Search) to convert text data into high-dimensional embeddings, which are then stored and indexed for optimized similarity search and retrieval. By utilizing FAISS’s vector search capabilities, this tool supports rapid and scalable access to relevant information, significantly enhancing the speed and accuracy of content retrieval.

## Features
- **URL Processing**: Accepts up to three URLs of news articles for analysis.
- **Data Embedding & Storage**: Processes and stores article data in a FAISS vector index for efficient retrieval.
- **Question-Answering**: Uses a language model to answer user queries based on the content from the provided URLs.
- **Streamlit Interface**: Provides an intuitive user interface for URL input and results display.

## Prerequisites
- Python 3.7 or later
- OpenAI API Key (stored in a `.env` file)

## Set Up Environment Variables: 
Create a .env file in the root directory and add your OpenAI API key:
```bash
OPENAI_API_KEY=your_openai_api_key
```

## Usage
Run the Application: 

1. Start the Streamlit application:

```bash
streamlit run app.py
```
2. Enter URLs:

In the sidebar, enter up to three URLs of news articles you want to analyze.

Click the "Process URLs" button to fetch and embed the content.

Ask Questions: After processing, enter any question related to the articles in the input box. The application will retrieve relevant sections from the articles and provide an answer based on the content.

## Code Structure
1. app.py: Main application file containing the Streamlit interface, URL processing, embedding, and question-answering functionality.
2. FAISS Integration: Uses FAISS for efficient vector storage and retrieval.
3. LangChain: Implements a question-answering model that uses LangChain’s RetrievalQAWithSourcesChain for retrieving relevant content with source information.

## Technologies Used
1. LangChain: Simplifies interaction with OpenAI's API for language processing and embedding.
2. FAISS: Allows fast storage and retrieval of vector embeddings.
3. Streamlit: Provides an interactive web-based user interface.

## Example Workflow
1. Input up to three URLs of news articles in the Streamlit sidebar.
2. Press "Process URLs" to load and embed article content.
3. Ask questions related to the articles in the main area, and receive concise, source-backed responses.
