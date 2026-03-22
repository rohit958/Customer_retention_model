Project: Customer churn indicator
Author: Rohit Kushwaha


Description:
"This notebook showcases an end-to-end workflow for integrating an LLM (Mistral) into a vector database-based retrieval and augmentation pipeline, using customer dataset records. The process begins by loading a CSV dataset as a Spark DataFrame, converting each row into a text string for embedding. Sentence Transformers are used to generate vector embeddings for these text representations, which are then indexed in FAISS for efficient similarity search.

When a query is made (e.g., "Which customer from Pune has a high churn score?"), the notebook encodes the question, retrieves the top-k most similar text rows, and passes them as context to the Mistral LLM via its API. The LLM is instructed to answer strictly based on the provided context. Outputs from multiple queries are collected, stored, and appended to a Delta table for persistent results."



Components:
  dataset: CSV
  Database: Databricks (source)- data stored in deltastore as condidering Gold Layer-(already cleaned data).
  Embedding and Tokenizing tool: Hugging face withh sentence-transformer
  LLM Model: mistralai (1.2.0-version)
  Vector Search - faiss-cpu(library) 
  
