# 🧠 Automated Resume & Cover Letter Generator

This project is an **automation workflow** that generates a **personalized resume and cover letter** for each job listing.

---

## 🚀 Features

### **Automated Resume Crafting**
- Generates an **HTML resume** from your data.  
- Hosts it live on **GitHub Pages**.  
- Converts it to **PDF** using **Gotenberg** and saves it to **Google Drive**.

### **Automated Cover Letter Generation**
- Uses an **LLM** to create a **tailored cover letter** for each job listing.

### **Simple Input Database Agent**
- Stores your experience in an **n8n Data Table** with the following fields:  
  `role`, `summary`, `task`, `skills`, `tools`, `industry`.  
- The main agent pulls this data using **RAG (Retrieval-Augmented Generation)** to personalize the outputs.

### **One-Time GitHub Setup**
- Initializes a **blank GitHub repository** to host HTML files online, allowing **Gotenberg** to access and convert them.

## 🧩 Tech Stack

- **Gotenberg** – Converts HTML to PDF  
- **GitHub Pages** – Hosts live HTML files  
- **n8n** – Handles data tables and workflow automation  
- **LLM (OpenAI / Cohere / etc.)** – Generates cover letters  
- **Google Drive** – Stores the final PDFs  

---

## ⚙️ Installation & Setup

### 1. Create a GitHub Repository
- This repo will host your HTML resume through **GitHub Pages**.

### 2. Set the Webhook URL
- In the `notify-n8n.yml` file, replace:
role | summary | task | skills | tools | industry

### 3. Create the n8n Data Table

Add the following columns:

role | summary | task | skills | tools | industry

### 4. Create a Google Spreadsheet
- Add these columns:  
company | cover_letter | resume

### 5. Customize the HTML Template
- Modify the HTML resume to your liking.  
- You can use an **LLM** to locate and edit specific sections.

### 6. Add Authentication and Link Your GitHub Repo
- Ensure your workflow has permission to **push updates** to your GitHub Pages branch.

### 7. Run the Workflow
- Once everything is connected, trigger the workflow to automatically generate and save **personalized resumes and cover letters**.
