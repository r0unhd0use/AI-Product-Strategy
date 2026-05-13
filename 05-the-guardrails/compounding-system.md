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

simulated coaching quality

but not:

whether conversations improved actual client outcomes.
Why this matters

Without outcome linkage:

the flywheel remains shallow
coaching risks optimizing for simulation rather than performance
**Fix plan:**

Connect:

CRM signals
service adoption
client growth metrics
manager evaluations

back into coaching and evaluation loops.


## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->
Context Connectivity
Current issue

Knowledge silos exist between:

firms
industries
coaching styles
advisory maturity levels
Goal

Create a connected intelligence layer where:

successful patterns transfer across contexts
firm playbooks inform coaching dynamically
insights compound across the ecosystem without exposing sensitive data

### In Summary; 
AccountantPro Coach compounds when every conversation, correction, and outcome improves future coaching quality — not just for one user, but across the entire advisory network.

## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
