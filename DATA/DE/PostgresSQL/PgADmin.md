
## 📊 What pgAdmin 4 Is

- **pgAdmin 4** is the **official GUI client for PostgreSQL**.
    
- It runs as a **web application** — usually accessible at `http://localhost:8080`.
    
- You can:
    
    - 🗃️ Explore databases visually
        
    - ✍️ Run SQL queries
        
    - 🧰 Create tables, users, schemas
        
    - 📈 Manage your PostgreSQL server
        

---

## 🐳 Running pgAdmin 4 with Docker

The standard way to run it:

`docker run -it \   -e PGADMIN_DEFAULT_EMAIL=admin@admin.com \   -e PGADMIN_DEFAULT_PASSWORD=admin \   -p 8080:80 \   dpage/pgadmin4`

✅ Explanation:

|Flag|Purpose|
|---|---|
|`-e PGADMIN_DEFAULT_EMAIL`|Default login email|
|`-e PGADMIN_DEFAULT_PASSWORD`|Default login password|
|`-p 8080:80`|Expose container port 80 → localhost port 8080|
|`dpage/pgadmin4`|The official pgAdmin image|

Then visit:  
👉 [http://localhost:8080](http://localhost:8080)  
and log in with the email/password you set.

Next - [[Final run Checklist with Docker compose]]
