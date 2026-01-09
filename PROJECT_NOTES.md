# 📘 PROJECT_NOTES.md
## Daily Task Scheduler (AI-Powered)

This document captures the **design decisions, trade-offs, and reasoning** behind the *Daily Task Scheduler (AI-Powered)* application.  
It explains *why* the system was designed this way, rather than only describing *what* it does.

---

## 🎯 Project Intent

The goal of this project was to demonstrate **AI-driven workflow design using AWS managed services**, rather than traditional full-stack development.

Key objectives:
- Embed AI into a real productivity use case
- Structure unstructured user input for reliable AI output
- Leverage fully managed AWS services to minimize operational overhead
- Design an application that can evolve into an enterprise-ready system

---

## 🧠 Key Design Decisions

### 1️⃣ No-Code Architecture (AWS PartyRock + Amazon Bedrock)

**Decision**  
The application uses AWS PartyRock for the UI and prompt orchestration, with Amazon Bedrock providing foundation model inference.

**Reasoning**
- Focuses effort on AI behavior and system design
- Removes the need for custom infrastructure and boilerplate code
- Enables rapid development and iteration
- Ensures scalability, availability, and security are handled by AWS

**Trade-offs**
- Limited control over backend logic
- Constrained customization compared to custom-built applications

This was an intentional decision to prioritize **AI reasoning and workflow design**.

---

### 2️⃣ Accepting Unstructured User Input

**Decision**  
Users are allowed to enter tasks as free-form text instead of a rigid schema.

**Reasoning**
- Reflects how users naturally maintain task lists
- Forces the AI to interpret intent, priority, and effort
- Demonstrates real-world AI usage scenarios

**Mitigation**
- Prompt structure enforces task clarity
- UI guidance encourages well-defined inputs

---

### 3️⃣ Prompt-Based Scheduling Logic

**Decision**  
Scheduling logic is implemented using prompt engineering rather than rule-based algorithms.

**Reasoning**
- Supports flexible reasoning over priorities, constraints, and time estimates
- Enables generation of productivity insights alongside schedules
- Avoids rigid logic that may not generalize across users

**Trade-off**
- Output quality depends on input accuracy and prompt design
- Less deterministic than traditional scheduling engines

---

### 4️⃣ Overload Detection via AI Reasoning

**Decision**  
Schedule overload is identified through AI analysis instead of fixed thresholds.

**Reasoning**
- Provides contextual explanations instead of binary errors
- Aligns more closely with human productivity judgment
- Allows suggestions and prioritization guidance

**Constraint**
- Overload detection is dependent on user-provided time estimates

---

## ⚠️ Known Limitations (Version 1)

- No persistent data storage
- No user authentication
- Single-day scheduling only
- No calendar integrations

These limitations were **intentional** to keep the application:
- Free-tier friendly
- Fully serverless
- Focused on AI-driven decision-making

---

## 🛠️ Production Considerations

In a production environment, this application would include:
- Persistent storage using Amazon DynamoDB
- User authentication via Amazon Cognito
- Hybrid scheduling logic (rules + AI reasoning)
- External calendar integrations (Google / Outlook)
- Observability and usage analytics

The AI reasoning layer powered by Amazon Bedrock would remain central to the system.

---

## 📈 Evolution Path (Version 2)

Planned improvements:
- Save daily and weekly schedules
- Track productivity trends
- Support multiple users and teams
- Introduce access control and auditability

The architecture is designed to support these additions without rewriting the core logic.

---

## 🎓 Key Learnings

- Effective AI systems require disciplined input structure
- Prompt design directly impacts output reliability
- Managed services significantly reduce operational complexity
- Designing for future scalability is critical even at MVP stage

---

## ✅ Summary

This project demonstrates:
- Practical AI integration using AWS managed services
- Conscious design trade-offs suitable for an MVP
- System-level thinking beyond simple AI chat interfaces
- A clear, realistic path toward enterprise readiness

---

## 📌 Author Notes

This document exists to explain architectural intent and decision-making and is intended for interview and portfolio review purposes.
