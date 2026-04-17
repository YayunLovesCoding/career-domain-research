# Netflix: Foundation Models for Recommendations

- **Source type**: Engineering blog (Netflix Tech Blog)
- **Company/Author**: Netflix
- **Date**: October 2024
- **URL**: https://netflixtechblog.com/foundation-models-for-recommendations-3be8e5e0f743
- **Domain**: Streaming content recommendations

## Summary

Netflix is exploring foundation model pretraining as a unifying approach across all recommendation surfaces (homepage, search, play-something, etc.). Rather than building separate models per surface, they are training large transformer-based models on user interaction sequences that can be fine-tuned for specific tasks. Key benefits include improved cold-start performance for new users and new titles, and better cross-surface transfer learning. The approach treats user behavior sequences similarly to how LLMs treat token sequences.

## Why it matters for career decisions

This is one of the clearest signals that the LLM/foundation model paradigm is being directly adopted into recommendation systems. Netflix -- historically a recsys-first company -- is converging their approach with LLM-style architectures. For an ML engineer considering recsys, this means: (1) LLM skills transfer directly into recsys work, (2) recsys is not a "legacy" field but one absorbing cutting-edge techniques, (3) the line between "LLM engineer" and "recsys engineer" is blurring at top companies.

## Key technical themes

- Foundation model pretraining for user representation
- Transformer-based sequence modeling of user behavior
- Multi-task learning across recommendation surfaces
- Cold-start mitigation through pre-trained representations

## Career relevance

- **Convergence signal**: Strong evidence that recsys and LLM domains are merging
- **Skill premium**: Engineers who understand both recsys evaluation and foundation model training are rare and valuable
- **Risk mitigation**: Pivoting to recsys does NOT mean leaving the LLM wave behind
