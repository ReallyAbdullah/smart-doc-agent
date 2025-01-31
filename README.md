# SmartDoc: Agentic AI-Powered Document Intelligence Platform

## Overview

**SmartDoc** is an advanced document intelligence platform that leverages multiple agentic AI strategies using **Autogen**, integrates open-source LLMs via **Ollama**, and incorporates a **Retrieval-Augmented Generation (RAG)** implementation with a **Streamlit frontend**. The goal of this project is to showcase how combining agentic workflows, RAG, and open-source models can deliver enhanced features and performance over vanilla RAG systems.

## Key Features

1. **Multi-Agent Collaboration (Autogen):**
   - **Document Preprocessing Agent**: Extracts, cleans, and splits documents into chunks for indexing.
   - **RAG Query Agent**: Retrieves relevant information and generates responses using RAG.
   - **Reasoning Agent**: Performs multi-step reasoning for complex queries.
   - **Task Automation Agent**: Automates tasks like generating summaries and follow-up emails.
   - **Feedback Loop Agent**: Collects user feedback to improve the system.

2. **Open-Source LLM Integration (Ollama):**
   - Utilizes open-source LLMs like **Llama 2**, **Mistral**, or **Falcon** via **Ollama**.
   - Supports easy deployment and scaling of models locally or in the cloud.

3. **Enhanced RAG Implementation:**
   - Uses **ChromaDB** or **FAISS** for efficient vector storage and retrieval.
   - Combines semantic search with keyword-based search for improved accuracy.
   - Implements contextual re-ranking and dynamic context management.

4. **Streamlit Frontend:**
   - Provides a user-friendly interface for uploading documents, asking questions, and viewing responses.
   - Includes advanced options for summarization, report generation, and task automation.
   - Incorporates a feedback mechanism to continuously improve the system.

5. **Enhanced Performance Over Vanilla RAG:**
   - Multi-agent orchestration for handling complex tasks.
   - Task-specific agents for specialized functions.
   - Dynamic context management for balanced speed and accuracy.
   - Continuous learning through user feedback.

## Workflow Example

1. **User Uploads a Document:**
   - The user uploads a technical report in PDF format.
   - The **Document Preprocessing Agent** extracts text, cleans it, and splits it into chunks.
   - The chunks are embedded and stored in a vector database.

2. **User Asks a Question:**
   - The user types a question: "What are the key findings of the report?"
   - The **RAG Query Agent** retrieves relevant chunks and generates a response.

3. **Advanced Task Automation:**
   - The user selects the "Generate Follow-Up Email" option.
   - The **Task Automation Agent** drafts a professional email summarizing the findings.

4. **Feedback Collection:**
   - The user rates the quality of the response.
   - The **Feedback Loop Agent** collects feedback to improve future responses.

## Technical Stack

- **Backend:**
  - **Autogen**: For orchestrating multiple agents and managing complex workflows.
  - **Ollama**: For deploying and running open-source LLMs.
  - **LangChain**: For building the RAG pipeline and integrating with the vector database.
  - **ChromaDB/FAISS**: For storing and retrieving document embeddings.
  - **Python**: For implementing the backend logic.

- **Frontend:**
  - **Streamlit**: For building the user interface.
  - **HTML/CSS**: For customizing the appearance of the Streamlit app.

- **LLMs:**
  - **Llama 2**, **Mistral**, or **Falcon**: Open-source models deployed via Ollama.

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Ollama server running and accessible at `http://localhost:11434`

### Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/smartdoc.git
   cd smartdoc
   ```

2. **Set Up Virtual Environment:**

   ```bash
   python -m venv smartdoc-env
   source smartdoc-env/bin/activate  # On Windows use `smartdoc-env\Scripts\activate`
   ```

3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

### Configuration

1. **Edit Configuration File (`config/config.yaml`):**

   ```yaml
   ollama:
     base_url: "http://localhost:11434"
     model: "llama2"

   chromadb:
     persist_directory: "./chroma_db"

   llm:
     embedding_model: "all-MiniLM-L6-v2"

   templates:
     reasoning: |
       Context:\n{context}\n\nQuestion: {question}\n\nPerform multi-step reasoning to answer the question.
     summary: |
       Context:\n{context}\n\nGenerate a concise summary of the document.
     email: |
       Summary:\n{summary}\n\nDraft a professional follow-up email based on the summary.
   ```

### Running the Application

1. **Start Ollama Server:**

   Ensure your Ollama server is running and accessible at `http://localhost:11434`.

2. **Run the Streamlit App:**

   ```bash
   streamlit run app.py
   ```

3. **Access the Application:**

   Open your web browser and go to `http://localhost:8501` to interact with SmartDoc.

## Usage

### Uploading Documents

- Click on the "Upload a document" button and select a PDF or text file.
- The document will be processed and stored in the vector database.

### Asking Questions

- Type a question in the "Ask a question about the document" box.
- Click "Submit" to get a response.

### Advanced Options

- Select "Summarize" to generate a concise summary of the document.
- Select "Generate Follow-Up Email" to draft a professional email based on the summary.

### Providing Feedback

- Rate the quality of the response using the slider.
- Click "Submit Feedback" to help improve the system.

## Contributing

Contributions are welcome! Please follow these steps to contribute to the project:

1. **Fork the Repository:**

   ```bash
   git fork https://github.com/yourusername/smartdoc.git
   ```

2. **Create a New Branch:**

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make Your Changes:**

   - Implement new features or fix bugs.
   - Ensure your code adheres to the project's coding standards.

4. **Commit Your Changes:**

   ```bash
   git add .
   git commit -m "Add your commit message"
   ```

5. **Push to Your Fork:**

   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create a Pull Request:**

   - Go to the original repository on GitHub.
   - Click on "New Pull Request".
   - Fill in the details and submit your pull request.

## Contact

- **Project Owner:** [Muhammad Abdullah]
- **Email:** [abdullahfast95@gmail.com]
- **GitHub:** [https://github.com/ReallyAbdullah](https://github.com/ReallyAbdullah)

---
