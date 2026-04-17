# Meta GEM: Generative Ads Foundation Model

- **Source:** Meta | https://ai.meta.com/research/publications/gem-ads-foundation-model/
- **Date:** 2025-11-10
- **Domain:** ads
- **Stage:** production

## Summary

GEM (Generative Ads Model) is Meta's largest ads foundation model, built at LLM scale to serve as a unified cross-platform ranking system for both Facebook and Instagram. It represents a fundamental architectural shift: rather than maintaining separate models per surface and objective, GEM consolidates ads ranking into a single foundation model that generalizes across platforms, ad formats, and optimization goals.

The model introduces several innovations to make foundation-model-scale training and serving feasible for ads. InterFormer attention separates processing of sequence features (user behavior histories) from non-sequence features (contextual signals), dramatically reducing computational cost. A multi-domain learning framework allows the model to share representations across Facebook and Instagram while preserving surface-specific behavior. A knowledge distillation framework transfers GEM's capabilities into smaller serving models at 2x the effectiveness of prior distillation approaches.

Training infrastructure pushes the boundaries of what Meta's ads systems have historically handled: a 23x increase in training FLOPS over prior models, enabled by HSDP (Hybrid Sharded Data Parallelism) for dense components, 2D parallelism for sparse embeddings, custom GPU kernels, and PyTorch 2.0 graph compilation that achieves 7x faster compilation times.

## Key Contributions

- Unified cross-platform ads ranking model at LLM scale spanning Facebook and Instagram
- InterFormer attention architecture that separately processes sequence and non-sequence features for computational efficiency
- Multi-domain learning framework enabling cross-platform knowledge sharing
- Knowledge distillation framework achieving 2x effectiveness over prior methods
- Training infrastructure innovations: HSDP, 2D parallelism for sparse embeddings, custom GPU kernels, PyTorch 2.0 graph compilation

## Results / Metrics

- 5% lift in Instagram ad conversions
- 3% lift in Facebook Feed ad performance
- 4x more efficient than prior model architectures
- 23x increase in training FLOPS over previous generation
- 7x faster compilation via PyTorch 2.0 graph compilation

## Methods / Architecture Notes

- InterFormer: decouples attention over sequence features (user event histories) from non-sequence features (context, ad metadata), reducing quadratic attention cost
- HSDP (Hybrid Sharded Data Parallelism) for dense model components across training clusters
- 2D parallelism strategy for sparse embedding tables
- Custom GPU kernels for training-critical operations
- PyTorch 2.0 graph compilation integration for end-to-end optimization
- Knowledge distillation pipeline to compress GEM into latency-constrained serving models

## Tradeoffs / Constraints

- Foundation model scale introduces significant training cost (23x FLOPS increase) requiring substantial GPU infrastructure investment
- Unified model across surfaces means surface-specific regressions must be carefully monitored and mitigated
- Knowledge distillation is required for serving — the full model cannot be served directly at production latency targets
- InterFormer's separation of sequence/non-sequence processing trades some cross-feature interaction richness for computational efficiency

## Why It Matters (Career Perspective)

GEM is the clearest signal yet that ads ML has become foundation model work. The model is built at LLM scale, uses transformer architectures, requires distributed training infrastructure (HSDP, model parallelism), and relies on the same knowledge distillation techniques used in LLM deployment. An engineer building GEM is doing substantively the same work as an engineer building a large language model — the difference is the application domain, not the skill set.

This has direct career implications: ads ML roles at Meta (and companies following this trajectory) now require and develop the exact skills that are most valued across the industry — large-scale distributed training, transformer architecture design, efficient inference, and model compression. Working on ads foundation models is no longer a narrowly specialized career path; it is mainstream ML engineering at the frontier.
