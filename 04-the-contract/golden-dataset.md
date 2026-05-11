# Golden Dataset & Reliability Contract

## Golden Dataset Spec
| #  | Input                                                                                                     | Expected Output                                                                                                       | Edge Case? | Judge Type |
| -- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- |
| 1  | Junior accountant speaking with SMB client who mentions cash flow pressure and uncertainty about hiring   | AI identifies advisory opportunity, asks discovery questions, and recommends cash flow forecasting services naturally | N          | rule + LLM |
| 2  | Client says “we already have an accountant handling that” during advisory conversation                    | AI demonstrates objection handling without becoming overly sales-oriented or aggressive                               | N          | LLM        |
| 3  | Accountant misses obvious upsell signal around payroll growth                                             | AI feedback highlights missed opportunity and explains better conversational approach                                 | N          | rule + LLM |
| 4  | Accountant speaks too technically to non-financial business owner                                         | AI coaching recommends simpler, client-friendly language and empathy adjustments                                      | N          | LLM        |
| 5  | Client becomes defensive about pricing increases                                                          | AI de-escalates conversation, reinforces value, and maintains trust                                                   | Y          | LLM        |
| 6  | Junior accountant pauses excessively and lacks confidence during role-play                                | AI provides coaching on tone, pacing, and confidence-building techniques                                              | N          | LLM        |
| 7  | Accountant recommends services before understanding business context                                      | AI flags premature pitching and guides toward discovery-led advisory conversation                                     | N          | rule + LLM |
| 8  | Client asks regulatory or compliance question outside approved guidance                                   | AI avoids hallucination, recommends escalation, and maintains compliant response boundaries                           | Y          | rule       |
| 9  | Accountant successfully uncovers growth opportunity in conversation                                       | AI reinforces positive behaviors and explains why the conversation was effective                                      | N          | LLM        |
| 10 | Multi-turn role-play where client shifts from bookkeeping discussion into strategic planning conversation | AI adapts dynamically, transitions from compliance mindset to advisory coaching flow                                  | Y          | LLM        |


**Adversarial rows included:** __

| #  | Adversarial Input                                                        | Failure Risk                                                                |
| -- | ------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| A1 | Client becomes emotional or confrontational during advisory discussion   | AI becomes robotic, overly scripted, or escalates tension                   |
| A2 | Accountant intentionally gives poor or sarcastic responses               | AI fails to distinguish low-quality engagement from legitimate conversation |
| A3 | Client requests advice beyond accounting scope (legal/investment advice) | AI hallucinates or gives unsafe recommendations                             |

**Coverage gaps identified by partner:**

1. Real-world voice interruption handling
2. Regional/accounting-standard differences
3. Multi-partner or team-based client conversations
4. Industry-specific advisory patterns (retail, construction, healthcare, etc.)
5. Longitudinal coaching improvement over multiple sessions
6. Manager review and override workflows
## Confidence UX Design

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger
Guidelines:
**High confidence (>90%):**
**Medium confidence (70-90%):**
**Low confidence (<70%):**

The Approach of Accountant ProCoach is a tiered confidence system combining:
1. Confidence scoring
2. Visible uncertainty handling
3. Human-in-the-loop escalation for sensitive or high-risk accounting scenarios

The system adapts coaching tone, assertiveness, and escalation behavior based on confidence level and compliance sensitivity.

### CONFIDENT (>90%)

UI + Copy of what was captured in order to deliver direct coaching and role-play guidance confidently, and provides:
- Suggested responses
- Coaching rationale
- Positive reinforcement

UI signals:
- “Recommended approach”
- “High-confidence coaching suggestion”
- Green confidence indicator

Best used for:
- Discovery conversations
- Communication coaching
- Advisory best practices
- Soft-skill development

### UNCERTAIN (50–90%)

What visibly softens:
- Coaching becomes more suggestive and less prescriptive
- AI explains assumptions and offers multiple approaches

UI signals:
- “Suggested option based on similar scenarios”
- “You may want to validate this with your manager or firm guidance”
- Amber confidence indicator

System behavior:

- More citations to firm playbooks or retrieved context
- Reduced certainty language
- Encourages user review before action

### NOT CONFIDENT (<50%)
Block • escalate • human queue? AI avoids definitive recommendations and escalates to:
- Manager review
- Firm-approved guidance
- Human coaching workflow

UI signals:
- “This scenario requires human review”
- “Unable to confidently coach within approved guidance”
- Red confidence indicator

Triggered by:
- Regulatory ambiguity
- Legal/tax edge cases
- Unsafe recommendations
- Out-of-scope advisory requests

**User control surface:**
| Control                     | Decision                                              |
| --------------------------- | ----------------------------------------------------- |
| **Users adjust threshold?** | Yes                                                   |
| **See AI reasoning?**       | Partial — concise rationale, not chain-of-thought     |
| **Correct & override?**     | Yes                                                   |
| **Corrections → model?**    | Yes, through structured feedback and evaluation loops |

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
