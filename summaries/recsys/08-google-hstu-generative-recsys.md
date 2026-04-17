# Google DeepMind: HSTU - Trillion-Parameter Generative Recommendations

- **Source type**: Research paper
- **Company/Author**: Google DeepMind
- **Date**: February 2024
- **URL**: https://arxiv.org/abs/2402.17152
- **Domain**: Large-scale recommendation systems

## Summary

Google DeepMind's "Actions Speak Louder than Words" paper introduces HSTU (Hierarchical Sequential Transduction Units), a trillion-parameter generative model for recommendations. The key thesis is radical: replace the traditional multi-stage recsys pipeline (candidate generation -> scoring -> re-ranking) with a single large generative model that directly predicts the next item a user should see. The paper reports 1.5x improvement over Google's prior production recsys and up to 10x reduction in overall system complexity. This is analogous to how large language models replaced multi-stage NLP pipelines.

## Why it matters for career decisions

This is arguably the most important recsys paper in recent years for career planning. It signals that Google -- the largest employer of recsys engineers -- is moving toward a paradigm where recommendation systems look architecturally identical to large language models: massive transformer models trained on sequences, with the primary difference being that the "tokens" are user actions rather than words. This has profound implications: (1) the skill set for building recsys and LLMs is converging, (2) the scale of investment is at the frontier (trillion parameters), (3) the traditional multi-stage pipeline expertise may become less important over time as unified models replace it.

## Key technical themes

- Generative sequential transduction for recommendations
- Unified retrieval+ranking in a single model
- Trillion-parameter scale recommendation models
- Replacing multi-stage pipelines with end-to-end generative models
- Actions (user behavior) as the fundamental token type

## Career relevance

- **Paradigm shift**: The biggest "convergence" signal between recsys and LLMs -- same architectures, different token types
- **Scale of investment**: Trillion-parameter recsys models = same infrastructure demands as frontier LLMs
- **Career positioning**: Engineers who can work at this intersection are positioned at the frontier of both fields
- **Risk to traditional recsys**: Classical multi-stage pipeline skills may depreciate faster than expected
