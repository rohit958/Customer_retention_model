# Customer_retention_model
This repository contains a full-scale implementation of a Retrieval-Augmented Generation (RAG) system developed within the Databricks Lakehouse. It transforms raw customer transactional and behavioral data into a searchable vector database, enabling Large Language Models (LLMs) to provide context-aware responses regarding customer churn, regional trends, and usage patterns.

Key Features:

Data Engineering: Automated ETL from CSV to Delta Tables using PySpark.

Vector Search: High-performance similarity search using FAISS and sentence-transformers (all-MiniLM-L6-v2).

LLM Integration: Seamless connection to Mistral AI via the latest Python SDK (v1.x) for context-driven inference.

Optimized Retrieval: Custom logic to flatten structured data into semantic strings for improved embedding accuracy.
