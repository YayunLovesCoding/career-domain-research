# The Great Convergence: How Ads, RecSys, and LLMs Are Merging

## The Thesis

The boundaries between Ads ML, Recommendation Systems, and Large Language Models are dissolving. What were once three distinct engineering disciplines with different architectures, training paradigms, and career tracks are converging into a single continuum of large-scale sequential prediction systems. For ML engineers making career decisions, this convergence is the most important structural trend to understand -- because it fundamentally changes the calculus of "which domain should I work in?"

## Architectural Convergence: One Architecture to Rule Them All

Eighteen months ago, the architecture stack for each domain looked fundamentally different. Ads systems ran wide-and-shallow models (logistic regression, gradient-boosted trees, relatively small deep networks) with massive hand-engineered feature stores. Recommendation systems used two-tower retrieval models, matrix factorization, and multi-stage pipelines. LLMs used autoregressive transformers at billion-to-trillion-parameter scale.

That picture is now outdated.

**Google's HSTU (Hierarchical Sequential Transduction Units)** is the clearest convergence signal. Published by DeepMind in February 2024, HSTU is a 1.5-trillion-parameter generative model for recommendations that replaces Google's entire multi-stage recsys pipeline with a single large transformer. The architecture is essentially identical to an LLM -- the only difference is that the "tokens" are user actions (clicks, watches, purchases) rather than words. HSTU achieved a 1.5x improvement over Google's prior production recsys and a 10x reduction in system complexity. This is the "GPT moment" for recommendations: a single massive generative model replacing a complex pipeline of specialized components.

**Meta's GEM (Generalized Embedding Model)** applies the same foundation model philosophy to ads. GEM is an LLM-scale ads foundation model that learns unified user and item representations across Meta's entire ads ecosystem. Rather than training separate models for each ad format, placement, and objective, GEM pretrains a single large model that can be fine-tuned for specific ads tasks -- the exact same pretrain-then-fine-tune paradigm that defines LLM engineering.

**Meta's ARM (Ads Recommendation Model)** pushes the scale further, serving trillion-parameter ads models in production. The infrastructure required to serve ARM -- model parallelism, quantization, batched inference, KV caching -- is the same infrastructure stack used to serve large language models. An engineer working on ARM inference optimization would be doing work nearly indistinguishable from an engineer optimizing LLM serving at Anthropic or OpenAI.

The conclusion is unavoidable: all three domains are converging on the transformer/foundation model architecture, and the engineering required to build, train, and serve these models is becoming domain-agnostic.

## Skill Convergence: The Shared Toolbox

As architectures converge, so do the required skills. The core competencies of a modern ML engineer working in any of these three domains now share roughly 70-80% overlap:

- **Distributed training**: Training trillion-parameter models requires expertise in data parallelism, tensor parallelism, pipeline parallelism, and expert parallelism. This is true whether the model predicts the next word, the next click, or the next purchase.
- **Large-scale embedding systems**: Ads, recsys, and LLMs all operate over massive embedding tables (user embeddings, item embeddings, token embeddings). TikTok's Monolith system handles trillion-scale collisionless embedding tables -- infrastructure that serves both recsys and ads use cases identically.
- **Attention mechanisms and sequence modeling**: The transformer's self-attention mechanism is now the computational backbone of all three domains. Understanding multi-head attention, positional encoding, and sequence-length scaling is universally required.
- **Inference optimization**: Serving large models under strict latency constraints (sub-100ms for ads auctions, sub-200ms for feed ranking, sub-1s for chat) demands the same techniques: quantization, pruning, speculative decoding, batched inference, and intelligent caching.
- **Evaluation at scale**: All three domains face the same fundamental challenge of evaluating model quality in production through online experiments, counterfactual estimation, and long-term metric measurement.

Epoch AI's data makes the convergence concrete: training compute is growing 4-5x per year at the frontier, but GPU performance only improves ~2x every 2-3 years. The gap must be closed by engineering talent. That talent -- distributed systems engineers, inference optimization specialists, ML systems architects -- is the same talent needed across all three domains.

