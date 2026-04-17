# Meta Andromeda: Next-Generation Ads Retrieval

- **Source:** Meta | https://ai.meta.com/blog/andromeda-ads-retrieval/
- **Date:** 2024-12-02
- **Domain:** ads
- **Stage:** production

## Summary

Andromeda is Meta's next-generation ads retrieval system, designed to process three orders of magnitude more candidates than the downstream ranking models. While ranking models (like GEM and ARM) evaluate hundreds to thousands of candidates, Andromeda operates at the retrieval stage where the candidate set is millions to billions. The system is custom-designed for the NVIDIA Grace Hopper Superchip, representing a hardware-software codesign approach where the model architecture is built around the capabilities of a specific accelerator.

The system achieves dramatic improvements across multiple dimensions: +6% recall (finding more relevant ads), +8% ads quality (better matches between users and ads), 3x queries per second, 100x feature extraction speedup, and a 10,000x increase in model capacity. These improvements come from rethinking retrieval as a GPU-first deep learning problem rather than the traditional approach of lightweight scoring models operating on pre-computed embeddings.

A distinctive feature of Andromeda is model elasticity — the ability to automatically adjust model complexity based on available resources and the estimated value of the audience being served. High-value ad impressions get more model compute; lower-value ones get a lighter-weight pass. This mirrors ARM's request-oriented computation but at the retrieval stage, where the efficiency gains from dynamic allocation are even larger due to the scale of the candidate set.

## Key Contributions

- Ads retrieval system processing 3 orders of magnitude more candidates than ranking
- Custom codesign with NVIDIA Grace Hopper Superchip architecture
- Model elasticity: automatic complexity adjustment based on resources and audience value
- GPU-first deep learning approach to retrieval, replacing lightweight scoring on pre-computed embeddings
- 10,000x model capacity increase enabling far richer retrieval representations

## Results / Metrics

- +6% recall improvement (finding more relevant ads in the candidate set)
- +8% ads quality improvement (better user-ad matching)
- 3x queries per second (serving throughput)
- 100x feature extraction speedup
- 10,000x model capacity increase over previous retrieval system

## Methods / Architecture Notes

- Custom-designed for NVIDIA Grace Hopper Superchip, leveraging unified CPU-GPU memory and high-bandwidth NVLink
- GPU-first retrieval: moves retrieval computation from CPU-based lightweight models to GPU-based deep learning models
- Model elasticity: dynamically adjusts the depth and width of model computation per request based on system load and estimated audience value
- Feature extraction pipeline redesigned for GPU execution, achieving 100x speedup
- Retrieval at scale: processes millions to billions of candidates per query

## Tradeoffs / Constraints

- Custom hardware codesign creates dependency on specific accelerator platforms (Grace Hopper) — migration to other hardware requires significant rearchitecture
- GPU-first retrieval dramatically increases hardware cost compared to CPU-based retrieval
- Model elasticity introduces non-determinism — the same query may get different quality results depending on current system load
- 10,000x model capacity increase requires proportionally more training data and compute to realize the full capacity advantage
- Operating at retrieval scale (billions of candidates) means even small per-candidate cost increases result in large aggregate compute requirements

## Why It Matters (Career Perspective)

Andromeda signals that ads retrieval — historically a domain of lightweight models, approximate nearest neighbor search, and CPU-based systems — is becoming a GPU-first deep learning problem. The skills required to build Andromeda are GPU systems engineering, hardware-software codesign, and deep learning at scale. This is a significant expansion of the "deep learning engineering" surface area in ads, extending it from ranking (where deep models have been standard for years) into retrieval.

For career planning, Andromeda means that GPU systems expertise is now valuable across the entire ads pipeline, not just ranking. Engineers who understand GPU memory hierarchies, hardware-specific optimization (as in the Grace Hopper codesign), and how to build deep learning systems that operate at retrieval scale are working on problems that are directly relevant to any large-scale ML serving role. The combination of scale (billions of candidates), latency constraints (real-time serving), and hardware codesign makes this among the most technically demanding work in production ML.
