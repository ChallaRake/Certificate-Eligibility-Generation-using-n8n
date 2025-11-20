# 📜 Certificate Eligibility Generation using n8n  
Automated Workflow for Performance Evaluation & Certificate Distribution

---

## 📌 Overview  
This project automates the entire certificate eligibility process for students using **n8n**, a workflow automation tool. It integrates **Google Sheets** for real-time student response data and **Gmail** for automated email notifications.

Whenever new performance data is submitted in the Google Sheet, the workflow evaluates the student's marks, task completions, and project status, then decides whether they are eligible for a **Gold**, **Silver**, **Bronze**, or **No Certificate**. Personalized emails are sent immediately based on the calculated result.

This end-to-end automation reduces manual evaluation effort, ensures timely communication, and maintains consistent certificate rules.

---

## 🖼️ Workflow Diagram

```
Google Sheets Trigger
         │
         ├── Gold Certificate Check ───> Eligible Gold Email
         │                                Not Eligible Email
         │
         ├── Silver Certificate Check ─> Eligible Silver Email
         │                                Not Eligible Email
         │
         └── Bronze Certificate Check ─> Eligible Bronze Email
                                          Not Eligible Email
```

---

## 🚀 Key Features  
- **Real-Time Google Sheets Integration**  
- **Multi-Level Eligibility Logic (Gold, Silver, Bronze)**  
- **Automated Gmail Notifications**  
- **Dynamic Email Personalization (Name, Email ID, Marks)**  
- **Fully No-Code Using n8n**  
- **Scalable Workflow for Institutions, Bootcamps, Training Programs**  

---

## 🧩 Workflow Components in Detail  

### 1️⃣ Google Sheets Trigger  
The workflow begins with the **Get row(s) from sheets** node.  
It watches a Google Sheet and automatically processes every newly added student response.

Each student row includes:
- Monthly Assessment Marks  
- Total Tasks Completed  
- Total Assignments Completed  
- Quiz Marks  
- Project Presentation Status  
- Email Address  

The data is passed into the three certificate evaluation branches simultaneously.

---

### 2️⃣ Gold Certificate Logic (🥇 Highest Tier)

A student receives a **Gold Certificate** if *all* conditions below are true:

| Criteria | Requirement |
|----------|-------------|
| Monthly Assessment Marks | > 80 |
| Total Tasks Completed | = 10 |
| Total Assignments Completed | = 10 |
| Quiz Marks | > 80 |
| Project Presentation | Yes |

Actions:
- **TRUE → Sends Gold Certificate Email**  
- **FALSE → Sends Not Eligible Email**

---

### 3️⃣ Silver Certificate Logic (🥈 Intermediate Tier)

Eligibility rules:

| Criteria | Requirement |
|----------|-------------|
| Monthly Assessment Marks | 60–80 |
| Total Tasks Completed | = 10 |
| Total Assignments Completed | = 10 |
| Quiz Marks | 60–80 |
| Project Presentation | Yes |

Actions:
- **TRUE → Sends Silver Certificate Email**  
- **FALSE → Sends Not Eligible1 Email**

---

### 4️⃣ Bronze Certificate Logic (🥉 Basic Tier)

Eligibility rules:

| Criteria | Requirement |
|----------|-------------|
| Monthly Assessment Marks | 40–60 |
| Total Tasks Completed | = 10 |
| Total Assignments Completed | = 10 |
| Quiz Marks | 40–60 |
| Project Presentation | Yes |

Actions:
- **TRUE → Sends Bronze Certificate Email**  
- **FALSE → Sends Not Eligible2 Email**

---

## ✉️ Automated Email Notifications  

Each output uses a Gmail node to send personalized messages:

### 🥇 Gold Certificate Email  
- Congratulates the student  
- Highlights excellent performance  

### 🥈 Silver Certificate Email  
- Appreciates good performance  
- Motivates aiming for Gold  

### 🥉 Bronze Certificate Email  
- Recognizes effort  
- Encourages further improvement  

### ❌ Not Eligible Email  
- Provides guidance for improvement  
- Encourages continuing participation  

---

## ⚙️ Tools & Technologies Used  

| Technology | Purpose |
|-----------|----------|
| **n8n** | Automation workflow builder |
| **Google Sheets Trigger** | Reads student responses |
| **IF Logic Nodes** | Evaluates eligibility conditions |
| **Gmail Node** | Sends email notifications |
| **Google Sheets** | Stores performance data |

---

## 🔍 Use Cases  
- Academic institutions and universities  
- Internship assessment programs  
- Skill-based training cohorts  
- Bootcamps and workshops  
- Corporate certification programs  

The system can be extended to:
- Generate downloadable certificates (PDF)  
- Send WhatsApp/Slack notifications  
- Create analytics dashboards  
- Route approvals through faculty/admin  

---

## 🧠 Learning Outcomes  
By building this project, you gain experience in:
- Structuring conditional logic for automation  
- Designing multi-branch workflows in n8n  
- Integrating Google Sheets & Gmail APIs  
- Sending real-time personalized notifications  
- Automating certification tasks  
- Scaling a workflow for large student batches  


---

## 📹 Demo Video

👉 **Watch the full workflow demo here:**  
*(Add your video link, YouTube URL, or MP4 file path below)*
<img width="1061" height="753" alt="Screenshot 2025-11-20 154355" src="https://github.com/user-attachments/assets/5a2e2533-f1a7-40c0-bdf8-957fff9d7efc" />

---

## 📜 License  
This project is intended for educational and automation demonstration purposes.  
Feel free to expand and adapt it as needed.

