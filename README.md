# fastest-rag-groq-milvus-bq

![Python](https://img.shields.io/badge/python-3.10%2B-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-app-orange)
![Milvus](https://img.shields.io/badge/Milvus-vector%20DB-green)
![Groq](https://img.shields.io/badge/Groq-LLM-red)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

🚀 **Fastest RAG Stack powered by Milvus and Groq**

This project is a Streamlit web app for fast Retrieval-Augmented Generation (RAG) using Milvus vector database and Groq LLMs. Upload a PDF, index it with binary quantized embeddings, and chat with your document using blazing-fast retrieval and inference.

## Features

- Upload and preview PDF documents
- Extract text and generate embeddings using HuggingFace models
- Binary quantization for efficient vector storage and search
- Store and search embeddings in Milvus vector DB (Lite)
- Retrieval-augmented chat powered by Groq LLMs
- Fast, streaming responses
- Session-based document management

## Getting Started

### Prerequisites

- Python 3.10+
- [Groq API key](https://console.groq.com/)
- [Milvus Lite](https://milvus.io/docs/v2.3.x/install_standalone-docker.md) (handled automatically)

### Step-by-Step Setup

#### 1. Install uv

**MacOS/Linux**
```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows**
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### 2. Create a uv project

```sh
uv init fastest-rag
cd fastest-rag
```

#### 3. Create a virtual environment and activate it

```sh
uv venv

# MacOS/Linux
source .venv/bin/activate

# Windows
.venv\Scripts\activate
```

#### 4. Install dependencies

```sh
uv add pymilvus llama-index llama-index-embeddings-huggingface llama-index-llms-groq streamlit beam-client
```

#### 5. Setup Groq

Get an API key from [Groq](https://console.groq.com/) and set it in the `.env` file as follows:

```
GROQ_API_KEY=<YOUR_GROQ_API_KEY>
```

#### 6. Setup Beam

Go to [Beam Cloud](https://www.beam.cloud/) and get started.  
Your default token will be generated automatically.

#### 7. Deploy the app on Beam cloud

```sh
python start_server.py
```
Copy and paste the token from beam.cloud when prompted.

#### 8. Run the app locally (optional)

Or you can also run the app locally by running the following command:

```sh
streamlit run app.py
```

## File Structure

- `app.py`: Main Streamlit app
- `rag.py`: RAG logic, embedding, vector DB, retrieval, and LLM integration
- `main.py`: Simple CLI entrypoint
- `start_server.py`: Beam Cloud deployment script

## License

MIT © Caleb Chandrasekar

## Acknowledgements

- [Milvus](https://milvus.io/)
- [Groq](https://groq.com/)
- [LlamaIndex](https://llamaindex.ai/)
- [Streamlit](https://streamlit.io/)