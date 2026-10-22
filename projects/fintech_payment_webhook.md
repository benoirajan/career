# Project STAR: Resilient Payment Webhook & Reconciliation Engine

### Context & Problem (Situation / Task)
* **Situation:** Payment service providers generated high bursts of asynchronous webhook events for payment captures, refunds, and disputes. 
* **Challenge:** Network timeouts and out-of-order webhook delivery caused intermittent double-credits, duplicate charge records, and reconciliation mismatches between external gateways and the internal ledger.
* **Goal:** Architect a bulletproof, idempotent webhook ingestion system meeting strict financial audit standards.

---

### Technical Solution & Architecture (Action)
* **Signature & Replay Verification:** Implemented HMAC-SHA256 signature verification and a timestamp window check to reject stale or replayed payloads before touching the database.
* **Idempotency Guard:** Introduced an idempotency layer utilizing unique gateway event IDs stored in Amazon Aurora PostgreSQL with unique constraints and Redis advisory locks to prevent race conditions during concurrent webhook delivery.
* **Asynchronous Queueing:** Decoupled webhook ingestion from business processing using AWS SQS with Dead-Letter Queues (DLQs) and exponential backoff retries.
* **State Machine & Ledger Reconciliation:** Engineered a finite state machine managing payment lifecycles (`PENDING` -> `CAPTURED` -> `REFUND_REQUESTED` -> `SETTLED` / `DISPUTED`) with automated daily reconciliation jobs comparing gateway reports against internal transaction logs.

---

### Quantifiable Results & Impact (Result)
* **Zero Duplication:** Eliminated 100% of duplicate payment ledger entries and race-condition double credits.
* **High Availability:** Maintained 99.99% ingestion availability during flash-sale traffic spikes, processing over 500+ webhooks/second.
* **Reconciliation Automation:** Reduced manual reconciliation discrepancies by 98%, saving finance teams ~15 hours of manual log inspection weekly.

---

### ATS Resume Bullets (Ready to Paste)
* Architected a high-throughput payment webhook ingestion pipeline using Spring Boot, AWS SQS, and Aurora PostgreSQL, processing 500+ events/sec with zero ledger duplication.
* Implemented cryptographic HMAC payload validation and distributed idempotency controls in Redis, eliminating race conditions and replay attacks.
* Designed an automated financial reconciliation state machine that resolved 98% of discrepancies between gateway settlements and internal balances.
