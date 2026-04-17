# Sequence Learning for Personalized Ads

- **Source:** Meta | https://ai.meta.com/research/publications/sequence-learning-personalized-ads/
- **Date:** 2024-11-19
- **Domain:** ads
- **Stage:** production

## Summary

This work describes Meta's paradigm shift from hand-crafted feature engineering to sequential user event modeling for ads personalization. Rather than manually designing features that summarize user behavior (e.g., "number of clicks in the last 7 days"), the system directly models the raw sequence of user events using transformer attention, allowing the model to learn which behavioral patterns are predictive of ad engagement.

The core technical innovation is Event-Based Features (EBFs), a standardized representation that converts heterogeneous user interactions (clicks, views, purchases, searches across different surfaces) into a uniform format suitable for sequence modeling. On top of this representation, the system applies transformer attention to learn temporal and contextual patterns in user behavior. A key infrastructure contribution is Jagged Flash Attention, a GPU kernel optimization that efficiently handles variable-length user sequences — different users have vastly different activity histories, and naive padding wastes significant compute.

The parallel to NLP is direct and intentional: user events are treated as tokens, the event sequence is the "document," and transformer attention learns contextual relationships between events just as it learns relationships between words. This is not a loose analogy — it is the same architecture, adapted for a different token vocabulary.

## Key Contributions

- Paradigm shift from hand-crafted feature engineering to sequential user event modeling for ads
- Event-Based Features (EBFs): standardized representation converting heterogeneous user interactions into a uniform sequence format
- Jagged Flash Attention: GPU kernel optimization for efficient attention over variable-length user event sequences
- Demonstration that NLP-style sequence modeling directly improves ads personalization

## Results / Metrics

- 2-4% more conversions on select audience segments
- Replacement of hand-crafted features with learned sequential representations
- GPU kernel efficiency gains from Jagged Flash Attention on variable-length sequences

## Methods / Architecture Notes

- Event-Based Features (EBFs): each user event (click, view, purchase, search) is encoded into a standardized representation regardless of event type or originating surface
- Transformer attention applied over user event sequences to learn temporal and contextual behavioral patterns
- Jagged Flash Attention: variant of Flash Attention optimized for variable-length sequences without requiring padding to a fixed maximum length
- Custom GPU kernel implementation for Jagged Flash Attention to maximize hardware utilization
- Sequential modeling replaces or augments hand-crafted aggregation features (counts, recency, frequency)

## Tradeoffs / Constraints

- Sequential modeling requires storing and processing full user event histories, significantly increasing data and compute requirements compared to aggregated features
- Variable-length sequences create serving challenges — Jagged Flash Attention addresses this but adds kernel complexity
- 2-4% conversion improvement on select segments suggests the approach is not uniformly beneficial across all user populations
- Transition from hand-crafted features to learned representations reduces interpretability of what the model is learning from user behavior

## Why It Matters (Career Perspective)

This work makes explicit what has been implicit in the ads ML trajectory: ads personalization is now an NLP problem with a different vocabulary. User events are tokens. Behavior sequences are documents. Transformer attention learns context. The technical skills required to build this system — sequence modeling, attention mechanisms, custom GPU kernels for efficient attention, handling variable-length inputs — are identical to the skills required for language model work.

For career planning, this convergence means that experience in ads sequence modeling is directly transferable to NLP and vice versa. An engineer who builds Jagged Flash Attention for user event sequences can build Flash Attention variants for language models. The domain-specific knowledge (what events to model, how to encode them) is relatively thin compared to the shared technical foundation. This is strong evidence that ads ML is not a career silo — it is a domain application of the same core ML engineering skills that power the most sought-after roles in the industry.
