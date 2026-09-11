# 32-Advance-Research-agent

App Streamlit pour uploader un article de recherche (PDF), OCRisé en markdown via Mistral, indexé dans une base de connaissances PgVector (embeddings locaux sentence-transformers), résumé automatiquement, puis interrogeable via un agent Q&A qui répond d'abord depuis la base de connaissances (en citant les passages sources exacts) et bascule vers Semantic Scholar / DuckDuckGo si insuffisant.

## Tech stack

streamlit, agno (Agent, Groq, ReasoningTools, DuckDuckGoTools, Knowledge/PgVector, SentenceTransformerEmbedder), mistralai (OCR), python-dotenv

## Lancer le projet

```bash
pip install -r requirements.txt
```

Nécessite une instance Postgres/PgVector en cours d'exécution. Créer un `.env` avec `MISTRAL_API_KEY=...` et `GROQ_API_KEY=...`

```bash
streamlit run research_assistant_agent.py
```
