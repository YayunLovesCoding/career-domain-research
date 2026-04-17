# 5-Year Career Risk Analysis: Ads vs RecSys vs LLMs

## Purpose

This document evaluates the career risk profile of three ML domains -- Ads, Recommendation Systems, and Large Language Models -- across five dimensions that matter most for a 5-year career planning horizon. Each dimension includes a risk assessment and supporting evidence from industry data.

---

## 1. Market Demand Stability

### Ads ML: Low Risk -- Anchored to a Trillion-Dollar Market

Global digital advertising spend exceeded $700B in 2024, growing at 10-12% annually (GroupM, eMarketer). The total advertising market -- including traditional media -- is projected to surpass $1 trillion by 2025. This is not speculative investment; it is revenue flowing through established business models at every major tech company. Google's ad revenue alone exceeded $230B in 2023. Meta derives 97%+ of revenue from advertising.

The demand for ads ML engineers is structurally tied to this spend. Every dollar of ad revenue requires ML systems to target, bid, rank, and measure. As long as advertising remains the dominant business model of the internet -- and there is no credible alternative on the horizon -- demand for ads ML talent will remain robust.

**Risk factor**: Privacy regulation (GDPR, Apple ATT, cookie deprecation) is disrupting ads measurement and targeting, but this creates more work for ads ML engineers (privacy-preserving ML, on-device models, aggregated measurement), not less.

### RecSys: Low Risk -- The #1 AI Workload at Major Platforms

Meta publicly states that recommendation systems are their single largest consumer of AI compute infrastructure. Every major platform -- YouTube, TikTok, Netflix, Spotify, Amazon, LinkedIn, Pinterest -- is investing aggressively in recsys. The competitive dynamic that TikTok created (algorithmically-driven content discovery replacing social-graph-driven feeds) has forced every social platform to treat recsys as an existential capability.

Over 30% of Facebook Feed content is now AI-recommended from accounts users do not follow -- a massive expansion of the recommendation surface. Netflix, Spotify, and Amazon continue to treat recommendation quality as a core competitive advantage.

**Risk factor**: Recsys is less visible as a "market" because it is embedded within product teams rather than generating direct revenue. This can make it harder to quantify investment, but the compute budgets speak clearly.

### LLMs: Moderate Risk -- Explosive Growth With a Revenue Gap

LLM investment is growing faster than any technology sector in recent memory. OpenAI reached $2B+ in annualized revenue by 2024. Anthropic, Google, Meta, and dozens of startups are investing tens of billions in training and serving infrastructure.

However, Sequoia Capital's "$600B question" analysis highlights a structural concern: the AI ecosystem is spending $600B+ annually on infrastructure, but generating only ~$100B in AI-specific revenue. That $500B gap must close through either revenue growth or spending correction. The telecom bubble of the early 2000s -- where real technology saw real adoption, but investment timelines were compressed -- is the relevant historical parallel.

**Risk factor**: A correction would not eliminate LLM careers (the technology is real and transformative), but it could produce a tighter job market in 2-3 years if infrastructure spending retracts. Timing a pivot into LLMs at the peak of a spending cycle carries cyclical risk.

**Verdict**: Ads and RecSys offer more stable demand floors. LLMs offer higher growth potential but with meaningful correction risk.

---

## 2. Compensation Trajectory

### Ads ML: Stable and Strong

Ads ML engineers at major tech companies (Google, Meta, Amazon, Microsoft) earn $300K-$600K+ total compensation at senior levels (levels.fyi data). Career ladders are well-established, with clear progression from IC4/L4 through principal/staff levels. Compensation is predictable and tied to stable advertising revenue.

### RecSys: Comparable to Ads, With an Emerging Premium

RecSys compensation at the same companies is roughly equivalent to ads ML at comparable levels. An emerging premium is developing for engineers who combine recsys expertise with foundation model fluency -- what might be called "GenAI for RecSys" hybrid roles. Netflix, YouTube, and Meta organic recsys teams are competing for this profile, which can command a 10-20% premium over traditional recsys roles.

### LLMs: Highest Premium, But Sustainability Uncertain

LLM/GenAI roles currently command the highest compensation premium in ML engineering. Levels.fyi data shows:
- Mid-level at frontier labs (OpenAI, Anthropic, DeepMind): $300K-$500K total comp
- Senior at frontier labs: $500K-$900K+
- Research scientists/leads: $700K-$1M+

The LLM premium over equivalent general ML roles is estimated at 30-80% at comparable levels, driven by a severe supply-demand imbalance that Elad Gil characterizes as the scarcest resource in tech.

