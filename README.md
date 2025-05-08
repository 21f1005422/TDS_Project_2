# 🤖 LLM-Powered Assignment Answering API

## 📘 Background

As a student of the **IIT Madras Online B.Sc. in Data Science and Applications**, you've enrolled in the **Tools in Data Science** course. To make your academic life more efficient, this project introduces a **Large Language Model (LLM)-based solution** that automatically answers questions from your graded assignments.

---

## 🎯 Project Objective

Build and deploy an API that accepts a question from one of the following five graded assignments and returns the answer that can be directly entered into the assignment:

- Graded Assignment 1  
- Graded Assignment 2  
- Graded Assignment 3  
- Graded Assignment 4  
- Graded Assignment 5  

---

## 🌐 API Overview

Your application exposes an API endpoint to receive questions and (optionally) file attachments, and returns the corresponding answer.

### 📍 Endpoint

POST https://your-app.vercel.app/api/

markdown
Copy
Edit

### 🔧 Request Format

- **Method**: `POST`
- **Content-Type**: `multipart/form-data`
- **Fields**:
  - `question` (required): The assignment question text.
  - `file` (optional): Any attachment necessary to answer the question (e.g., a `.zip` or `.csv` file).

### 🧪 Example `curl` Request

```bash
curl -X POST "https://your-app.vercel.app/api/" \
  -H "Content-Type: multipart/form-data" \
  -F "question=Download and unzip file abcd.zip which has a single extract.csv file inside. What is the value in the 'answer' column of the CSV file?" \
  -F "file=@abcd.zip"
📤 Expected Response
A JSON object containing the answer:

json
Copy
Edit
{
  "answer": "1234567890"
}
🚀 Deployment Instructions
Deploy your application using a platform like:

Vercel

Render

Railway

If using ngrok, ensure the tunnel stays active for evaluation.

📂 Project Setup & Sharing
Create a public GitHub repository for your project.

Add an MIT LICENSE file.

Commit and push all code to the repository.
