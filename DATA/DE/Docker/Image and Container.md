 - [[Workflow]]
## 🧠 Why Image Comes Before Container

Because **an image is the blueprint**, and a **container is the running instance built from that blueprint** — just like:

- 🍰 **Image** = cake _recipe_
    
- 📦 **Container** = actual _cake_ made from that recipe
    

You **can’t bake the cake without the recipe first** — the same way you **can’t run a container without an image**.

---

### 📦 Image = Template (Read-Only)

An **image** is a **snapshot of an environment**. It’s a packaged version of:

- OS base (e.g., Debian or Alpine Linux)
    
- Runtime (e.g., Python 3.9)
    
- Dependencies (`pandas`, `sqlalchemy`)
    
- Your code (`ingest_data.py`)
    
- Entry instructions (`ENTRYPOINT`, `CMD`)
    

👉 It’s like a sealed box of everything needed **to run your application** — but it’s _not running yet_.

We create this image once using:

`docker build -t my_app:v1 .`

---

### 🐳 Container = Running Instance (Mutable)

A **container** is a _live, running copy_ of that image.

When you do:

`docker run -it my_app:v1`

Docker says:

1. 🛠️ “Take the image `my_app:v1`”
    
2. 📦 “Create a writable layer on top”
    
3. 🚀 “Run it as a container”
    

Containers are **temporary, isolated environments** that:

- Can be started, stopped, and destroyed easily
    
- Can store runtime data (logs, temporary files)
    
- All start from the same _image base_
    

---

### 🧱 Real-World Analogy

|Concept|Real-World Equivalent|
|---|---|
|🖼️ Image|A recipe card or machine blueprint|
|📦 Container|The actual cake or manufactured machine|
|🏭 Build image|Writing the recipe / blueprint|
|▶️ Run container|Baking the cake / assembling the product|

👉 Just like you **can bake many cakes from the same recipe**, you can run **many containers from the same image**.