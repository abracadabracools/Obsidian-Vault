
[[Workflow]]

🧠 Docker Data Engineering Architecture – Detailed Flow

**📁 Local Host (Your Machine)**

- Stores source code (`ingest_data.py`, `Dockerfile`)
    
- Stores persistent database files (via Docker **volumes**)
    
- Starts Docker containers
    

**🐳 Ingestion Container (Python ETL)**

- Runs your Python script
    
- Downloads CSV from URL
    
- Reads + processes data (with `pandas`)
    
- Connects to Postgres and inserts rows
    

**🐘 Postgres Container (Database)**

- Runs PostgreSQL database server
    
- Receives data from ingestion container
    
- Stores data permanently in a **volume** (on host disk)
    

**📊 Docker Volume**

- Physically stores all database files (tables, indexes, WAL logs)
    
- Lives on your **host machine**, but mounted into Postgres container
    

**🖥️ pgAdmin Container (Client GUI)**

- Connects to Postgres via Docker network
    
- Queries and visualizes the data
    
- Stores only small UI preferences (not actual data)