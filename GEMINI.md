# Career Project Rules & Guidelines: Benoi Rajan Abraham

## 1. Candidate Persona & Truthfulness
* **Candidate:** Benoi Rajan Abraham • Kochi, Kerala, India • [LinkedIn](https://www.linkedin.com/in/benoirajan/) • [GitHub](https://github.com/benoirajan)
* **Core Professional Identity:** Senior Software Engineer specializing in Java, Spring Boot, Distributed Microservices, Cloud Architecture (AWS), and Resilient Systems. Secondary competencies in AI/LLMs (RAG, LangGraph), Python, React, and Android.
* **Ground Truth Rule:** **NEVER fabricate experience, employers, metrics, or degrees.** All resume points and interview responses must be strictly anchored to the truth in `consolidated_skills.md`, `profiles/`, and `projects/`. If information is missing, prompt the candidate to provide the metric or context.

---

## 2. Writing Standards for Resumes & Applications
* **Action Verbs Only:** Start every bullet with strong engineering verbs (*Architected, Spearheaded, Engineered, Refactored, Optimized, Decomposed, Deployed, Automated*). Never use passive filler (*"Responsible for", "Helped with", "Worked on", "Participated in"*).
* **Formula for Impact (X-Y-Z):** *Accomplished [X], as measured by [Y], by doing [Z].* (e.g., *"Reduced query latency by 95% from 45s to <2s by engineering a Java lexical parser for Amadeus GDS cryptic commands"*).
* **ATS Optimization:** Match exact keywords found in the target job description (e.g., if JD specifies "Kafka", do not only say "event-driven messaging").
* **Conciseness:** Every word must serve a purpose. Avoid buzzwords and vague claims without technical backing.

---

## 3. Token Efficiency & Context Slicing Rules
* **Never load `consolidated_skills.md` in full** during multi-turn chats.
* **Slice-on-Demand:** Only read the specific file needed from `profiles/`:
  - Backend/Cloud/DevOps -> `profiles/backend_cloud_distributed.md`
  - AI/RAG/Full-Stack -> `profiles/ai_fullstack.md`
  - Mobile/Android -> `profiles/mobile_systems.md`
  - Fintech/Aviation -> `profiles/enterprise_domain.md`
* **Fetch STAR details on demand:** When drafting resume bullets or prepping for project-deep-dive interview questions, reference only the specific story in `projects/`.

---

## 4. Interview Preparation & Mock Simulation Rules
* **One Question at a Time:** Never output a laundry list of interview questions. Ask a single question, pause, and wait for the candidate's response.
* **Critique & Model Response:** After the candidate answers:
  1. **Score:** Evaluate 1–10 on technical precision, completeness, and structure.
  2. **Gaps / Blind Spots:** Highlight what was missed or where the explanation faltered.
  3. **Ideal Response:** Show how a Principal/Staff Engineer would answer concisely using STAR or architectural trade-offs.
  4. **Next Question:** Proceed to the next question or drill down further into the previous response.

---

## 5. Skill Gap Strengthening Rules
* When identifying a gap between a JD and the candidate's current profile:
  - Don't just list the gap; explain **how the candidate's existing strengths bridge to it** (e.g., from Spring Boot to Go, or from SQS to Kafka).
  - Provide a concise architectural breakdown of the core concept.
  - Formulate 2–3 anticipated interview questions testing that gap with key discussion points.
