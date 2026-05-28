# Interview Preparation Pack
## Role: Systems Integration Engineer — Nscale

---

## Table of Contents

1. [JD Analysis & Role Breakdown](#1-jd-analysis--role-breakdown)
2. [Role Summary & What Interviewers Look For](#2-role-summary--what-interviewers-look-for)
3. [Top Focus Areas to Prepare](#3-top-focus-areas-to-prepare)
4. [Key Concepts You Must Understand](#4-key-concepts-you-must-understand)
5. [Likely Real-World Scenarios](#5-likely-real-world-scenarios)
6. [Common Pitfalls & Weak Answers to Avoid](#6-common-pitfalls--weak-answers-to-avoid)
7. [Answering Strategy](#7-answering-strategy)
8. [Interview Question Bank](#8-interview-question-bank)
9. [Mock Interview Test (4 Rounds)](#9-mock-interview-test-4-rounds)
10. [Practical Hands-On Assessment](#10-practical-hands-on-assessment)
11. [Final Preparation Plan](#11-final-preparation-plan)
12. [Final Summary](#12-final-summary)

---

## 1. JD Analysis & Role Breakdown

### Extracted Role Details

| Dimension | Detail |
|-----------|--------|
| **Role Title** | Systems Integration Engineer |
| **Seniority** | Mid-Senior (3–5 years required; scope suggests IC2/IC3 level) |
| **Company Stage** | Pre-IPO, high-growth, scaling 500 → 1,000+ employees |
| **Industry** | GPU Cloud / AI Infrastructure |
| **Primary Platform** | Palantir Foundry (integration hub) |
| **Reporting To** | Senior Director of Systems Integrations |

### Core Responsibilities (Prioritized by JD Weight)

| Priority | Responsibility |
|----------|---------------|
| 1 | Design & build enterprise integrations (ERP, HRIS, CRM, ATS, ITSM) |
| 2 | JML automation (Joiner/Mover/Leaver lifecycle workflows) |
| 3 | Solution architecture — patterns, ADRs, standards definition |
| 4 | Data quality, governance, master data management |
| 5 | Compliance support (SOX, SOC 2, ISO 27001) |
| 6 | Operational monitoring, alerting, and L2/L3 support |
| 7 | Tooling evaluation and PoC builds |
| 8 | M&A integration support |

### Must-Have Technical Skills

- REST APIs, webhooks, OAuth 2.0, SAML 2.0, SCIM provisioning
- Integration platforms: Workato, Celigo, MuleSoft, Boomi, Zapier, or Make (at least one)
- Core SaaS integrations: NetSuite/SAP, Workday/BambooHR, Salesforce/HubSpot, Greenhouse/Lever
- IAM: Okta, JumpCloud, Azure AD
- Python or JavaScript (scripting, custom API logic)
- SQL (validation, troubleshooting, data queries)
- ETL/ELT patterns, data transformation, field mapping
- API troubleshooting: HTTP logs, JSON payloads, status codes

### Good-to-Have Skills

- Palantir Foundry hands-on experience
- JML workflow design and implementation
- SOX/SOC 2/ISO 27001 compliance knowledge
- Enterprise/solutions architecture background
- Pre-IPO company experience
- M&A integration exposure
- CI/CD for integration pipelines
- Data governance and MDM frameworks

### Domain Knowledge Required

- Enterprise application landscape (SaaS ecosystem)
- Identity & Access Management lifecycle
- Audit and compliance controls (ITGCs)
- Integration architecture patterns (point-to-point, hub-and-spoke, event-driven)
- Data ownership and master data management

### Leadership & Behavioral Expectations

- Translate ambiguous business requirements into concrete technical designs
- Define and enforce integration standards across the org
- Create documentation (ADRs, runbooks, playbooks)
- Work cross-functionally with HR, Finance, IT, Security, and Enterprise Architecture
- Own production reliability — not just build and hand off
- Influence tooling and platform decisions

### Likely Business Problems You'll Be Asked to Solve

1. "Our HRIS and ERP are out of sync — how do you fix it?"
2. "We onboarded 50 people last quarter and 10 had wrong access for 2 weeks — what went wrong and how do you solve it?"
3. "We're acquiring a startup — how do you integrate their 15 SaaS tools into our estate?"
4. "Auditors want proof that leavers lose access within 24 hours — how do you demonstrate this?"
5. "Our integration platform is failing silently — how do you know something is broken before the business does?"

---

## 2. Role Summary & What Interviewers Look For

### Role in Plain Language

You are the engineer who makes all of Nscale's internal software systems talk to each other reliably. When someone joins the company, your code provisions their accounts. When they leave, your code revokes access. When Finance closes the books, your pipelines ensure data from CRM, ERP, and billing systems are consistent. You sit at the intersection of software engineering, enterprise IT, and business operations.

This is not a pure developer role and not a pure IT admin role — it is a **technical integration specialist** with ownership over architecture, automation, compliance, and production reliability.

### What the Interviewer Is Looking For

| Dimension | Signal They Want |
|-----------|-----------------|
| **Hands-on depth** | Real experience with APIs, auth flows, data transformation — not just theoretical knowledge |
| **System thinking** | Can you see how data flows end-to-end across 10+ systems, not just one API at a time? |
| **Compliance awareness** | Do you naturally think about audit trails, access controls, and change management? |
| **Reliability engineering** | Do you build integrations that fail gracefully, alert loudly, and recover automatically? |
| **Business translation** | Can you talk to a non-technical HR VP and then go build exactly what was needed? |
| **Scalability mindset** | Pre-IPO means this will be scrutinized — are your solutions built to last, not just to work today? |
| **Ownership** | Do you monitor, support, and improve what you built, or do you throw it over the wall? |

---

## 3. Top Focus Areas to Prepare

| # | Focus Area | Why It Matters |
|---|-----------|----------------|
| 1 | JML (Joiner/Mover/Leaver) workflow design | Explicitly called out; likely a deep technical drill |
| 2 | REST API design, OAuth 2.0, SCIM | Core technical foundation tested in every round |
| 3 | Integration architecture patterns | You'll be asked to whiteboard hub-and-spoke vs event-driven |
| 4 | HRIS + Identity integration (Workday → Okta) | The canonical enterprise integration use case |
| 5 | Error handling and retry patterns | Critical for production reliability |
| 6 | SOX/SOC 2 controls for integrations | Nscale is pre-IPO — this is non-negotiable |
| 7 | Data quality and master data management | Explicitly listed as a core responsibility |
| 8 | Palantir Foundry or equivalent iPaaS | Mentioned as the primary platform — research it |
| 9 | SQL for data validation | Will likely appear in a practical test |
| 10 | Troubleshooting API failures | Scenario questions will test this |
| 11 | Integration platform trade-offs | PoC, evaluation, build vs buy decisions |
| 12 | M&A integration strategy | Mentioned explicitly — have a framework ready |
| 13 | ADR writing and documentation | Soft skill with technical depth |
| 14 | Monitoring and alerting design | Operational maturity signal |
| 15 | Pre-IPO scale and compliance pressures | Cultural and contextual fit |

---

## 4. Key Concepts You Must Understand

### Authentication & Authorization

**OAuth 2.0 Flows**
- Authorization Code Flow (user-facing apps)
- Client Credentials Flow (machine-to-machine integrations — most common in enterprise integrations)
- Refresh token mechanics and token expiry handling

**SAML 2.0**
- SP-initiated vs IdP-initiated flows
- Assertions, attributes, metadata exchange
- Use in SSO between SaaS applications

**SCIM (System for Cross-domain Identity Management)**
- SCIM 2.0 endpoints: `/Users`, `/Groups`
- Operations: Create, Read, Update, Delete (CRUD) + Patch
- Used for automated provisioning from IdP (Okta) to downstream apps
- Difference between SCIM push vs SCIM pull

**API Key vs OAuth vs Service Accounts**
- When to use each and associated security risks

---

### Integration Architecture Patterns

| Pattern | Description | When to Use | Trade-offs |
|---------|-------------|-------------|------------|
| **Point-to-Point** | Direct API calls between two systems | Simple, low volume, 2–3 systems | Does not scale; becomes a spaghetti mess at 10+ systems |
| **Hub-and-Spoke** | Central integration platform mediates all flows | Standard enterprise at 10–50 integrations | Single point of failure; platform dependency |
| **Event-Driven / ESB** | Systems publish events; consumers subscribe | High volume, real-time, loose coupling | Complex to operate; eventual consistency challenges |
| **Batch ETL** | Scheduled data extracts and loads | Reporting, archival, non-real-time sync | Latency; hard to handle deletes |
| **API Gateway / Facade** | Unified API layer over multiple backends | Standardizing messy legacy API surfaces | Extra hop; versioning complexity |

---

### JML (Joiner/Mover/Leaver) Architecture

```
JOINER FLOW:
ATS (Greenhouse) ──► HRIS (Workday) ──► IdP (Okta) ──► App Provisioning ──► Hardware Request

MOVER FLOW:
HRIS Role Change ──► Okta Group Update ──► App Role Recalculation ──► Access Review Trigger

LEAVER FLOW:
HRIS Termination ──► Okta Suspend/Deactivate ──► App Deprovisioning ──► MDM Device Wipe ──► License Reclaim
```

**Critical SLAs for Compliance:**
- Leavers: deprovisioning must complete within 2–4 hours of termination (SOX/SOC 2 requirement)
- All steps must be logged with timestamps (audit trail)
- No manual workarounds allowed (SOX control)
- Failed steps must alert immediately

---

### Data Quality Concepts

- **Master Data Management (MDM):** Designating a single authoritative source for each data entity (e.g., employee data lives in HRIS, not 5 systems)
- **Golden Record:** The authoritative merged version of a record across systems
- **Data Lineage:** Knowing where data originated, how it transformed, and where it landed
- **Idempotency:** Running the same integration twice produces the same result — critical for retries
- **Deduplication strategies:** Exact match, fuzzy match, survivorship rules

---

### Compliance Concepts for Integrations

| Control | What It Means for Integrations |
|---------|-------------------------------|
| **SOX ITGC** | Logical access controls must be auditable; access provisioning/deprovisioning must be controlled and documented |
| **SOC 2 CC6** | Logical and physical access is restricted; JML workflows must demonstrate controlled access |
| **SOC 2 CC7** | System operations monitored for anomalies — integration monitoring and alerting |
| **ISO 27001 A.9** | Access control policy — same JML/SCIM considerations |
| **Change Management** | All integration changes must go through a controlled change process |

---

### Error Handling Patterns

```python
# Retry with exponential backoff (Python example)
import time
import requests

def call_api_with_retry(url, headers, payload, max_retries=3):
    for attempt in range(max_retries):
        try:
            response = requests.post(url, headers=headers, json=payload)
            response.raise_for_status()
            return response.json()
        except requests.exceptions.HTTPError as e:
            if response.status_code == 429:  # Rate limited
                wait = 2 ** attempt
                time.sleep(wait)
            elif response.status_code >= 500:  # Server error - retry
                time.sleep(2 ** attempt)
            else:  # 4xx client error - do not retry
                raise
        except requests.exceptions.ConnectionError:
            time.sleep(2 ** attempt)
    raise Exception(f"API call failed after {max_retries} retries")
```

Key error handling considerations:
- Distinguish retryable (5xx, 429, network timeouts) from non-retryable (4xx) errors
- Idempotency keys to prevent duplicate operations on retry
- Dead letter queues for failed events
- Circuit breaker pattern for downstream system failures
- Alert on sustained failure rate, not just individual failures

---

## 5. Likely Real-World Scenarios

| Scenario | What They Are Testing |
|----------|-----------------------|
| "Design the onboarding workflow for 50 new hires joining on the same day" | JML at scale, idempotency, race conditions |
| "An API integration has been silently failing for 3 hours — walk me through your investigation" | Troubleshooting, monitoring design |
| "Finance says the headcount in NetSuite doesn't match Workday — how do you investigate?" | Data quality, MDM, tracing data lineage |
| "We're acquiring a 200-person company — they have Salesforce, HubSpot, and 10 other tools. What's your plan?" | M&A integration framework |
| "A SOX auditor wants to see proof that leavers lose access within 24 hours — what do you show them?" | Compliance, audit trails, logging |
| "Okta says a user's account is active but Workday shows them as terminated — what happened?" | Data sync debugging, JML reliability |
| "We need to evaluate whether to use Workato, Celigo, or build custom. How do you decide?" | Platform evaluation, build vs buy |
| "The Salesforce API rate limit is 15,000 calls/day and we're hitting it — what do you do?" | API efficiency, bulk operations, throttling |

---

## 6. Common Pitfalls & Weak Answers to Avoid

| Pitfall | Why It Fails |
|---------|-------------|
| "I would use webhooks for everything" | Shows lack of nuance — webhooks fail silently, have no delivery guarantee without confirmation, and need fallback polling |
| "I'd just write a Python script to sync the data" | Misses platform context, monitoring, error handling, maintainability, and compliance requirements |
| "I haven't worked with Palantir Foundry but I'm a quick learner" | Not wrong, but needs to be supplemented with comparable iPaaS depth |
| Generic STAR answers without integration-specific detail | Behavioral answers need technical grounding for this role |
| Ignoring compliance when describing JML | Fatal — SOX/SOC 2 is explicitly mentioned; every JML answer must address audit trails |
| "We tested it in staging so it should be fine" | Production integration work requires monitoring, alerting, and rollback — testing alone is insufficient |
| Describing integration as purely technical with no business context | This role requires translating business needs — show you understand the "why" |
| Treating all data syncs as identical | Different entities (employees, customers, contracts) have different ownership, frequency, and conflict resolution rules |

---

## 7. Answering Strategy

### For Technical Questions: Use DEEP Framework

- **D**efine the problem and constraints (systems, volume, SLAs)
- **E**xplain your approach and architecture
- **E**dge cases and error scenarios you've considered
- **P**roduction readiness (monitoring, documentation, compliance)

### For Scenario Questions: Use TRACE Framework

- **T**rigger — what event initiates this?
- **R**oute — what path does data take through systems?
- **A**ction — what does each system do?
- **C**ontrols — what compliance/error controls exist?
- **E**vidence — how do you prove it worked (audit logs, monitoring)?

### For Architecture Questions

Always cover:
1. Current state (what problem exists)
2. Target state (what you are designing)
3. Trade-offs considered (why this approach over alternatives)
4. Migration path (how to get there without breaking things)
5. Operational concerns (monitoring, alerting, runbooks)

### For Behavioral Questions: STAR with Metrics

- Situation (2–3 sentences, business context)
- Task (your specific role and ownership)
- Action (technical detail — what exactly you built/changed)
- Result (quantified outcome — time saved, errors eliminated, SLA met)

---

## 8. Interview Question Bank

---

### 8.1 Resume & Introduction Questions

---

**Q1: Walk me through your background and why you're a fit for this role.**

*Why asked:* Baseline fit check; tests self-awareness and communication.

*Strong answer includes:*
- Clear progression from earlier integration work to increasing complexity
- Specific systems you've integrated (name the ERP, HRIS, CRM)
- One or two concrete outcomes (e.g., "automated onboarding for 300 employees")
- Why Nscale's scale and pre-IPO context excites you specifically

*Weak answer misses:*
- Generic "I'm a team player who loves automation"
- No specific systems or platforms named
- No connection to Nscale's specific challenges (IPO, scale, compliance)

*Sample outline:*
> "I have 4 years building enterprise integrations at [company], where I owned the integration layer between Workday, Okta, Salesforce, and NetSuite using MuleSoft. I designed and implemented the JML automation that reduced manual IT provisioning work by 80% and helped us pass our first SOC 2 audit. What excites me about Nscale is the pre-IPO scale challenge — building integration infrastructure that can hold up under audit scrutiny while supporting aggressive headcount growth is exactly the type of problem I want to own."

---

**Q2: What is the most complex integration you have built? Walk me through the architecture.**

*Why asked:* Tests real depth vs. surface-level familiarity.

*Strong answer includes:*
- Named systems on both ends
- Auth method used (OAuth, API key, SCIM)
- Data transformation logic (field mapping, type conversion, ID reconciliation)
- Error handling and retry strategy
- How you monitored it in production
- What you would do differently now

*Weak answer misses:*
- High-level description without mentioning auth, transformation, or error handling
- No production monitoring consideration
- No reflection or lessons learned

---

**Q3: Describe a time an integration you built failed in production. What happened?**

*Why asked:* Tests ownership, post-mortems, and learning culture.

*Strong answer includes:*
- Honest description of the failure mode (silent failure, data corruption, missed webhook)
- How it was detected (ideally by your monitoring, not by users)
- Root cause analysis process
- Immediate remediation steps
- Systemic changes made to prevent recurrence
- Documentation or runbook updates

*Weak answer misses:*
- Blaming the vendor or another team
- No systemic fix — just "we fixed the bug"
- Failure was caught by end users, not monitoring

---

### 8.2 Role-Fit Questions

---

**Q4: Nscale is scaling from 500 to 1,000+ people and preparing for IPO. What does that mean for an integration engineer?**

*Why asked:* Tests business context awareness and IPO readiness understanding.

*Strong answer includes:*
- Audit trail requirements intensify (SOX ITGC readiness)
- Every manual process is a compliance risk — automation is mandatory
- Integration failures become business-critical (not just IT inconveniences)
- Documentation and change management become formal requirements
- Data consistency directly affects financial reporting accuracy
- Speed matters — integrations must support rapid onboarding without slowing HR

*Weak answer misses:*
- Only mentioning scale without mentioning compliance
- Not connecting integrations to financial reporting accuracy

---

**Q5: This role sits at the intersection of IT, engineering, and business operations. How do you manage that?**

*Why asked:* Tests cross-functional effectiveness and communication style.

*Strong answer includes:*
- Concrete example of translating a business requirement (HR: "new hires need access day one") into a technical design
- How you document and get alignment before building
- How you communicate integration failures to non-technical stakeholders
- How you manage conflicting priorities between business teams

---

**Q6: Palantir Foundry is mentioned as the primary integration platform. What's your experience with it, and how would you approach getting up to speed?**

*Why asked:* Tests honesty, platform awareness, and learning approach.

*If you have Foundry experience:*
- Describe specific pipelines, transforms, and connector types used

*If you don't:*
> "I haven't worked directly in Foundry, but I've used [MuleSoft / Workato / Boomi] for similar iPaaS use cases — orchestrating API calls, managing data transforms, and building event-driven flows. My approach would be to start with Palantir's documentation and training, map concepts from platforms I know (e.g., Foundry Pipelines ≈ MuleSoft Flows, Foundry Transforms ≈ ETL logic), build a PoC on a lower-risk integration in the first two weeks, and pair with the existing Foundry team to understand the established patterns."

---

### 8.3 Technical Knowledge Questions

---

**Q7: Explain the difference between OAuth 2.0 Client Credentials flow and Authorization Code flow. When would you use each in enterprise integrations?**

*Why asked:* Authentication is foundational to every integration.

*Strong answer:*
- **Authorization Code Flow:** User is present; used for delegated access (e.g., a user authorizing your app to read their Salesforce data). Requires redirect URI, authorization code exchange.
- **Client Credentials Flow:** Machine-to-machine; no user present; application authenticates as itself. Used for background integration processes (e.g., syncing Workday employees to Okta nightly). The most common flow in enterprise integrations.
- Authorization Code requires refresh tokens and UI interaction; Client Credentials uses client ID + secret for token exchange directly.

*Weak answer misses:*
- Confusing the two flows
- Not mentioning that Client Credentials is the enterprise integration standard
- Forgetting token expiry and refresh handling

---

**Q8: What is SCIM and how does it work in the context of user provisioning?**

*Why asked:* Central to JML automation and IAM integration.

*Strong answer:*
- SCIM 2.0 is a standardized REST-based protocol for automating user provisioning between identity providers and applications
- IdP (Okta) acts as SCIM client, applications act as SCIM server
- Endpoints: `POST /Users` (create), `PUT/PATCH /Users/{id}` (update), `DELETE /Users/{id}` (deprovision)
- Attributes: `userName`, `emails`, `groups`, `active`
- Advantage over custom APIs: standardized schema, automatic deprovisioning on `active: false`
- Difference between SCIM push provisioning (IdP pushes on change) vs. SCIM import/reconciliation (IdP pulls to discover existing users)
- Limitations: not all apps have SCIM; some have partial SCIM support (e.g., no group push)

---

**Q9: What is the difference between ETL and ELT, and when would you use each in an enterprise integration context?**

*Strong answer:*

| | ETL | ELT |
|-|-----|-----|
| **Process** | Extract → Transform → Load | Extract → Load → Transform |
| **Where transform happens** | Staging/integration layer | Target data warehouse |
| **Best for** | Sensitive data that must be cleaned before landing; legacy systems | Modern cloud data warehouses (Snowflake, BigQuery); large volumes |
| **Example use** | Syncing HRIS to ERP (transform employee ID format, null-check required fields before loading to NetSuite) | Syncing raw event data to a data warehouse for reporting |

In enterprise SaaS integrations (not data warehouse), ETL is typically used — you transform in your integration platform (Workato, MuleSoft) before writing to the target system, because SaaS APIs enforce schema and validation.

---

**Q10: Walk me through how you would design retry and error handling for a critical integration (e.g., HRIS → IdP sync).**

*Why asked:* Production reliability is explicitly in the JD.

*Strong answer covers:*
1. **Classify errors:** 4xx (client errors, do not retry — fix the payload), 5xx (server errors, retry), 429 (rate limit, backoff), network timeout (retry)
2. **Exponential backoff with jitter:** Avoid thundering herd on shared APIs
3. **Idempotency:** Assign idempotency key per operation; retrying same operation must not create duplicates (e.g., don't create the same Okta user twice)
4. **Dead letter queue / failed record store:** Records that fail after max retries go to a review queue; do not silently drop
5. **Alerting:** Alert on failure rate threshold, not just individual failures
6. **Circuit breaker:** If downstream is consistently failing, stop hammering it and alert
7. **Manual retry capability:** Operations team can inspect failed records and re-trigger
8. **Audit log entry:** Every attempt (success or failure) logged with timestamp and outcome

---

**Q11: How do you handle rate limits when integrating with a SaaS API like Salesforce or HubSpot?**

*Strong answer:*
- Read the API documentation to understand limits (daily limits, per-minute limits, concurrent limits)
- Use bulk API endpoints where available (Salesforce Bulk API 2.0 for large datasets vs. REST API)
- Implement request throttling in your integration layer — don't parallelize all calls
- Cache read-heavy data locally to avoid repeated API calls for reference data
- Use API rate limit headers (`X-RateLimit-Remaining`, `Retry-After`) to dynamically throttle
- Schedule large syncs during off-peak hours
- Request a rate limit increase if legitimately needed
- Consider webhook subscriptions instead of polling to dramatically reduce API call volume

---

**Q12: What is the difference between a synchronous and an asynchronous integration? Give an example of each.**

*Strong answer:*
- **Synchronous:** Caller waits for the response before proceeding. Example: A user creates a contract in your CRM and your integration immediately writes it to NetSuite and returns a confirmation before the UI unblocks. Pro: immediate feedback. Con: latency, cascading failures.
- **Asynchronous:** Caller sends a message/event and does not wait for completion. Processing happens separately. Example: When Workday detects a termination, it publishes an event to a queue; the Okta deprovisioning workflow consumes that event independently. Pro: decoupled, resilient. Con: eventual consistency, harder to debug.
- In enterprise integrations, asynchronous patterns (event-driven, message queues) are preferred for high-volume or non-blocking operations; synchronous is used where the UI or business process requires immediate confirmation.

---

**Q13: Describe how you would build a reliable webhook receiver for a critical system.**

*Strong answer:*
1. **Acknowledge immediately (HTTP 200):** Return 200 as soon as the webhook arrives — before processing — to prevent the sender from retrying prematurely
2. **Queue for async processing:** Put the payload into an internal queue (e.g., SQS, RabbitMQ, or iPaaS queue) for processing
3. **Verify the signature:** Most platforms (Okta, GitHub, Stripe) sign webhooks with HMAC-SHA256; verify the signature to reject spoofed events
4. **Idempotency check:** Store processed event IDs to handle duplicate deliveries
5. **Replay mechanism:** Ability to re-process events from the queue for debugging
6. **Monitoring:** Alert on queue depth (events backing up) and processing failures
7. **Schema validation:** Validate payload shape before processing to catch breaking changes in the sender's schema

---

**Q14: What SQL would you write to identify duplicate employee records across two systems?**

*Why asked:* SQL is explicitly listed as a required skill for data validation.

```sql
-- Find employees in HRIS that have duplicate entries based on email
SELECT 
    email,
    COUNT(*) AS record_count,
    STRING_AGG(employee_id::text, ', ') AS employee_ids,
    STRING_AGG(status, ', ') AS statuses
FROM hris_employees
GROUP BY email
HAVING COUNT(*) > 1
ORDER BY record_count DESC;

-- Cross-system: Find employees in Workday but missing in Okta
SELECT 
    w.employee_id,
    w.email,
    w.full_name,
    w.status AS workday_status,
    o.login AS okta_login
FROM workday_employees w
LEFT JOIN okta_users o ON LOWER(w.email) = LOWER(o.login)
WHERE w.status = 'active'
  AND o.login IS NULL;

-- Find employees with access in Okta but terminated in Workday
-- (compliance risk: orphaned accounts)
SELECT 
    o.login,
    o.full_name,
    o.account_status AS okta_status,
    w.status AS workday_status,
    w.termination_date
FROM okta_users o
INNER JOIN workday_employees w ON LOWER(o.login) = LOWER(w.email)
WHERE w.status = 'terminated'
  AND o.account_status = 'active'
ORDER BY w.termination_date;
```

*Strong answer also mentions:*
- Case-insensitive email comparison (LOWER())
- Handling null values
- Joining on stable identifiers where email may change (employee ID preferred where available)
- Running this as a scheduled data quality check, not just one-off

---

**Q15: What is an Architectural Decision Record (ADR) and when would you write one?**

*Strong answer:*
- An ADR is a short document capturing: the context, the decision made, the alternatives considered, and the reasoning — particularly when a decision has significant and long-lasting consequences
- For integrations: write an ADR when choosing between integration architecture patterns, selecting a platform (Workato vs. MuleSoft), choosing a data ownership model, or deciding on a JML approach
- Key sections: Context, Decision, Status (Proposed/Accepted/Deprecated), Consequences (positive and negative), Alternatives Considered
- Value: future engineers understand WHY a decision was made, not just what was decided; prevents relitigating the same decisions

---

### 8.4 Practical Scenario-Based Questions

---

**Q16: Design the Joiner workflow for a new employee at Nscale. Start from offer acceptance in Greenhouse and end with the employee having full access on day one.**

*Why asked:* This is the core JML scenario and will be asked in depth.

*Strong answer — full workflow:*

```
TRIGGER: Greenhouse "Hired" status updated (webhook → integration platform)

STEP 1: HRIS Record Creation
- Sync new hire data from Greenhouse to Workday (or BambooHR)
- Map fields: name, email, start date, department, manager, job title, location
- Generate employee ID in HRIS
- Validation: check for duplicate email, required fields present
- Error: alert HR if creation fails

STEP 2: Identity Creation (Okta)
- Trigger: Workday "pre-hire" employee created OR start date - X days
- Create Okta user with attributes from Workday
- Assign base groups (company-wide access, department group)
- Generate temporary password / send activation email
- Validation: confirm Okta user created with correct attributes

STEP 3: Application Provisioning (SCIM / API)
- Based on Okta group membership, SCIM pushes user to downstream apps:
  - Google Workspace / Microsoft 365 (email, calendar)
  - Slack
  - ITSM tool (ServiceNow/Jira)
  - HR portal
  - Role-specific tools (engineer: GitHub, AWS; finance: NetSuite)
- Not all apps support SCIM — some require API calls or manual triggers

STEP 4: Hardware / Equipment Ordering
- Trigger: HRIS record created with start date and location
- API call to device management system or IT ticketing to create hardware request
- Route to correct office/shipping address

STEP 5: Confirmation and Monitoring
- Send notification to IT/HR that provisioning is complete
- Log all steps with timestamps to audit trail
- Alert if any step fails or times out

COMPLIANCE CONTROLS:
- All access granted based on role-based rules, not individual requests
- Audit log captures who requested access, what was granted, when
- No access granted before official start date (unless explicitly approved)
```

*Weak answer misses:*
- Steps between Greenhouse and Okta (HRIS is the intermediary, not Greenhouse → Okta direct)
- Error handling at each step
- Role-based access control principles
- Audit trail requirement
- What happens if the employee's start date changes after provisioning starts

---

**Q17: A user was terminated in Workday but still has active Okta access 3 days later. Walk me through your investigation and fix.**

*Why asked:* Tests troubleshooting depth and understanding of JML failure modes.

*Strong answer:*

**Investigation:**
1. Check the Workday-to-Okta integration logs — was the termination event fired? What was the timestamp?
2. Check if the event was received by the integration platform (Workato/Foundry) — was there a processing error?
3. Check Okta provisioning logs — was a deactivation request sent? What was the response?
4. Check if there was a timing issue — did termination happen after business hours when a scheduled sync was paused?
5. Check if the employee had multiple accounts or accounts provisioned outside the standard JML flow (shadow IT)

**Likely root causes:**
- Workday termination event did not trigger webhook (webhook delivery failure)
- Integration platform had an unhandled error (e.g., Okta returned 429 and retry failed silently)
- Employee had a secondary account not linked to HRIS record
- Termination was done as a status field change, not via the workflow that triggers the integration

**Immediate fix:**
- Manually deactivate the Okta account now (do not wait for the automated fix)
- Audit all downstream apps provisioned via Okta — revoke there too
- Document the incident with timeline

**Systemic fix:**
- Add a daily reconciliation job: query Workday for all terminated employees, cross-check Okta for active accounts, auto-flag and deactivate mismatches
- Improve webhook delivery monitoring — alert if no Workday termination events received in a 24-hour period during business days
- Add end-to-end integration tests for the leaver flow

---

**Q18: Finance reports that the headcount number in NetSuite doesn't match Workday. It's month-end close and they need it fixed in 2 hours. What do you do?**

*Strong answer — two tracks: immediate and systemic:*

**Immediate (firefighting):**
1. Pull the current headcount from both systems via SQL/API — get exact numbers and delta
2. Export both datasets and diff them — identify which specific records are missing or extra in NetSuite
3. Likely causes: new hires added in Workday but sync failed; terminations processed in Workday but not yet reflected in NetSuite; timing difference (sync runs at midnight but Workday was updated today)
4. For the immediate gap: identify the delta records, validate them, manually trigger a sync or apply a corrective data patch to NetSuite
5. Communicate a timeline to Finance — "I'll have this resolved in 90 minutes, here is the current delta"

**Root cause (post-close):**
1. Review integration logs for failed syncs in the relevant period
2. Identify the failure pattern (one-time spike or recurring?)
3. Implement a data reconciliation report that runs daily and alerts when delta exceeds a threshold
4. Consider adding a real-time sync for hires/terminations rather than relying on a nightly batch

---

**Q19: You are evaluating whether to use Workato, Celigo, or build a custom Python-based integration framework. What is your evaluation criteria?**

*Strong answer:*

| Criteria | Workato | Celigo | Custom Python |
|----------|---------|--------|---------------|
| Pre-built connectors | 1,000+ | 200+ | None — build all |
| TCO (3 years) | High license cost | Medium license cost | Low license, high build time |
| Maintenance burden | Low (vendor-managed) | Low | High (own everything) |
| Flexibility | Medium (recipe limitations) | Medium | Maximum |
| Compliance/audit features | Built-in logging | Built-in logging | Build yourself |
| Developer skill requirement | Low-code + some code | Low-code | Full code |
| Time to first integration | Days | Days | Weeks |
| Vendor lock-in risk | High | High | Low |

**Framework for the decision:**
1. Volume and complexity: high volume, many integrations → iPaaS is better value; few complex custom integrations → custom code
2. Team skill profile: low-code team → Workato/Celigo; strong engineering team → more flexibility
3. Pre-IPO compliance: iPaaS platforms have built-in audit logging and SOC 2 compliance certifications; custom code requires you to build all of that
4. Palantir Foundry is already chosen — evaluate whether Foundry can handle the iPaaS use cases before adding another tool

**Recommendation structure:** "My recommendation is [X] because [3 key reasons]. The main trade-off is [Y]. I would validate with a 2-week PoC on [specific integration]."

---

### 8.5 System Design & Architecture Questions

---

**Q20: Design the integration architecture for Nscale's core application landscape. Assume 20+ SaaS tools, 1,000 employees, and pre-IPO compliance requirements.**

*Strong answer covers:*

**Core Principles:**
1. Hub-and-spoke model with Palantir Foundry as the integration hub (aligns with JD)
2. HRIS (Workday) as the system of record for employees
3. CRM (Salesforce) as the system of record for customers
4. ERP (NetSuite) as the system of record for financial data
5. Okta as the identity hub — all access flows through Okta

**Architecture Diagram (text form):**
```
                    ┌─────────────────────┐
                    │   Palantir Foundry  │
                    │   (Integration Hub) │
                    └──────┬──────────────┘
                           │
    ┌──────────────────────┼────────────────────────────────────┐
    │                      │                                     │
┌───┴───┐           ┌──────┴──────┐                      ┌──────┴──────┐
│ HRIS  │           │    Okta     │                      │   NetSuite  │
│Workday│◄─────────►│(Identity Hub│◄──SCIM──►[All Apps]  │   (ERP)     │
└───┬───┘           └─────────────┘                      └──────┬──────┘
    │                                                           │
    ├──► ATS (Greenhouse) ──► New Hire Data                    │
    ├──► Benefits Platform                                      │
    └──► Payroll                                    ┌──────────┴──────┐
                                                    │   Salesforce    │
                                                    │   (CRM/Revenue) │
                                                    └─────────────────┘
```

**Compliance Controls:**
- All data flows logged in Foundry with timestamp, source, destination, and transform applied
- Okta serves as the single access control plane — no direct provisioning to apps outside Okta
- Change management: all integration changes via Git + code review before deployment
- Daily reconciliation jobs flag data discrepancies

**What NOT to build:**
- Direct point-to-point connections between apps (e.g., Greenhouse directly pushing to NetSuite)
- Manual CSV exports/imports as integration mechanisms

---

**Q21: How would you design an integration monitoring and alerting system for 50+ production integrations?**

*Strong answer:*

**What to monitor:**
1. Integration execution health: success/failure rate per integration
2. Data volume anomalies: sudden drop in records synced (possible silent failure)
3. Latency: P50, P95 execution times — spikes indicate upstream issues
4. Error rate by error type: 4xx vs 5xx vs timeout
5. Queue depth: events backing up indicate processing bottleneck
6. Dependency health: API endpoint availability for each downstream system
7. Data quality metrics: null rates, schema violations, duplicate rates post-sync

**Alerting tiers:**
- **P1 (Page immediately):** JML leaver flow failed, financial sync failed on month-end, any integration >4 hours behind
- **P2 (Slack alert, business hours):** Non-critical sync failure, elevated error rate
- **P3 (Dashboard/daily digest):** Data quality degradation, unusual volume pattern

**Tools:**
- Integration platform native dashboards (Foundry, Workato)
- Custom dashboards in Grafana or Datadog pulling integration metrics via API
- Pagerduty for P1 escalation

---

### 8.6 Behavioral & STAR Questions

---

**Q22: Tell me about a time you had to push back on a business requirement because it would create a compliance or security risk.**

*Why asked:* Tests judgment, communication, and alignment with Nscale's IPO-readiness needs.

*Strong answer includes:*
- Specific compliance risk identified (e.g., "HR wanted to manually export employee CSV to provision accounts — this would bypass access controls and be impossible to audit for SOX")
- How you explained the risk in business terms (not just technical)
- Alternative solution you proposed
- How you got alignment
- Outcome (process improved, not just "they accepted it")

---

**Q23: Describe a situation where you had to learn a new integration platform quickly to deliver a project.**

*Strong answer includes:*
- Context and timeline pressure
- Specific steps you took (documentation, vendor training, PoC build, paired with expert)
- What you shipped and the outcome
- What you would do differently with more time

---

**Q24: Tell me about a time you identified and fixed a systemic data quality problem across multiple systems.**

*Strong answer includes:*
- How you identified the problem (audit? complaint? your own monitoring?)
- How you traced the root cause across multiple systems
- The fix you designed (not just a one-off patch — a systemic change)
- How you involved the data owners
- Ongoing monitoring put in place

---

**Q25: Give me an example of when you balanced speed of delivery with long-term technical quality.**

*Why asked:* Pre-IPO environment often has tension between moving fast and building correctly.

*Strong answer:*
- Acknowledge the tension is real and healthy
- Describe a specific decision: "We needed an HR-to-Slack integration in 2 days for a company-wide announcement. I built a targeted, narrow integration with hardcoded employee filters — it was not the scalable solution. I documented the shortcuts taken, added a tech debt ticket with estimated effort to generalize it, and revisited it 3 weeks later when there was capacity."
- Key: you made the conscious trade-off, documented it, and closed it — not just left it as permanent debt

---

### 8.7 Leadership & Stakeholder Questions

---

**Q26: How do you get alignment from a business stakeholder who wants a quick-and-dirty integration that will create long-term problems?**

*Strong answer:*
1. Understand their underlying need first — what outcome are they trying to achieve?
2. Acknowledge the urgency — don't dismiss the business pressure
3. Show the cost of the "quick" solution concretely — "this will create 2 hours of manual reconciliation every week and will fail SOX audit"
4. Offer a tiered option: "Here's a compliant version that takes 3 days instead of 1"
5. Document the decision regardless — if they override your recommendation, have a written record

---

**Q27: You are onboarding as the first dedicated integration engineer. How do you approach the first 90 days?**

*Strong answer — structured 30/60/90 plan:*

**First 30 days (Discovery):**
- Map the full application estate — every SaaS tool, every integration that exists
- Identify existing integrations: how they were built, by whom, on what platform
- Catalogue data flows, authentication methods, and dependencies
- Identify top 3 risks: integrations that are fragile, undocumented, or non-compliant
- Meet with stakeholders: HR, Finance, IT Security, Engineering, Procurement

**30–60 days (Quick Wins):**
- Fix the highest-risk integration issue identified
- Document one complete integration end-to-end (create the template for others)
- Establish the integration platform choice and set up development environment
- Define integration standards (naming, error handling, logging patterns)
- Deliver one new integration to demonstrate value

**60–90 days (Foundation):**
- Design the JML workflow architecture
- Define data governance model (system of record per entity)
- Build integration monitoring dashboard
- Create integration runbook template
- Present integration roadmap to Senior Director

---

## 9. Mock Interview Test (4 Rounds)

---

### Round 1: HR/Recruiter Screening

**Duration:** 30 minutes | **Pass Benchmark:** 32/40

---

| # | Question | Expected Answer Points | Score |
|---|----------|----------------------|-------|
| 1 | Tell me about yourself and your integration engineering background | Named systems, platforms, 1–2 outcomes, connection to Nscale's context | /5 |
| 2 | What integration platforms have you used? Describe depth of experience | At least one platform named with specifics; not just "I've heard of Workato" | /5 |
| 3 | What does JML stand for and what does it mean in an enterprise context? | Joiner/Mover/Leaver; user lifecycle automation; access provisioning/deprovisioning | /5 |
| 4 | Have you worked in a pre-IPO or high-growth company before? | Context awareness; understanding of compliance acceleration; scale challenges | /5 |
| 5 | What is your experience with identity providers like Okta or Azure AD? | SCIM provisioning, group-based access, JML integration, SSO | /5 |
| 6 | What is your experience with compliance frameworks like SOX or SOC 2? | Relevant if yes; if no, awareness + willingness to learn is acceptable | /5 |
| 7 | Why Nscale specifically? | Pre-IPO scale, integration complexity, GPU/AI industry growth | /5 |
| 8 | What are your salary expectations and availability? | Clear and realistic | /5 |

**Interviewer Criteria:** Communication clarity, baseline technical vocabulary, relevant experience, motivation fit

---

### Round 2: Core Technical Interview

**Duration:** 60–75 minutes | **Pass Benchmark:** 52/65

---

| # | Question | Expected Answer Points | Score |
|---|----------|----------------------|-------|
| 1 | Explain the difference between SCIM and just calling an app's API directly for provisioning. When is SCIM better? | Standardized schema, automatic deprovisioning, IdP-managed lifecycle vs. custom code | /10 |
| 2 | Walk me through how OAuth 2.0 Client Credentials flow works. Write pseudocode for a token refresh handler. | Correct flow description + working retry/refresh logic in code | /10 |
| 3 | Write SQL to find all active Okta users whose Workday status is "terminated" | Correct JOIN, LOWER() for email, correct filter logic (see Q14) | /10 |
| 4 | You're building a webhook receiver. How do you ensure no events are lost if your processing service goes down for 10 minutes? | Queue-based architecture, webhook acknowledgement, replay mechanism | /10 |
| 5 | What are the trade-offs between using an iPaaS like Workato vs. writing custom Python for integrations? | TCO, speed, flexibility, maintenance, compliance features — must cover multiple dimensions | /10 |
| 6 | How do you handle API rate limits in a high-volume sync? | Bulk API, throttling, off-peak scheduling, backoff, caching, webhook vs. polling | /5 |
| 7 | What is idempotency and why does it matter for integration retries? | Definition + concrete example + consequence of not having it (duplicates) | /10 |

**Interviewer Criteria:** Technical depth, problem decomposition, real-world awareness, code quality (for SQL/pseudocode)

---

### Round 3: Scenario / Architecture Round

**Duration:** 60–75 minutes | **Pass Benchmark:** 52/65

---

| # | Question | Expected Answer Points | Score |
|---|----------|----------------------|-------|
| 1 | Design the complete Leaver workflow. A Workday termination must result in full deprovisioning within 4 hours. Cover all steps, failure handling, and audit trail. | All 5+ steps, error handling per step, audit logging, SLA monitoring, reconciliation job | /15 |
| 2 | We have 25 SaaS tools and currently use point-to-point integrations. We're moving to Palantir Foundry as a hub. How do you approach the migration without breaking existing integrations? | Discovery, inventory, prioritization, phased migration, rollback plan, parallel running | /15 |
| 3 | Salesforce and NetSuite both have customer contract data and they're out of sync. Finance and Sales are arguing about which is correct. How do you resolve this technically and organizationally? | MDM, system of record designation, business owner alignment, reconciliation job, ongoing governance | /10 |
| 4 | You're tasked with integrating an acquired company's 15 SaaS tools into Nscale's estate within 60 days. Walk me through your approach. | Discovery → mapping → prioritization → JML migration first → application consolidation → data migration | /15 |
| 5 | How do you design integration monitoring for 50+ production integrations so the team knows about failures before the business does? | Tiered alerting, metrics per integration, anomaly detection on volume, P1/P2/P3 escalation | /10 |

**Interviewer Criteria:** Architecture quality, completeness of thinking, operational awareness, compliance integration, realistic delivery approach

---

### Round 4: Behavioral & Leadership Round

**Duration:** 45–60 minutes | **Pass Benchmark:** 36/45

---

| # | Question | Expected Answer Points | Score |
|---|----------|----------------------|-------|
| 1 | Tell me about the most complex integration project you've led. What was your role, what broke, and what did you learn? | Ownership, technical depth, learning orientation, honest reflection | /10 |
| 2 | Describe a time you disagreed with a technical decision made by a more senior engineer. How did you handle it? | Respectful challenge, data-backed argument, outcome, relationship preserved | /10 |
| 3 | Give an example of when you improved a process to eliminate a manual workaround that was creating compliance risk. | Process improvement, stakeholder buy-in, measurable outcome, ongoing controls | /10 |
| 4 | How do you balance being a hands-on individual contributor with also influencing architectural standards for the team? | Demonstrates both technical depth and systems-level thinking; documentation, ADRs, mentoring | /5 |
| 5 | What does "ownership" mean to you in an integration engineering context? | Monitoring, on-call, documentation, proactive improvement — not just build and hand off | /10 |

**Interviewer Criteria:** Self-awareness, communication, ownership culture fit, influence without authority, alignment with Nscale's "relentless innovation and accountability" values

---

### Overall Score Summary

| Round | Total | Pass Mark | Weight |
|-------|-------|-----------|--------|
| Round 1 (Screening) | 40 | 32 (80%) | Gate |
| Round 2 (Technical) | 65 | 52 (80%) | 35% |
| Round 3 (Scenario/Architecture) | 65 | 52 (80%) | 40% |
| Round 4 (Behavioral) | 45 | 36 (80%) | 25% |

**Overall pass benchmark:** Score ≥ 80% across weighted Rounds 2–4, with no round below 70%.

---

## 10. Practical Hands-On Assessment

---

### Assessment 1: Integration Design Challenge (90 minutes)

**Prompt:**

> Nscale is onboarding 10 new engineers next Monday. Today is Thursday. The process currently involves:
> - HR manually creates their profiles in Workday
> - IT manually creates Okta accounts and assigns groups
> - Engineering manually adds them to GitHub and AWS
> - IT manually orders laptops via the vendor portal
>
> Your job is to design an automated JML Joiner workflow to replace this. The workflow should be triggered from Greenhouse (ATS) upon offer acceptance with a start date confirmed.
>
> Deliverables:
> 1. A written design document (integration flow, systems, data mapping, error handling)
> 2. A Python pseudocode or actual implementation of the trigger-to-HRIS step
> 3. A list of compliance controls you would add for SOX readiness
> 4. A monitoring and alerting plan for this workflow

---

**Expected Output — Sample Excellent Response:**

**Design Document:**

```
TRIGGER: Greenhouse webhook fires on candidate status = "Hired"
         Payload: {candidate_id, name, email, start_date, department, manager_email, role_title}

STEP 1: Workday Employee Pre-Hire Record Creation
  - POST /workers (Workday REST API)
  - Map fields: firstName, lastName, workEmail, startDate, jobProfile (from department → jobProfile mapping table)
  - Store Workday worker ID for downstream steps
  - Validation: check email uniqueness, required fields, start_date ≥ today+1
  - Error handling: alert HR Ops channel on failure; do not proceed to Step 2

STEP 2: Okta User Creation (trigger: 5 days before start date)
  - POST /api/v1/users (Okta API, Client Credentials)
  - Attributes: login=workEmail, firstName, lastName, department, managerId (from Okta)
  - Assign groups: "all-employees", "engineering-team", "github-access", "aws-developer"
  - Okta SCIM will propagate to GitHub, Slack, JIRA automatically
  - Validation: verify Okta user created with correct group memberships

STEP 3: AWS IAM / GitHub Access (via Okta SCIM)
  - Okta group push to GitHub (SSO group sync)
  - Okta group push to AWS IAM Identity Center
  - If apps don't support SCIM: trigger API calls to GitHub (POST /orgs/{org}/invitations) and AWS

STEP 4: Hardware Request
  - Trigger on: Workday record created with location and start_date
  - POST /tickets (ServiceNow or IT ticketing API)
  - Payload: employee name, email, start_date, location, standard_equipment_package=engineering
  - SLA: ticket created ≥ 7 days before start for domestic, 14 days for international

STEP 5: Completion Notification
  - Send summary email to IT, HR, and hiring manager
  - Confirm all steps completed with timestamps

DATA MAPPING TABLE:
| Greenhouse Field     | Workday Field         | Transformation                    |
|---------------------|-----------------------|-----------------------------------|
| candidate.first_name | worker.legalFirstName | None                              |
| candidate.last_name  | worker.legalLastName  | None                              |
| candidate.email      | worker.workEmail      | Validate email format             |
| offer.start_date     | worker.startDate      | ISO 8601 format                   |
| job.department       | worker.jobProfile     | Lookup: dept_name → job_profile_id|
| hiring_manager.email | worker.managerId      | Lookup: email → Workday worker ID |
```

**Python Implementation — Greenhouse Webhook to Workday:**

```python
import hmac
import hashlib
import json
import logging
import time
import requests
from flask import Flask, request, jsonify

app = Flask(__name__)

GREENHOUSE_WEBHOOK_SECRET = "your_webhook_secret"
WORKDAY_API_BASE = "https://wd3.myworkday.com/ccx/service/your_tenant"
WORKDAY_TOKEN_URL = "https://auth.workday.com/token"
WORKDAY_CLIENT_ID = "your_client_id"
WORKDAY_CLIENT_SECRET = "your_client_secret"

logger = logging.getLogger(__name__)

DEPARTMENT_TO_JOB_PROFILE = {
    "Engineering": "job_profile_123",
    "Finance": "job_profile_456",
    "Sales": "job_profile_789",
}

def verify_greenhouse_signature(payload_body: bytes, signature: str) -> bool:
    expected = hmac.new(
        GREENHOUSE_WEBHOOK_SECRET.encode(),
        payload_body,
        hashlib.sha256
    ).hexdigest()
    return hmac.compare_digest(expected, signature)

def get_workday_access_token() -> str:
    response = requests.post(
        WORKDAY_TOKEN_URL,
        data={
            "grant_type": "client_credentials",
            "client_id": WORKDAY_CLIENT_ID,
            "client_secret": WORKDAY_CLIENT_SECRET,
        }
    )
    response.raise_for_status()
    return response.json()["access_token"]

def create_workday_prehire(employee_data: dict, max_retries: int = 3) -> dict:
    token = get_workday_access_token()
    headers = {"Authorization": f"Bearer {token}", "Content-Type": "application/json"}
    
    job_profile_id = DEPARTMENT_TO_JOB_PROFILE.get(employee_data["department"])
    if not job_profile_id:
        raise ValueError(f"Unknown department: {employee_data['department']}")
    
    payload = {
        "worker": {
            "legalFirstName": employee_data["first_name"],
            "legalLastName": employee_data["last_name"],
            "workEmail": employee_data["email"],
            "startDate": employee_data["start_date"],
            "jobProfile": {"id": job_profile_id},
        }
    }
    
    for attempt in range(max_retries):
        try:
            response = requests.post(
                f"{WORKDAY_API_BASE}/workers",
                headers=headers,
                json=payload
            )
            if response.status_code == 201:
                logger.info(f"Workday pre-hire created for {employee_data['email']}")
                return response.json()
            elif response.status_code in (429, 503):
                wait = 2 ** attempt
                logger.warning(f"Workday API rate limited, retrying in {wait}s")
                time.sleep(wait)
            elif response.status_code == 409:
                logger.warning(f"Duplicate record detected for {employee_data['email']}")
                raise ValueError("Employee already exists in Workday")
            else:
                response.raise_for_status()
        except requests.exceptions.ConnectionError:
            if attempt == max_retries - 1:
                raise
            time.sleep(2 ** attempt)
    
    raise Exception(f"Workday creation failed after {max_retries} retries")

@app.route("/webhooks/greenhouse/hired", methods=["POST"])
def handle_greenhouse_hire():
    # Return 200 immediately to prevent Greenhouse from retrying
    signature = request.headers.get("X-Greenhouse-Signature", "")
    if not verify_greenhouse_signature(request.data, signature):
        return jsonify({"error": "Invalid signature"}), 401
    
    # Acknowledge receipt immediately
    payload = request.get_json()
    
    # Queue for async processing (simplified - in production use SQS/RabbitMQ)
    try:
        process_new_hire(payload)
    except Exception as e:
        logger.error(f"Failed to process hire for {payload.get('email')}: {e}")
        # Alert HR Ops
        send_alert(f"JML Joiner failed for {payload.get('email')}: {str(e)}")
        return jsonify({"status": "error", "message": str(e)}), 500
    
    return jsonify({"status": "accepted"}), 200

def process_new_hire(payload: dict):
    application = payload.get("application", {})
    candidate = application.get("candidate", {})
    
    employee_data = {
        "first_name": candidate["first_name"],
        "last_name": candidate["last_name"],
        "email": candidate["email_addresses"][0]["value"],
        "start_date": application.get("start_date"),
        "department": application.get("jobs", [{}])[0].get("departments", [{}])[0].get("name"),
    }
    
    workday_record = create_workday_prehire(employee_data)
    logger.info(f"Joiner flow Step 1 complete: Workday ID {workday_record['id']}")
    # Continue with Steps 2–5...

def send_alert(message: str):
    # Post to Slack #it-alerts channel via webhook
    pass

if __name__ == "__main__":
    app.run(port=8080)
```

**SOX Compliance Controls:**
1. All provisioning actions logged with actor (system), timestamp, action type, and outcome
2. No manual provisioning steps — all access granted via automated rules only
3. Access based on job role/department (RBAC), not individual request
4. Two-person integrity for privileged access (e.g., admin accounts require manual approval)
5. Reconciliation report runs daily — active users vs. active HRIS employees
6. All code changes to JML workflow go through git PR review before deployment
7. Integration logs retained for 12 months (SOX audit requirement)
8. Alert on any deprovisioning SLA breach (>4 hours for leavers)

**Monitoring & Alerting:**
- Emit metrics: `jml_joiner.step1.success`, `jml_joiner.step1.failure` per step
- P1 alert: any step fails for an employee starting within 24 hours
- P2 alert: step takes >30 minutes (SLA breach)
- Dashboard: daily view of all joiner workflows — status per step per employee
- Reconciliation check: T+1 day after start date, verify all steps completed; if not, page on-call

---

**Evaluation Rubric:**

| Dimension | 0–2 (Poor) | 3–4 (Acceptable) | 5 (Excellent) |
|-----------|-----------|-----------------|---------------|
| Integration flow completeness | Missing major steps | Core steps present, gaps in error handling | All steps, error handling, retries, validation |
| Code quality | Broken or pseudocode only | Functional but no error handling | Working, handles errors, idempotent, secure |
| Compliance thinking | Not mentioned | Mentioned but vague | Specific SOX controls wired into the design |
| Monitoring plan | Not mentioned | Generic "add logging" | Specific metrics, alert tiers, reconciliation |
| Data mapping | Assumed automatic | Partial mapping shown | Complete mapping table with transformations |

**Passing score:** 18/25

---

### Assessment 2: SQL Data Quality Scenario (30 minutes)

**Prompt:**

> You have two tables: `hris_employees` (Workday export) and `okta_users` (Okta export). Write SQL queries to answer the following:
>
> 1. Find all active Okta users who are not present in HRIS (potential orphaned accounts)
> 2. Find all active HRIS employees who are missing from Okta (potential provisioning failure)
> 3. Find HRIS employees whose email in Workday doesn't match their Okta login
> 4. Find employees where the department in HRIS doesn't match the department in Okta

```sql
-- Table schemas:
-- hris_employees: employee_id, first_name, last_name, email, department, status, start_date, termination_date
-- okta_users: okta_id, login (email), first_name, last_name, department, status, created_at, last_login

-- Q1: Active Okta users not in HRIS (orphaned accounts — compliance risk)
SELECT 
    o.okta_id,
    o.login AS okta_email,
    o.first_name,
    o.last_name,
    o.status AS okta_status,
    o.created_at
FROM okta_users o
LEFT JOIN hris_employees h ON LOWER(o.login) = LOWER(h.email)
WHERE o.status = 'ACTIVE'
  AND h.employee_id IS NULL
ORDER BY o.created_at;

-- Q2: Active HRIS employees missing from Okta (provisioning failure)
SELECT 
    h.employee_id,
    h.email AS hris_email,
    h.first_name,
    h.last_name,
    h.status AS hris_status,
    h.start_date
FROM hris_employees h
LEFT JOIN okta_users o ON LOWER(h.email) = LOWER(o.login)
WHERE h.status = 'active'
  AND h.start_date <= CURRENT_DATE
  AND o.okta_id IS NULL
ORDER BY h.start_date;

-- Q3: Email mismatch between HRIS and Okta (data quality issue)
SELECT 
    h.employee_id,
    h.email AS hris_email,
    o.login AS okta_email,
    h.first_name,
    h.last_name
FROM hris_employees h
INNER JOIN okta_users o 
    ON LOWER(h.first_name) = LOWER(o.first_name) 
    AND LOWER(h.last_name) = LOWER(o.last_name)
WHERE h.status = 'active'
  AND o.status = 'ACTIVE'
  AND LOWER(h.email) != LOWER(o.login);

-- Q4: Department mismatch (stale data, mover workflow may have failed)
SELECT 
    h.employee_id,
    h.email,
    h.department AS hris_department,
    o.department AS okta_department
FROM hris_employees h
INNER JOIN okta_users o ON LOWER(h.email) = LOWER(o.login)
WHERE h.status = 'active'
  AND o.status = 'ACTIVE'
  AND LOWER(TRIM(h.department)) != LOWER(TRIM(o.department))
ORDER BY h.email;
```

**Evaluation Rubric:** Correct JOINs (5), LOWER() for email comparison (5), correct filters on status (5), handling NULL correctly in LEFT JOIN (5), practical ordering and output (5) — Total: 25 points. Pass: 18/25.

---

## 11. Final Preparation Plan

---

### 1-Day Crash Plan (8 hours)

| Time | Topic | Activity |
|------|-------|----------|
| Hour 1–2 | JML workflow design | Read Q16, Q17 fully; sketch your own Joiner/Leaver diagram |
| Hour 3 | OAuth 2.0 + SCIM | Read Q7, Q8; be able to explain without notes |
| Hour 4 | SQL practice | Write all 4 queries from Assessment 2 from scratch |
| Hour 5 | Integration patterns | Read Q20; practice drawing hub-and-spoke architecture |
| Hour 6 | Error handling + monitoring | Read Q10, Q21 |
| Hour 7 | Behavioral answers | Prepare STAR answers for Q22, Q23, Q25 |
| Hour 8 | Mock round | Do Round 2 and Round 3 questions aloud — time yourself |

---

### 3-Day Focused Plan

| Day | Morning (3 hrs) | Afternoon (3 hrs) | Evening (1 hr) |
|-----|-----------------|-------------------|----------------|
| Day 1 | Deep dive JML (Q16, Q17, Assessment 1) | OAuth, SCIM, IAM concepts (Q7, Q8) | Read Palantir Foundry docs/overview |
| Day 2 | SQL practice (Assessment 2) + data quality (Q14, Q24) | Architecture patterns + ADRs (Q20, Q15) | Compliance concepts (SOX/SOC 2 table in §4) |
| Day 3 | Behavioral STAR answers (Q22–Q25) | Mock interview all 4 rounds out loud | Prepare 5 questions to ask the interviewer |

---

### 7-Day Full Prep Plan

| Day | Focus | Key Activities |
|-----|-------|---------------|
| Day 1 | JD deep analysis + self-gap assessment | Map your experience to each JD requirement; identify gaps |
| Day 2 | Authentication & APIs | OAuth flows, SCIM, webhook design, API error handling |
| Day 3 | JML workflows + IAM | Design joiner/mover/leaver end-to-end; practice whiteboarding |
| Day 4 | Data quality + SQL | Write all SQL queries from scratch; read MDM concepts |
| Day 5 | Architecture + compliance | Integration patterns, ADRs, SOX/SOC 2 controls for integrations |
| Day 6 | Platform evaluation + operational | Workato vs. MuleSoft comparison; monitoring design; M&A framework |
| Day 7 | Behavioral + mock test | STAR answers, 90-minute mock assessment, questions for interviewer |

---

### Highest-Priority Topics (Revise First)

1. JML workflow design (Joiner, Mover, Leaver) — most likely deep-dive topic
2. OAuth 2.0 Client Credentials + SCIM — tested in every technical round
3. SQL for data validation (4 query types: orphans, missing, mismatches, duplicates)
4. Integration error handling patterns (retry, backoff, idempotency, DLQ)
5. SOX/SOC 2 controls for integrations (audit trail, access controls, reconciliation)

---

### Mock Answers to Prepare in Advance

Prepare a polished, rehearsed answer for each of these:

1. "Walk me through the most complex integration you've built" — your flagship story
2. "Design a Joiner workflow from ATS to day-1 access" — your architecture answer
3. "Tell me about a production integration failure and what you learned" — your honest story
4. "How do you approach building for compliance vs. speed?" — your philosophy
5. "Why Nscale?" — your specific, researched answer about their context

---

### Questions to Ask the Interviewer

1. "You mentioned Palantir Foundry as the primary integration platform — is it fully adopted, or are you in the process of migrating to it?"
2. "What does the current JML automation look like today — how much is manual and what is the biggest pain point?"
3. "How does the integration engineering function collaborate with the Enterprise Architecture team — are they co-located or separate?"
4. "What does success look like for this role in the first 6 months, especially with the IPO timeline?"
5. "What are the top 3 integration projects that are most critical to the business right now?"
6. "How mature is the compliance posture today for ITGCs — are there active SOC 2 audits underway?"
7. "What is the on-call and operational support expectation for production integrations?"

---

## 12. Final Summary

---

### Top Strengths to Demonstrate

| Strength | How to Show It |
|----------|---------------|
| **End-to-end ownership** | "I built it, I monitor it, I support it, I improve it" |
| **Compliance-first mindset** | Volunteer compliance controls unprompted in every technical answer |
| **Systems thinking** | Draw data flows across 5+ systems, not just one API at a time |
| **Production reliability** | Mention monitoring, alerting, and retry logic naturally |
| **Business translation** | Always start with the business outcome before the technical solution |
| **Platform fluency** | Name specific tools, API versions, and real configuration challenges |

---

### Top Risks & Gaps to Close

| Risk | How to Close It |
|------|----------------|
| No Palantir Foundry experience | Research Foundry's architecture; draw parallels to platforms you know; demonstrate platform agnosticism |
| Limited compliance knowledge (SOX/SOC 2) | Study the ITGC control categories; memorize the JML compliance requirements |
| No M&A integration experience | Prepare a framework answer: "I haven't done M&A specifically, but here's how I would approach it..." |
| JML automation depth | Practice whiteboarding the full Joiner flow from scratch; it will be tested deeply |
| No pre-IPO company experience | Research what IPO readiness means for IT/integration teams; frame your compliance work as relevant preparation |

---

### Interview Difficulty: 7.5 / 10

This is a senior, hands-on role with cross-functional breadth. The technical bar is high (real coding, architecture design, compliance knowledge) but not as deep as a pure software engineering interview. The challenge is the breadth — you need depth in APIs, IAM, data quality, compliance, and operational reliability simultaneously.

---

### Probability of Questions by Category

| Category | Probability |
|----------|------------|
| JML workflow design | 95% |
| OAuth / SCIM / IAM concepts | 90% |
| Integration architecture (whiteboard) | 85% |
| Error handling and production reliability | 80% |
| SQL / data validation | 75% |
| Platform trade-off discussion (iPaaS) | 75% |
| Compliance (SOX/SOC 2) | 70% |
| Behavioral STAR questions | 70% |
| Monitoring and alerting design | 65% |
| M&A integration framework | 50% |
| Palantir Foundry specific | 45% |
| ADR writing / documentation | 40% |
| CI/CD for integrations | 35% |

---

*Prepared for the Systems Integration Engineer role at Nscale. Tailored to JD published 2026-05-28.*
