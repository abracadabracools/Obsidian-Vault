- [[Workflow]]

📁 Local Host (Disk)
│
├── Source Code: ingest_data.py, Dockerfile
├── Volume: ./ny_taxi_postgres_data/ (DB storage)
│
▼
🐳 Docker Engine
│
├── 🐍 Ingestion Container (Python Script)
│     - Runs ETL code
│     - Reads CSV
│     - Sends data to DB
│
├── 🐘 Postgres Container (Database)
│     - Receives data
│     - Writes to volume (persistent storage)
│
└── 🖥️ pgAdmin Container (GUI)
      - Connects to Postgres
      - Queries & displays data
