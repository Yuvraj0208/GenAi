# Assignment 1 - News Article Analysis and Job Postings Analysis

LangChain notebook that uses an LLM on Groq to
- Part 1: classify the topic, summarize and pull out key entities for the first 30 BBC news articles
- Part 2: classify the domain and extract skills / education / experience for the first 25 job postings

## Files
- `Generative AI - Assignment 1.ipynb` - the full notebook with outputs
- `bbc-news-data.csv` - BBC news dataset (2225 articles, tab separated)
- `job_title_des.csv` - job postings dataset (2277 postings)
- `part1_news_results.csv` / `part2_jobs_results.csv` - the final dataframes saved from the notebook
- `requirements.txt` - python packages
- `.env.example` - copy to `.env` and add your Groq key

## How to run
1. `pip install -r requirements.txt` (Python 3.12)
2. Create `.env` with `GROQ_API_KEY=...`
3. Open the notebook and run all cells. Both loops together take around 10 minutes because of the Groq free tier rate limits.

## Model used
- `openai/gpt-oss-120b` through Groq (temperature 0)
