# Assignment 2 - Smart Mutual Fund Advisor (RAG + LangGraph)

Gradio app that suggests a mutual fund portfolio from free text preferences like
"low risk portfolio" or "high return, only Aditya Birla". It uses RAG over the
Kaggle mutual funds dataset with ChromaDB and Groq hosted LLMs, and Part 2 rebuilds
the same pipeline as a LangGraph graph.

## Files
- `Generative AI - Assignment 2.ipynb` - the full notebook with outputs
- `mutual_funds_data.csv` - dataset (35,559 rows, first 1000 are indexed)
- `requirements.txt` - python packages
- `.env.example` - copy to `.env` and add your Groq key

## How to run
1. `pip install -r requirements.txt` (Python 3.12)
2. Install Ollama and run `ollama pull nomic-embed-text`
3. Create `.env` with `GROQ_API_KEY=...`
4. Open the notebook and run all cells. Gradio launches inline at the end of Part 1 and Part 2.

## Models used
- LLMs (via Groq): `openai/gpt-oss-120b`, `qwen/qwen3.8-27b`, `openai/gpt-oss-20b`
- Embeddings (via Ollama): `nomic-embed-text`
- Vector DB: ChromaDB (persisted to `chroma_mutual_funds_db/`)
