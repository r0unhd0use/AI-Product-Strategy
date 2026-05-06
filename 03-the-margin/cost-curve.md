# Cost Curve & Pricing Strategy

## Packaging Decision

### Leader
AI Role-Play Coaching

“Practice real client conversations with AI.”

This is the feature they come for:

Differentiated
Demo-friendly
Emotionally compelling
Immediately understandable

This is the hoook.

### Filler
Personalized Learning & Feedback

“Tailored coaching, scoring, and improvement tracking.”

Important, valuable, increases retention:

Skill progression
Feedback summaries
Scenario recommendations
Manager insights

But probably not enough to buy standalone.

Increases stickiness + ARPU.

### Killer
Embedded Advisory Performance System

“Improves real client outcomes and advisory growth.”

This is the feature that must become indispensable:

Connects training → real-world performance
Tracks improvement over time
Reinforces advisory behaviors in workflow
Links to measurable business outcomes:
Client growth
Service adoption
Revenue lift

If firms would pay for this alone, it’s can become the killer.

## Cost Curve

| Feature                                     | Complexity | Model Tier | Cost/Req (Est.) | Volume % | Weighted |
| ------------------------------------------- | ---------- | ---------- | --------------- | -------- | -------- |
| Session summaries, scoring, recommendations | Simple     | Small      | $0.002          | 45%      | $0.0009  |
| Scenario generation, coaching feedback      | Medium     | Mid        | $0.02           | 35%      | $0.007   |
| Real-time voice role-play conversations     | Complex    | Frontier   | $0.15           | 20%      | $0.03    |

Blended Estimated AI Cost / Session
≈ $0.038 / interaction

Cost Strategy

Use frontier models only for high-value conversational moments, while routing summaries, scoring, and coaching workflows to cheaper models to maintain scalable margins.

## Cost Model
| Cost Category                      | Per-User / Month (Est.)    | Notes                                                                                                 |
| ---------------------------------- | -------------------------- | ----------------------------------------------------------------------------------------------------- |
| **Inference (primary model)**      | ~$12–18                    | Real-time voice role-play and complex coaching interactions using frontier models                     |
| **Inference (cascading / triage)** | ~$3–5                      | Summaries, scoring, tagging, recommendations, and lightweight coaching tasks routed to smaller models |
| **Infrastructure**                 | ~$2–4                      | Hosting, orchestration, APIs, session management, monitoring, and workflow services                   |
| **Data / storage**                 | ~$1–2                      | Conversation history, analytics, transcripts, embeddings, and user profiles                           |
| **Human-in-the-loop**              | ~$3–6                      | Expert review, scenario refinement, QA, evaluation, and coaching calibration                          |
| **Total AI COGS**                  | **~$21–35 / user / month** | Early-stage estimate; expected to improve significantly with routing optimization                     |


## Cascading Strategy

### Triage model:

Small / mid-tier model for:

- Summaries
- Skill scoring
- Classification
- Recommendations
- Session analytics

### Frontier LLM for:

- Real-time voice role-play
- Complex advisory simulations
- Dynamic objection handling
- High-emotion conversational coaching

### Routing rule:

Only escalate to frontier models when:

- Real-time conversation quality matters
- High reasoning complexity is required
- User interaction directly impacts perceived coaching realism

All structured, repetitive, or post-session workflows default to cheaper models.

Expected cascade ratio:

- Small models: 60–70%
- Mid models: 20–30%
- Frontier models: 10–15%

Goal: reserve expensive intelligence for moments users truly feel and value.
<!-- Cheap model → frontier model routing logic -->

## Pricing Model

### Current pricing:

Prototype / pilot stage (not commercially packaged yet)

### Proposed AI pricing:

$79–149 per accountant / month depending on:

- Usage volume
- Voice interaction limits
- Manager analytics
- Team coaching features

Enterprise pricing for firms based on seat tiers and advisory enablement packages.

### Model:

Hybrid (seat-based + usage-aware)

### Primary pricing:

- Per accountant seat

Secondary controls:
- Usage thresholds for high-volume voice simulations
- Enterprise tiering for manager insights and analytics

Goal: align pricing to workforce enablement, not token consumption.


## Stress Tests
| Scenario                             | Impact on Margin                                                                | Response                                                                                                                                 |
| ------------------------------------ | ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Inference costs 3x**               | High impact due to voice + frontier model dependency                            | Increase cascading to cheaper models, reduce frontier usage, optimize session length, introduce usage caps on premium voice interactions |
| **Heaviest segment doubles**         | Moderate margin compression from power users consuming disproportionate compute | Introduce tiered pricing, fair-use limits, or premium “unlimited coaching” plans                                                         |
| **Model provider raises prices 50%** | Significant short-term pressure due to provider concentration risk              | Switch to multi-model routing, renegotiate vendor mix, shift more workflows to smaller/open-source models                                |

### Strategic Pricing Insight

The long-term opportunity is to price AccountantPro Coach as:  an AI workforce capability layer
not a chatbot subscription

That’s what supports premium seat pricing and stronger margins over time.
## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

### Before (traditional SaaS)
Current pricing:

- Per-seat software subscription with predictable fixed pricing and minimal usage-based variability.
- Current gross margin:
- Typically high-margin SaaS economics (~75–85%) driven by low incremental serving costs.
- Value framed as: Static training, enablement, and learning content designed to improve accountant knowledge and professional development.

**After (AI-enabled):**
Proposed pricing:

- $79–149 per accountant / month using a hybrid seat-based + usage-aware pricing model.
- AI COGS per user/month:
- ~$21–35 per user / month.

Expected gross margin:
- ~60–75% depending on voice usage, model routing efficiency, and enterprise deployment scale.

Value framed as: An AI-powered advisory coaching system that improves real client conversations, accelerates accountant development, and increases client value through personalized role-play, coaching, and performance feedback.

**Net margin shift:**
- Margin moves from ~80% to ~65%.
Why the margin changes:
- Margins compress because inference costs, voice interactions, orchestration, and evaluation infrastructure introduce variable AI-driven COGS that traditional SaaS products do not carry.
- The largest cost drivers are frontier-model voice simulations and real-time coaching workflows.
- Margin protection depends on an effective cascading strategy that routes most interactions to smaller, lower-cost models while reserving frontier models for high-value conversational moments.

Unlike traditional SaaS, where incremental serving costs are near-zero, AccountantPro Coach behaves more like a scalable digital workforce capability where compute cost scales with engagement and usage depth. The tradeoff is lower gross margin in exchange for materially higher product value, stronger workflow embedding, and increased pricing power tied directly to user performance outcomes.
