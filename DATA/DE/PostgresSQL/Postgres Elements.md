 
##🧱 [[PostgresSQL]] Core Concepts (With Examples)

### 1. 📁 **Database**

- A _database_ is the top-level container where all your data lives.
    
- You can have multiple databases inside one Postgres instance.
    

`CREATE DATABASE ny_taxi;`

---

### 2. 📂 **Schema**

- A _schema_ is like a folder inside a database.
    
- It helps organize tables and other objects logically.
    

`CREATE SCHEMA raw_data;`

---

### 3. 📊 **Tables**

- Tables are the core data structures — they store rows and columns (like Excel sheets).
    

`CREATE TABLE trips (     trip_id SERIAL PRIMARY KEY,     pickup_datetime TIMESTAMP,     dropoff_datetime TIMESTAMP,     passenger_count INT,     total_amount FLOAT );`

---

### 4. 📈 **Rows & Columns**

- A **row** = one record
    
- A **column** = one field (attribute) of that record
    

Example row in `trips` table:

|trip_id|pickup_datetime|dropoff_datetime|passenger_count|total_amount|
|---|---|---|---|---|
|1|2021-01-01 08:15:00|2021-01-01 08:35:00|2|23.50|

---

### 5. 🔍 **Queries (SQL)**

Postgres uses **SQL (Structured Query Language)** to interact with data.

Examples:

- **Insert data:**
    

`INSERT INTO trips (pickup_datetime, dropoff_datetime, passenger_count, total_amount) VALUES ('2021-01-01 08:15:00', '2021-01-01 08:35:00', 2, 23.50);`

- **Query data:**
    

`SELECT passenger_count, AVG(total_amount) FROM trips GROUP BY passenger_count;`

- **Filter data:**
    

`SELECT * FROM trips WHERE total_amount > 20;`


Next - [[Usage and Concepts]]
