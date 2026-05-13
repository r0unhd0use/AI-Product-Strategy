# Compounding System Design

## Feedback Loops
| Loop                      | Input                                                                           | Output Compounds?                                                                           | Status             |
| ------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------ |
| **Recursive Learning**    | User role-plays, corrections, coaching feedback, manager overrides              | **Partial** — coaching quality improves as corrections and successful patterns are captured | **Active (early)** |
| **Cross-Domain Transfer** | Accounting scenarios across industries, firm styles, and advisory conversations | **Limited** — some best practices transfer, but domain learning is still siloed             | **Active (weak)**  |
| **Network Intelligence**  | Shared usage patterns, top-performing advisory conversations, benchmarking data | **No (today)** — users mostly learn in isolation without collective intelligence loops      | **Missing / weak** |

### Recursive Learning
How it compounds
Users practice conversations
AI captures:
- Corrections
- Missed opportunities
- Successful advisory behaviors

Feedback improves:
- Coaching quality
- Scenario realism
- Recommendation accuracy
- Current weakness

Most signals are still:

- session-based
- unstructured
- not fully fed back into model or evaluation loops

Next step
1. Create structured feedback pipelines:
- Correction tagging
- Outcome tracking
- Reinforcement scoring

### Cross-Domain Transfer
How it compounds

Patterns learned in one advisory context improve performance in adjacent scenarios:

- Retail → hospitality
- Payroll → cash flow advisory
- Compliance → strategic planning conversations
- Current weakness

Knowledge remains:

- scenario-specific
- lightly personalized
- weakly connected across industries and firms

Next step

Build:
- Shared advisory pattern libraries
- Industry abstraction layers
- Retrieval systems that connect similar conversational outcomes across domains
- Network Intelligence
- How it compounds

The system should learn from:

- high-performing accountants
- successful conversations
- manager corrections
- team-level trends

and improve coaching quality for all users.

Current weakness

Users currently operate in isolation:

- No shared benchmarking
- No collective learning loop
- No “best conversation patterns” network effect
  
Next step

Build:

- Team benchmarking dashboards
- Shared coaching insights
- Top-performer pattern extraction
- Organization-level advisory intelligence

**Broken loop identified by partner:**
Broken Loop (Partner Found)
Practice → feedback → no real-world outcome validation

The system currently measures:

- simulated coaching quality

but not:

- whether conversations improved actual client outcomes.

Why this matters

Without outcome linkage:

- the flywheel remains shallow
- coaching risks optimizing for simulation rather than performance

**Fix plan:**

Connect:

- CRM signals
- service adoption
- client growth metrics
- manager evaluations

back into coaching and evaluation loops.


## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->
Context Connectivity
Current issue

Knowledge silos exist between:

- firms
- industries
- coaching styles
- advisory maturity levels
- Goal

Create a connected intelligence layer where:

- successful patterns transfer across contexts
- firm playbooks inform coaching dynamically
- insights compound across the ecosystem without exposing sensitive data

### In Summary; 
AccountantPro Coach compounds when every conversation, correction, and outcome improves future coaching quality — not just for one user, but across the entire advisory network.

## Governance Policy

# **AccountantPro Coach — Governance Policy v1.0**

---

## **SCOPE**

AI features within AccountantPro Coach including:

* AI role-play conversations
* Advisory coaching recommendations
* Conversation scoring and feedback
* Personalized learning recommendations
* Voice-enabled coaching interactions
* Manager review and benchmarking workflows

Excludes:

* Final accounting, tax, legal, or financial advice generation
* Autonomous filing, compliance submission, or financial decision-making
* Internal analytics systems governed separately by firm data policies

---

## **AUTONOMY BOUNDARIES**

### **Allowed autonomous actions**

* Simulated client role-play conversations
* Coaching recommendations and feedback
* Communication and advisory skill guidance
* Scenario generation and practice exercises
* Personalized learning suggestions

### **Human approval required**

* Compliance-sensitive recommendations
* Tax or regulatory interpretation
* Escalation-related guidance
* Manager performance evaluations affecting HR decisions
* Any recommendation tied to financial commitments or client remediation

### **Never autonomous**

* Filing or submitting regulated financial documents
* Providing definitive legal, tax, or investment advice
* Overriding firm-approved policies or controls
* Acting on behalf of firms or clients in external systems
* Modifying official accounting records or financial data

---

## **ESCALATION TRIGGERS**

Escalate to human review when:

