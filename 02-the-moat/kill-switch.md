# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** |Primarily dependent on OpenAI for core LLM capabilities | HIGH | Stand up secondary provider (e.g. Anthropic) with API keys and basic parity testing|
| **Abstraction** | Partial / minimal abstraction; prompts and logic tied to one model behavior | HIGH | Wrap all LLM calls in a single service layer|
| **Routing** |No dynamic routing; single-model usage across all functions | HIGH |Enable config-based model switching (env variable or feature flag) |
| **Eval** |No formal evaluation harness; quality assessed informally | HIGH |Create lightweight eval set (10–20 scenarios) to compare outputs across models |

## Portability Score
<!-- Ready / Partial / Locked -->
2 / 5 (High dependency, low switch readiness)

You can switch—but not quickly or confidently
High reliance on one provider’s behavior and tuning

## If OpenAI doubles pricing tomorrow:
<!-- What's your 48-hour response? -->

If OpenAI doubles pricing tomorrow:
Impact: Immediate margin pressure / cost spike
Response: Reduce usage, optimize prompts, begin switching
Time to switch: ~2–4 weeks
Risk: Medium–High (commercial viability affected short-term)

## If OpenAI ships a competing product:
<!-- What's defensible that they can't replicate? -->
If OpenAI ships a competing product:
Impact: Core features (role-play + coaching) commoditized
Response: Compete on domain depth, workflow embedding, and data loops
Time to respond: Immediate (but strategic repositioning needed)
Risk: High (feature parity achieved quickly by platform)
