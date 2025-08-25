# 🔐 Secrets API Project

This project demonstrates how to fetch a **random secret** from a custom API using **Express.js**, **Axios**, and **EJS**.  
A username, secret is fetched from the API & displayed dynamically in the UI.

---

## 🚀 Tech Stack
- **Express.js** – Backend server
- **Axios** – API requests
- **EJS** – Templating engine for UI rendering

---

## ⚙️ Steps to Run the Project

1. **Download / Clone the Project**
   ```bash
   git clone https://github.com/Bhuvanyu02/Secrets-Project.git
   cd Secrets-Project
   ```
   
2. **Install Dependencies**
  ```bash
    npm i
  ```

3. **Run the Server**
  ```bash
  node index.js
  ```

4. **Open your browser and visit:**
  ```bash
  http://localhost:3000
  ```
---
## 📌 Features
  
  1. Fetches a random secret from API
  2. Displays result on EJS-rendered UI
  3. Simple and lightweight setup

---
## 📂 Project Structure

  ├── views/          # EJS templates
  ├── public/         # Static assets (CSS, JS)  
  ├── index.js        # Main server file
  ├── package.json
  └── README.md

---

## 🧩 Sample Code

Here’s the core route that fetches a secret and renders it with EJS:

```js
app.get('/', async (req, res) => {
    try {
        const result = await axios.get("https://secrets-api.appbrewery.com/random");
        res.render("index.ejs", {
            secret: result.data.secret,
            user: result.data.username
        });
    } catch (error) {
        console.log(error);
        res.status(500).send("Something went wrong!");
    }
});
```
---

## 🎯 Example
When you open the app in your browser, it fetches a random secret and shows both the secret text and the username neatly in the UI.

---

## 📸 Screenshots
<img width="1900" height="948" alt="image" src="https://github.com/user-attachments/assets/ad4ae40f-74fd-46e0-8aef-b541081bceef" />

- After hovering on the image

<img width="1899" height="948" alt="image" src="https://github.com/user-attachments/assets/77beba32-112a-4b8d-8062-03ff4e9bce65" />