1. Confidence score <60%
2. User requests regulated accounting, legal, or tax advice
3. Prompt injection or role-override attempt detected
4. Hallucination or unsupported factual claim detected
5. Emotional distress, aggressive behavior, or client conflict escalation occurs
6. User explicitly requests human review
7. More than 3 failed conversational recovery attempts occur in one session
8. AI crosses from coaching into operational accounting recommendations

---

## **AUDIT CADENCE**

### **Weekly**

* Automated evaluation against golden dataset
* Hallucination and prompt-injection testing
* Reliability metric review:

  * Accuracy
  * Drift velocity
  * Confidence calibration
  * Voice latency

### **Monthly**

* Human review of:

  * Random coaching sessions
  * Escalated interactions
  * Compliance-sensitive scenarios
* Manager feedback audit on coaching quality

### **Quarterly**

* Full governance review with:

  * Security
  * Legal/compliance
  * Product leadership
* Red-team assessment against:

  * Prompt injection
  * Unsafe advisory behavior
  * Data leakage risks

---

## **REGULATORY EXPOSURE (EU AI ACT / GDPR / SECTOR)**

### **EU AI Act**

AccountantPro Coach is positioned as:

* professional training and coaching software, not autonomous financial decision-making infrastructure.

Primary risk areas:

* advisory recommendation interpretation
* compliance boundary confusion
* overreliance on AI-generated coaching

### **GDPR**

Controls include:

* Data minimization in prompts and transcripts
* Role-based access controls
* User correction and deletion workflows
* No training on customer-sensitive data without explicit approval
* Retention controls for voice and conversation data

### **Sector / Compliance Controls**

* Human escalation for regulated accounting scenarios
* No autonomous financial recommendations
* Audit logging for coaching outputs and escalation events
* Firm-level policy customization and approval workflows

---

# **Agent Topology**

| Agent                         | Purpose                                    | Allowed Actions                                 | Restricted Actions                         | Approval Required      |
| ----------------------------- | ------------------------------------------ | ----------------------------------------------- | ------------------------------------------ | ---------------------- |
| **Role-Play Agent**           | Simulate client conversations              | Generate conversational scenarios and responses | Provide regulated advice                   | No                     |
| **Coaching Agent**            | Evaluate and coach conversations           | Score, summarize, and recommend improvements    | Make HR/performance decisions autonomously | No                     |
| **Compliance Boundary Agent** | Detect unsafe or regulated scenarios       | Flag escalation conditions                      | Override governance rules                  | Yes (human escalation) |
| **Manager Insights Agent**    | Team-level analytics and benchmarking      | Aggregate coaching trends                       | Make autonomous personnel recommendations  | Yes                    |
| **Evaluation Agent**          | Golden dataset scoring and drift detection | Run evaluations and audits                      | Modify production prompts/models directly  | Yes                    |

---

# **Governance Principle**

AccountantPro Coach is designed to augment accountant capability — not replace professional judgment, regulated oversight, or firm governance controls.

---

# **One-line summary**

**The governance model prioritizes controlled autonomy: AI can coach and simulate independently, but regulated judgment, compliance interpretation, and operational accountability always remain human-owned.**

## Shadow AI Audit
| Tool                                          | Owner                         | Risk    | Decision          |
| --------------------------------------------- | ----------------------------- | ------- | ----------------- |
| **ChatGPT / Claude**                          | Product / prompt development  | **M**   | **Govern**        |
| **Alvio.io**                                  | Prompt development            | **M**   | **Govern**        |
| **Lovable**                                   | Prototype build               | **M**   | **Govern**        |
| **ElevenLabs**                                | Voice agent + synthetic voice | **H**   | **Govern**        |
| **Google Docs / Sheets / Slides AI features** | Product / business planning   | **L–M** | **Keep / Govern** |
| **Zapier / Make automations**                 | Workflow automation           | **M–H** | **Govern**        |

### Tools Found

6

### After Triage
#### Keep: Google Workspace AI features
#### Govern: ChatGPT / Claude, Alvio.io, Lovable, ElevenLabs, Zapier / Make
#### Kill: Any unapproved AI tool handling client data, financial records, voice recordings, or prompt/IP logic without security review

### Hidden Spend

Estimated hidden AI/tooling spend: $200–800/month, depending on seats, voice usage, prototype hosting, and automation volume.

### Key Risk

The highest-risk area is voice + client simulation data, because it may include sensitive practice scenarios, personal data, or proprietary coaching IP.

### Immediate Action

Create a simple approved-tool register covering: tool owner, data allowed, data prohibited, retention policy, and escalation contact.

