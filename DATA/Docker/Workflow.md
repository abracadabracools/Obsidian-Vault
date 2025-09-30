🐳 [[Docker]]


## 🧪 Example Workflow (ETL Pipeline)

1. 🐘 Start Postgres database container
    
    `docker run -d --name pgdb -e POSTGRES_USER=root -e POSTGRES_PASSWORD=root postgres:13`
    
2. 🐍 Build and run ingestion container
    
    `docker build -t ingest:v1 . docker run -it --network=my_net ingest:v1 --db=ny_taxi --url=data.csv`
    
3. 📊 Connect with pgAdmin container
    
    `docker run -d --network=my_net -p 8080:80 dpage/pgadmin4`
    
4. ⚙️ Orchestrate all with Docker Compose
    
    `docker-compose up -d`

Workflow – From Start to End (Line Diagram)

               ┌────────────────────────────────────────────┐
               │              1. Write Code                │
               │    - Python scripts / ingestion script   │
               │    - requirements.txt                    │
               │    - config files                        │
               └────────────────────────────────────────────┘
                                      │
                                      ▼
               ┌────────────────────────────────────────────┐
               │         2. Create Dockerfile              │
               │    - Define base image (e.g. python:3.9)  │
               │    - Install dependencies                │
               │    - Copy code into image               │
               │    - Set ENTRYPOINT/CMD                 │
               └────────────────────────────────────────────┘
                                      │
                                      ▼
               ┌────────────────────────────────────────────┐
               │         3. Build Docker Image             │
               │   $ docker build -t my_app:v1 .          │
               │   - Docker reads Dockerfile              │
               │   - Creates layered image               │
               │   - Stored locally                      │
               └────────────────────────────────────────────┘
                                      │
                                      ▼
               ┌────────────────────────────────────────────┐
               │         4. Run a Container                │
               │   $ docker run -it my_app:v1             │
               │   - Starts container from image          │
               │   - Executes your script/code            │
               │   - Runs isolated environment            │
               └────────────────────────────────────────────┘
                                      │
                                      ▼
               ┌────────────────────────────────────────────┐
               │       5. Use Volumes & Networks           │
               │   - Volumes store persistent data         │
               │   - Networks connect multiple containers  │
               │     (e.g., app ↔ database ↔ pgAdmin)      │
               └────────────────────────────────────────────┘
                                      │
                                      ▼
               ┌────────────────────────────────────────────┐
               │       6. Orchestrate with Compose         │
               │   - Define multi-container setup          │
               │   - $ docker-compose up -d                │
               │   - Runs DB + API + Ingestion + UI        │
               └────────────────────────────────────────────┘
                                      │
                                      ▼
               ┌────────────────────────────────────────────┐
               │          7. Deploy Anywhere               │
               │   - Push image to Docker Hub / registry  │
               │   - Run on cloud (AWS, GCP, etc.)        │
               │   - Integrate with CI/CD pipelines       │
               └────────────────────────────────────────────┘


**Code → Dockerfile → Build Image → Run Container → Add Volumes/Network → Compose Multi-Services → Deploy Anywhere**

---

✅ **Quick Explanation of Each Step:**

| Step | Name                       | What Happens                                             |
| ---- | -------------------------- | -------------------------------------------------------- |
| 1️⃣  | **Write Code**             | Your ETL script, database logic, API, etc.               |
| 2️⃣  | **Create Dockerfile**      | Blueprint: tells Docker how to build the image           |
| 3️⃣  | **Build Image**            | Package everything into a portable image                 |
| 4️⃣  | **Run Container**          | Launch an isolated environment from that image           |
| 5️⃣  | **Use Volumes & Networks** | Persist data + connect services (e.g. Postgres, scripts) |
| 6️⃣  | **Compose Orchestration**  | Manage multi-container setups easily                     |
| 7️⃣  | **Deploy Anywhere**        | Push to cloud or run in production pipelines             |

---
