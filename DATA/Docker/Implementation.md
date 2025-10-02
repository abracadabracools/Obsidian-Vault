## 🗂️ DOCKER COMPOSE DATA INGESTION CHECKLIST

**Goal:** Bring up PostgreSQL & pgAdmin with Docker Compose, then ingest data from a CSV using a Python ingestion script (in a container).

---

### 🥇 1. 📁 **Project Setup (Folder Structure)**

Create a clean project directory:


---

### 🥈 2. 🐳 **Write Docker Compose File**

Create `docker-compose.yml`:


---

### 🥉 3. ▶️ **Start Containers**

Start the services:

`docker-compose up -d`


---

### 🪄 4. 📜 **Create Ingestion Script (`ingest_data.py`)**


---

### 🏗️ 5. 🐍 **Dockerize the Ingestion Script**

Create a Dockerfile (optional but recommended):

Then build the image:

`docker build -t ingest_data:v01 .`

---

### 🏁 6. 🚀 **Run the Ingestion Container**

Run the ingestion script inside Docker, attached to the same network:

---

### 📊 7. ✅ **Final Verification**
