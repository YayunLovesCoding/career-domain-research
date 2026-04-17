# a16z — Who Owns the Generative AI Platform?

- **URL**: https://a16z.com/who-owns-the-generative-ai-platform/
- **Date**: January 2024
- **Company/Author**: Andreessen Horowitz (Matt Bornstein, Rajko Radovanovic)
- **Source type**: Blog / Market analysis
- **Domain**: LLM

## Summary

This influential a16z analysis maps the emerging GenAI value chain into three layers and asks where value will accrue:

1. **Infrastructure layer** (compute, cloud): Currently dominated by Nvidia, AWS, Azure, GCP. High margins, strong moats.
2. **Model layer** (foundation model providers): OpenAI, Anthropic, Google, Meta. Expensive to build, unclear if sustainable margins exist. Commoditization pressure from open-source (Llama, Mistral).
3. **Application layer** (end-user products): Where most startups are building. But thin margins — most revenue flows back to model providers as API costs. High customer acquisition cost.

The key insight for careers: **the middle layer of the stack — fine-tuning, RAG pipelines, orchestration frameworks (LangChain, etc.) — is the most vulnerable to commoditization.** As model providers improve their APIs and models get more capable, the need for complex orchestration decreases. Meanwhile, the extremes of the stack (frontier model training on one end, and deep domain application building on the other) retain the most value.

## Why it matters for career decisions

This is the single most important framework for evaluating which LLM skills will retain value. The implication is:

- **High durability**: Pretraining, inference optimization, safety research, systems engineering for model serving
- **High durability**: Deep domain application building (where you need domain expertise + ML)
- **Lower durability**: Generic prompt engineering, basic RAG implementation, LangChain/orchestration plumbing

For an ads ML engineer considering the pivot, this suggests targeting the **infrastructure/systems layer** (where ads experience with serving ML at scale transfers well) or the **deep application layer** (where ads domain expertise + LLM capability = unique value), rather than the generic "AI engineer" middle.

## Key metrics
- N/A (qualitative market analysis)

## Tradeoffs
- VC perspective may overweight startup/disruption narratives
- The "middle layer" thesis may be too pessimistic — complex enterprise deployments still need orchestration
- Analysis is from early 2024; stack is evolving rapidly