## The "User Actions as Tokens" Paradigm

The most elegant expression of convergence is the reconceptualization of user behavior as a language. In the LLM paradigm, a model predicts the next token in a sequence of words. In the new recsys/ads paradigm, a model predicts the next action in a sequence of user events.

Meta's sequence learning framework treats every user interaction -- viewing a post, clicking an ad, watching a video, sending a message -- as a token in the user's "behavioral language." The model learns to predict what a user will do next, just as GPT learns to predict what word comes next. HSTU makes this explicit: it uses autoregressive generation (the same left-to-right generation used by ChatGPT) to produce recommendations.

Netflix's foundation model work follows the same pattern. Rather than building separate models per recommendation surface, Netflix trains a single large transformer on user interaction sequences that can be fine-tuned for specific surfaces -- homepage, search, "play something." The pretrain-fine-tune pipeline mirrors exactly what LLM teams do when adapting a base model for different downstream tasks.

This paradigm shift has a profound implication for career planning: if you understand autoregressive sequence modeling deeply -- whether you learned it building LLMs or building ad click prediction models -- you understand the core abstraction that now powers all three domains.

## Where They Still Differ: The Remaining 20%

Despite convergence, meaningful differences remain -- and they matter for career specialization.

**Ads retains unique complexity in:**
- Auction theory and mechanism design (second-price auctions, budget pacing, bid optimization)
- Causal measurement and incrementality (did the ad cause the purchase, or would it have happened anyway?)
- Real-time bidding infrastructure (making per-impression decisions in <10ms at millions of QPS)
- Advertiser-side optimization (budget allocation, creative selection, audience targeting)
- Privacy-preserving measurement under regulatory constraints (GDPR, ATT, cookie deprecation)

**Recsys retains unique complexity in:**
- Exploration/exploitation tradeoffs (balancing showing users what they like vs. discovering new preferences)
- Diversity and novelty optimization (avoiding filter bubbles, maintaining catalog coverage)
- Multi-objective ranking (engagement vs. satisfaction vs. platform health -- LinkedIn's challenge of memes vs. professional content)
- Cold-start problems (recommending for new users and new items with no history)

**LLMs retain unique complexity in:**
- Alignment and safety (RLHF, constitutional AI, jailbreak prevention)
- Language understanding and generation (linguistic competence, reasoning, instruction following)
- Long-context modeling (extending context windows, retrieval-augmented generation)
- Multimodal integration (text, image, video, audio in a single model)

These remaining differences create genuine domain expertise that takes years to develop. But crucially, they represent perhaps 20% of the total skill set, down from 60-70% just three years ago.

## The Key Insight: What "Staying in Ads" Actually Means Now

Here is the most important reframing for career decision-making: "staying in ads ML" increasingly means "doing foundation model work applied to advertising." If you are working on Meta's GEM or ARM, or Google's ads foundation models, or Amazon's ads ranking systems -- you are building and serving trillion-parameter transformer models. You are doing distributed training across GPU clusters. You are optimizing inference latency for massive models. You are working on the same technical frontier as LLM engineers, just applied to a different problem domain.

The pivot question, then, is not really about technical skill sets. It is about application domain, organizational context, and career narrative. An engineer working on GEM at Meta and an engineer working on Llama at Meta are using substantially overlapping skills, working in similar infrastructure, and solving structurally similar problems. The difference is in the business context (advertising revenue vs. developer platform), the evaluation criteria (ROAS and CTR vs. MMLU and HumanEval), and the external perception of the work.

Karl Higley's observation captures it well: the "traditional" ML engineer who spent most of their time on feature engineering and shallow models is being supplanted by a new archetype -- the engineer who builds and adapts foundation models for applied problems. This transition is happening simultaneously in ads, recsys, and LLMs. The engineers who will thrive are those who internalize the foundation model paradigm, regardless of which application domain they call home.

The convergence is not coming. It is here. The three domains are becoming three applications of the same underlying technology -- and the career question should be reframed accordingly.
