# Project STAR: Airline GDS Terminal Modernization & Microservices Migration

### Context & Problem (Situation / Task)
* **Situation:** Aviation flight operations and dispatchers relied on cryptic character-based Amadeus GDS terminal sessions to query Passenger Name Records (PNRs), manage tail numbers, and adjust flight fuel requirements.
* **Challenge:** Monolithic architecture hosted on aging EC2/Tomcat instances was brittle, lacked auditability, and required manual intervention whenever terminal sessions dropped during flight turnarounds.
* **Goal:** Modernize cryptic GDS interactions into cloud-native RESTful microservices on AWS ECS Fargate while maintaining strict backward-compatibility and zero flight operational downtime.

---

### Technical Solution & Architecture (Action)
* **Terminal Parsing Engine:** Designed a robust Java-based lexical parser with deterministic regular expressions to decode unstructured cryptic Amadeus command streams into structured JSON schemas.
* **Containerized Microservices:** Migrated legacy Tomcat workloads into containerized Spring Boot microservices deployed on AWS ECS Fargate, managed via CloudFormation templates.
* **Private Network Isolation:** Enforced AWS VPC PrivateLink / VPC Endpoints to isolate aviation operational services completely from the public internet, routing through Application Load Balancers (ALBs).
* **Automated Operational Workflows:** Built asynchronous workers for PNR status tracking, tail-assignment updates, and fuel-order dispatch notifications with automated retries.

---

### Quantifiable Results & Impact (Result)
* **Turnaround Efficiency:** Reduced PNR query and fuel update latency from 45 seconds to sub-2 seconds via modern API contracts.
* **Operational Reliability:** Achieved 99.95% uptime for critical dispatch services, cutting manual dispatcher escalations by 70%.
* **Cost & Infrastructure Optimization:** Lowered cloud compute costs by 35% by migrating from over-provisioned EC2 instances to auto-scaled ECS Fargate containers.

---

### ATS Resume Bullets (Ready to Paste)
* Spearheaded the migration of legacy airline flight operations from monolithic EC2/Tomcat servers to containerized Spring Boot microservices on AWS ECS Fargate.
* Engineered a high-speed parsing engine to translate unstructured Amadeus GDS cryptic commands into structured RESTful JSON APIs, reducing dispatcher query latency by 95%.
* Established secure zero-trust network boundaries using AWS VPC Endpoints and PrivateLink, ensuring complete public internet isolation for critical flight data.
