---
name: skill-gap-strengthener
description: Diagnoses skill gaps between Benoi Rajan Abraham's profile and target job descriptions, producing focused architectural cheat-sheets, conceptual bridge guides, and targeted interview drill questions to strengthen weak areas.
---

# Skill: Skill Gap Strengthener

Use this skill whenever the user asks to strengthen a weak area, identify what they are missing for a target position, or learn how to speak confidently about technologies they have limited hands-on experience with.

---

## Workflow Steps

### Step 1: Diagnose the Gap
1. Compare target requirements against Benoi's `profiles/` and `consolidated_skills.md`.
2. Categorize the gap:
   * **Category A: Adjacent Technology** (e.g., knows RabbitMQ/SQS, needs Apache Kafka or Pulsar; knows PostgreSQL, needs MongoDB or Cassandra).
   * **Category B: Architectural Abstraction** (e.g., Distributed transactions, 2PC vs SAGA pattern, event sourcing, Kubernetes orchestration).
   * **Category C: Completely New Domain/Tool** (e.g., GraphQL Federation, Golang, Terraform HCL, eBPF).

### Step 2: Build the Conceptual Bridge
Do NOT overwhelm with generic tutorials. Bridge from what Benoi already knows:
* *"Since you already master X in Spring/AWS, here is how Y translates in concept and syntax."*
* Contrast pros, cons, and architectural trade-offs.

### Step 3: Produce the Architectural Cheat Sheet
Deliver a high-density, concise cheat sheet containing:
1. **Core Problem Solved:** Why does this technology exist instead of traditional alternatives?
2. **Key Architectural Concepts:** The 3–5 non-negotiable concepts an interviewer expects you to know cold (e.g. for Kafka: Partitions, Consumer Groups, Offset Commit semantics, Replication Factor, Leader/Follower).
3. **Common Production Pitfalls:** What breaks in production? (e.g. partition rebalances, hot partitions, poison pill messages).

### Step 4: Generate Targeted Interview Drill Questions
Provide 2–3 sharp interview questions specifically designed to test this gap:
* Give the **Question**.
* Give the **Candidate Strategy** (how to frame the answer using existing distributed systems principles even if direct production experience was recent).
* Provide the **Model Answer**.
