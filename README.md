# 🗓️ Daily Task Scheduler (AI-Powered)

An AI-powered daily task scheduling application built using **AWS PartyRock** and **Amazon Bedrock**.  
The app transforms an unstructured list of tasks into a **realistic, time-blocked daily schedule**, while also providing **productivity tips** and **overload warnings**.

🔗 **Live Demo**:  
https://partyrock.aws/u/180706484338/k2N-O_zTJ/Daily-Task-Scheduler-(AI-Powered)

---

## 🚀 What This Application Does

- Accepts a list of daily tasks with priorities and estimated effort  
- Understands urgency, importance, and time constraints  
- Generates a clean, realistic daily schedule with breaks  
- Provides productivity tips and focus recommendations  
- Warns users when the schedule is overloaded  

This project demonstrates how **AI applications** can be built using **no-code tools** and **managed foundation models** on AWS.

---

## 🧠 Architecture Overview

The application uses a **serverless, no-code architecture** powered by AWS managed services.

- **PartyRock** handles the user interface and prompt orchestration  
- **Amazon Bedrock** provides foundation model inference  
- No backend servers, databases, or model hosting are required  

All scaling, security, and availability are managed by AWS.

---

## 🏗️ Architecture Flow

1. User enters tasks and available time through PartyRock widgets  
2. Structured inputs are passed as optimized prompts  
3. Amazon Bedrock processes the prompts using foundation models  
4. The AI generates:
   - A prioritized daily schedule
   - Time blocks with breaks
   - Productivity tips and overload warnings  
5. Results are displayed instantly in the browser

---

## 🖼️ Architecture Diagram

![Architecture Diagram](architecture/architecture-diagram.png)

---

## ☁️ Why Amazon Bedrock?

Amazon Bedrock is ideal for this project because it:

- Provides fully managed access to foundation models  
- Eliminates the need for model training or hosting  
- Automatically scales with demand  
- Operates within a secure AWS-managed environment  
- Integrates seamlessly with PartyRock for no-code AI development  

This allows developers to focus on **problem-solving and product design**, not infrastructure.

---

## 🔍 Comparison with Traditional Application Architecture

| Aspect | PartyRock + Bedrock | Traditional App |
|------|---------------------|-----------------|
| Coding | No-code | Frontend + backend code |
| AI Models | Pre-built foundation models | Custom ML models |
| Infrastructure | Fully managed | EC2 / APIs / ML hosting |
| Scalability | Automatic | Manual configuration |
| Time to Build | Minutes | Days or weeks |

---

## ⚠️ Challenges & Limitations

- No persistent user data storage  
- Output quality depends on user-provided task estimates  
- Scheduling logic is prompt-based, not rule-based  

**Mitigations**:
- Structured inputs reduce ambiguity  
- Separate analysis prompts detect overloads  
- Clear UI guidance improves input quality  

---

## 🧰 Tech Stack

- **AWS PartyRock** – No-code AI application builder  
- **Amazon Bedrock** – Foundation model inference  
- **AWS Managed Infrastructure** – Serverless, scalable backend  

---

## 🎯 Key Takeaways

- Demonstrates AI product thinking beyond chat interfaces  
- Shows understanding of modern serverless AI architectures  
- Highlights effective use of AWS managed services  
- Suitable for portfolios, interviews, and demos  

---

## 📌 Author

Built by **Sarvesh Kushwaha**  
GitHub: https://github.com/001skush
