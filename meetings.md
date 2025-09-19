### Week of Sept 19 – Meeting Notes

1. **What has been completed this week?**  
   I completed background reading on two main topics relevant to my project:  
   * **Automated Data Collection:** I reviewed tutorials and articles on building Python-based data ingestion pipelines that use `requests`, `pandas`, and scheduling tools (such as `cron` or Apache Airflow) to automatically download and preprocess large public datasets.  
   * **Vector Databases:** I read introductory material on vector search technologies (e.g., FAISS and Pinecone) to understand how high-dimensional embeddings can be stored and queried efficiently for downstream machine-learning or retrieval tasks.  
   These readings help me plan how the PEMs data could be pulled automatically and later stored for similarity search.

2. **Is there any roadblock?**  
   My main challenge is deciding which specific PEMS data source and API endpoints to start with, since there are multiple versions and formats. I will clarify this with Seerat during our next meeting.

3. **What is the agenda for next week?**  
   * Identify the exact PEMS dataset and API (or file URLs) to target.  
   * Draft a small Python script to download a single day or month of data automatically.  
   * Continue learning how to transform tabular sensor readings into vector embeddings suitable for a vector database.

4. **Are meeting notes/Wiki/GitHub updated?**  
   Yes. This `meetings.md` file and my preliminary notes on data-pipeline approaches and vector databases have been committed and pushed to the repository.
