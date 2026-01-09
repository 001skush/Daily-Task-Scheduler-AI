📘 PROJECT_NOTES.md
Daily Task Scheduler (AI-Powered)

This document captures the design decisions, trade-offs, limitations, and reasoning behind the Daily Task Scheduler (AI-Powered) application.
It is intended to explain why the system was built this way, not just what it does.

🎯 Project Intent

The primary goal of this project was to demonstrate AI-driven workflow design on AWS, not traditional full-stack development.

Specifically, the project focuses on:

Embedding AI into a real productivity use case

Structuring unstructured user input for reliable AI output

Leveraging fully managed AWS services to minimize operational overhead

Designing a system that can evolve into an enterprise-grade solution

🧠 Key Design Decisions
1️⃣ No-Code Architecture (PartyRock + Bedrock)

Decision:
Use AWS PartyRock with Amazon Bedrock instead of building a custom frontend and backend.

Reasoning:

Keeps the focus on AI logic and system behavior

Eliminates boilerplate infrastructure work

Demonstrates modern rapid AI application development patterns

Ensures scalability, availability, and security are AWS-managed

Trade-off:

Limited control over low-level application behavior

No custom backend logic in v1

This was an intentional trade-off to prioritize AI workflow design.

2️⃣ Accepting Unstructured User Input

Decision:
Allow users to enter tasks as free-form text instead of a strict schema.

Reasoning:

Mirrors how people actually write task lists

Forces the AI to perform reasoning and interpretation

Demonstrates real-world AI usage rather than ideal inputs

Mitigation:

Prompt structure enforces clear task interpretation

Examples and UI guidance improve input quality

3️⃣ Prompt-Based Scheduling Logic

Decision:
Use prompt engineering instead of rule-based scheduling algorithms.

Reasoning:

Allows flexible reasoning across priorities, effort, and constraints

Enables productivity insights beyond simple scheduling

Keeps the system adaptable without hardcoding business rules

Trade-off:

Output quality depends on prompt clarity

Less deterministic than traditional scheduling algorithms

This approach reflects how AI is often used in modern decision-support systems.

4️⃣ Overload Detection via AI Reasoning

Decision:
Detect overloaded schedules through AI analysis rather than strict calculations.

Reasoning:

Allows nuanced warnings and recommendations

Enables explanations instead of binary errors

Aligns with human-like productivity judgment

Constraint:

Overload detection depends on accurate time estimates from users

⚠️ Known Limitations (V1)

No persistent storage (data resets on refresh)

Single-day scheduling only

No user authentication

No external calendar integrations

These limitations were accepted by design to keep the project:

Free-tier friendly

Fully serverless

Focused on AI reasoning rather than infrastructure complexity

🛠️ What I Would Change in Production

In a production-grade version, I would introduce:

Persistent storage using Amazon DynamoDB

User authentication via Amazon Cognito

Hybrid scheduling logic (rules + AI)

Calendar integrations (Google / Outlook)

Usage analytics and feedback loops to improve AI output quality

The core AI reasoning layer (Bedrock) would remain unchanged.

📈 Evolution Path (V2 Vision)

This project is designed to evolve naturally into an enterprise-ready system:

Save historical schedules and productivity metrics

Provide weekly and monthly insights

Support multiple users and teams

Introduce access controls and auditability

This evolution would demonstrate scalability without rewriting the core logic.

🎓 Key Learnings

AI systems require input discipline, not just model access

Prompt structure directly affects output reliability

Managed services accelerate innovation when used intentionally

Designing for evolution is as important as building v1

✅ Summary

This project demonstrates:

Practical AI integration using AWS managed services

System-level thinking beyond simple AI chat interfaces

Conscious trade-offs suitable for an MVP

A clear path toward enterprise-grade expansion

📌 Author Notes

This document exists to explain architectural intent and decision-making, especially in interview and portfolio review contexts.
