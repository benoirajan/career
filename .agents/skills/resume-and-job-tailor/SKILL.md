---
name: resume-and-job-tailor
description: Parses target job descriptions (JDs), evaluates skill match against modular profiles, identifies ATS keywords, and generates tailored resumes and cover letters for Benoi Rajan Abraham.
---

# Skill: Resume & Job Tailor

Use this skill whenever the user provides a Job Description (JD), asks to apply for a role, or requests a customized resume or cover letter.

---

## Workflow Steps

### Step 1: Analyze the Job Description (JD)
1. Extract the target role title, senior level, and company domain.
2. Identify **Mandatory Requirements** vs. **Preferred/Nice-to-Have Skills**.
3. Extract critical **ATS Keywords** (e.g., `Java 17`, `Spring Boot`, `AWS ECS`, `Kafka`, `PostgreSQL`, `Distributed Caching`, `Microservices`).

### Step 2: Select the Matching Profile Slice
Do NOT read `consolidated_skills.md`. Select only the relevant profile slice from `profiles/`:
* If Backend/Cloud/DevOps -> Read `profiles/backend_cloud_distributed.md`
* If AI/Full-Stack/LLM -> Read `profiles/ai_fullstack.md`
* If Mobile/Android -> Read `profiles/mobile_systems.md`
* If Fintech/Airline domain -> Read `profiles/enterprise_domain.md`

### Step 3: Compute Match & Gap Analysis
Generate a quick tabular assessment:
* **Direct Matches (Strong):** Skills candidate has proven in production.
* **Transferable Matches:** Skills where adjacent experience applies (e.g., RabbitMQ -> Kafka, AWS SQS -> Google PubSub).
* **Missing / Gaps:** Keywords required by the JD that are absent from the profile.
* **Match Score:** Estimated ATS alignment percentage (e.g., 85%).

### Step 4: Tailor the Resume & Cover Letter
1. Open `templates/resume_base_ats.md` and `templates/cover_letter_template.md`.
2. Inspect `projects/` for applicable STAR stories matching the JD's primary pain points (e.g. `projects/fintech_payment_webhook.md` for payment/high-throughput roles, `projects/airline_gds_modernization.md` for migration/microservices roles).
3. Tailor the **Professional Summary**, **Technical Skills**, and **Experience Bullets**:
   - Reorder technical skills so the JD's primary requirements appear first.
   - Inject the extracted ATS keywords naturally into bullet points.
   - Enforce the X-Y-Z formula (*Accomplished [X], measured by [Y], through [Z]*).
4. Generate the customized cover letter highlighting 2 specific project accomplishments that directly solve the employer's needs.

---

## Output Format
Always present:
1. **Fit Analysis & Keyword Checklist** (Tabular summary of matches and missing keywords).
2. **Tailored Resume (Markdown)** (Ready to copy or export to PDF).
3. **Targeted Cover Letter** (Personalized to the hiring team and company).