**Risk factor**: This premium will likely compress as talent supply grows. The 30-80% premium is a disequilibrium phenomenon. If the market corrects (per Sequoia's thesis), the premium could compress faster. However, even a compressed premium would likely leave LLM engineers well-compensated by absolute standards.

**Verdict**: LLMs offer the highest current compensation, but ads and recsys offer more predictable long-term trajectories. The risk-adjusted compensation over 5 years may be closer than the current snapshot suggests.

---

## 3. Automation and Commoditization Risk

### Ads ML: Augmentation, Not Elimination

Meta's REA (Recommendation Engine Autopilot) and KernelEvolve demonstrate that AI agents can augment ads ML engineers by automating feature engineering, hyperparameter tuning, and model iteration -- reportedly enabling 5x output per engineer. But this augments rather than eliminates the role. Engineers shift toward oversight, system design, and problem formulation.

The deeper structural trend is that foundation models are automating feature engineering -- Meta's sequence learning approach replaces hundreds of hand-crafted features with learned representations. This deprecates traditional feature-engineering skills but increases demand for engineers who can build and train large models.

### RecSys: Similar Trajectory to Ads

RecSys is following the same automation curve as ads. Karl Higley's analysis identifies feature engineering and feature-store-centric work as the skills most at risk of deprecation. Foundation models for recommendations (Netflix, LinkedIn, Pinterest) are replacing the traditional feature-pipeline-heavy approach. Engineers who can adapt foundation models for recommendation tasks are in higher demand; engineers whose primary skill is maintaining feature stores face commoditization.

### LLMs: The Paradox of Self-Commoditization

LLM engineering faces a unique paradox: the technology it builds is the technology most likely to automate parts of itself. Fine-tuning is already being commoditized by API providers -- what required a team of ML engineers in 2023 can now be done with a single API call. The a16z "GenAI platform" analysis identifies the middle layer of the stack (RAG pipelines, orchestration frameworks, basic fine-tuning) as most vulnerable to commoditization.

However, the extremes of the LLM stack remain deeply specialized: frontier model training (a skill possessed by perhaps a few thousand people globally), inference optimization (where hardware limitations create an engineering bottleneck that grows with each model generation), and safety/alignment research. Epoch AI's data -- training compute growing 4-5x/year against hardware improvements of 2x every 2-3 years -- ensures that systems engineering talent remains the bottleneck.

**Verdict**: All three domains face automation of routine tasks. The safe harbor in every case is the same: systems-level engineering, architecture design, and problem formulation. Feature engineering and pipeline plumbing are being automated everywhere.

---

## 4. Career Optionality (Doors Opened)

### Ads ML: Strong Transferability, Growing Over Time

Ads ML skills transfer to recsys with roughly 80%+ overlap -- two-tower retrieval models, ranking systems, multi-stage pipelines, and large-scale serving are shared infrastructure. YouTube's deep retrieval systems, for instance, use architectures nearly identical to ads retrieval. As ads systems adopt foundation model architectures (GEM, ARM, HSTU-style), transferability to LLM roles is also growing.

Unique ads skills in causal inference, measurement, and experimentation are valuable across all data-intensive domains -- not just ML. These skills transfer to product analytics, growth engineering, and even policy/economics roles.

**Limitation**: External perception. "Ads ML engineer" may be perceived as narrower than the actual skill set warrants, potentially requiring extra effort to reposition for non-ads roles.

### RecSys: Highest Optionality -- The Bridge Domain

RecSys occupies the natural bridge position between ads and LLMs. The skill overlap with ads is ~80% (shared retrieval and ranking infrastructure). The skill overlap with LLMs is growing rapidly as recsys adopts foundation model approaches (Netflix, Google HSTU, LinkedIn). Eugene Yan's analysis concludes that "recsys engineer who can leverage LLMs" is a more durable career position than "pure LLM engineer" for product-facing ML roles.

RecSys also offers the broadest industry applicability: e-commerce (Amazon), streaming (Netflix, Spotify), social media (Meta, TikTok), professional networking (LinkedIn), search (Google), and emerging verticals (healthcare, finance, education). This vertical diversity provides resilience against downturns in any single sector.

### LLMs: Highest Brand Value, But Potential Specialization Trap

An LLM background opens doors to frontier research labs (OpenAI, Anthropic, DeepMind, xAI), well-funded startups (hundreds forming annually per Elad Gil's analysis), and high-visibility positions at major tech companies. The "brand value" of LLM experience on a resume is currently unmatched.

**Limitation**: If the LLM field narrows or corrects, over-specialization in LLM-specific work (e.g., alignment research, prompt engineering) may limit lateral mobility. The Latent Space survey shows that 70% of "AI engineers" come from software engineering backgrounds, not ML -- suggesting that the AI engineer role may become more commoditized from the supply side than frontier ML roles. The a16z analysis warns that the middle layer (fine-tuning, RAG, orchestration) is most at risk.

**Verdict**: RecSys offers the highest long-term optionality by bridging the other two domains. LLMs offer the highest current brand value. Ads offers the most stable base with growing transferability.

---

## 5. Overall Risk Rating and Recommendation

| Dimension | Ads ML | RecSys | LLMs |
|---|---|---|---|
| Market demand stability | Low risk | Low risk | Moderate risk |
| Compensation trajectory | Stable, strong | Stable, emerging premium | Highest current, may compress |
| Automation risk | Moderate (feature eng.) | Moderate (feature eng.) | Bifurcated (low at frontier, high at middle) |
| Career optionality | Good, growing | Highest | High brand, specialization risk |
| **Overall 5-year risk** | **Low** | **Low-to-moderate** | **Moderate** |

### Composite Assessment

**Ads ML** is the lowest-risk option. It offers stable compensation, durable demand, and increasingly convergent technical skills. The primary risk is perceptual -- being seen as "just ads" -- rather than substantive.

**RecSys** is slightly higher risk only because it requires a job change (transition cost), but offers the best risk-adjusted optionality. It bridges the ads and LLM worlds, and the domain is experiencing a renaissance driven by foundation model adoption. A recsys role at a company actively adopting foundation models (Netflix, YouTube, Meta organic) provides both stability and frontier technical exposure.

**LLMs** carry the highest risk due to the spending-revenue gap identified by Sequoia and the potential for a cyclical correction. However, the risk is cyclical, not structural -- AI engineering has strong long-term fundamentals even if near-term hiring tightens. The risk is most acute for engineers at the application/middle layer; those working on frontier training, inference optimization, or safety face low commoditization risk.

### The Bottom Line

None of these three domains is a bad career bet over five years. The convergence trend means that strong engineering skills developed in any domain will transfer to the others. The question is not "which domain survives" (all three will) but "which position gives you the best combination of stability, growth, and optionality given your current starting point." For an ML engineer currently in ads, the answer depends on risk tolerance -- but all three paths lead to viable outcomes.
