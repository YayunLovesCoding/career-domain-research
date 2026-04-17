# Epoch AI — Trends in Machine Learning Compute

- **URL**: https://epochai.org/trends-in-machine-learning-compute
- **Date**: 2024-2025 (ongoing research)
- **Company/Author**: Epoch AI (research organization tracking AI trends)
- **Source type**: Report / Research
- **Domain**: LLM

## Summary

Epoch AI maintains one of the most rigorous empirical analyses of how ML compute is evolving. Their key findings relevant to career planning:

1. **Training compute is growing 4-5x per year** for frontier models. GPT-4 used roughly 100x more compute than GPT-3. This exponential growth shows no signs of stopping as of early 2025.
2. **The doubling time** for training compute at the frontier is approximately 6 months — much faster than Moore's Law.
3. **Inference compute is growing even faster** than training compute as models are deployed to hundreds of millions of users. The inference cost of serving ChatGPT, Claude, etc. at scale is a massive engineering challenge.
4. **Hardware is not keeping pace**: GPU performance improvements (~2x every 2-3 years) cannot match the 4-5x/year growth in compute demand. The gap must be closed by systems engineering, algorithmic efficiency, and architectural innovation.
5. **Scaling laws continue to hold**: More compute reliably produces better models, which justifies continued investment.

## Why it matters for career decisions

This is the strongest quantitative argument that **LLM engineering will not be commoditized anytime soon**. The key insight:

The gap between compute demand (4-5x/year) and hardware improvement (~2x/2-3years) means that **engineering talent is the bottleneck**. Every generation of models requires not just more GPUs, but more clever engineering to make training and inference feasible. This creates sustained demand for:

- **Distributed systems engineers**: Training across thousands of GPUs requires sophisticated parallelism (tensor, pipeline, data, expert parallelism)
- **Inference optimization engineers**: Serving models efficiently (quantization, speculative decoding, KV cache optimization, batching strategies)
- **ML systems engineers**: Bridging the gap between algorithmic ideas and practical training runs

These are exactly the kinds of skills that an ML engineer from ads (who deals with large-scale serving, optimization under latency constraints, and systems-level thinking) would bring to LLM engineering.

## Key metrics
- Training compute growing 4-5x per year at the frontier
- ~6 month doubling time for frontier training compute
- Inference compute growing even faster than training compute
- Hardware improvement lag: ~2x every 2-3 years (GPUs)

## Tradeoffs
- Compute trends could slow if scaling laws hit diminishing returns
- New architectures (e.g., mixture of experts, SSMs) could reduce compute needs
- The trend assumes continued massive capital investment, which Sequoia questions
