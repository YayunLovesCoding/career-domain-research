# Spotify: Reinforcement Learning for Music Recommendation

- **Source type**: Engineering blog
- **Company/Author**: Spotify Engineering
- **Date**: June 2024
- **URL**: https://engineering.atspotify.com/2024/reinforcement-learning-recommendations/
- **Domain**: Music/audio streaming recommendations

## Summary

Spotify is moving beyond traditional supervised learning (predict-click) toward reinforcement learning for optimizing long-term user satisfaction. The approach uses bandit algorithms and off-policy evaluation to balance exploration (showing users new music they might like) with exploitation (playing safe favorites). A key insight is that optimizing for short-term engagement metrics (clicks, streams) can hurt long-term retention, so Spotify is developing reward functions that capture user satisfaction over sessions and weeks rather than individual interactions.

## Why it matters for career decisions

This signals that recsys is evolving beyond the "predict CTR" paradigm that dominates ads. While ads systems are heavily optimized for short-term conversion, organic recommendation systems are developing more sophisticated optimization objectives. RL-based approaches require a different skill set than standard supervised ML -- understanding of exploration, off-policy evaluation, reward design, and long-horizon optimization. For an ML engineer in ads, this represents both an opportunity (new technical challenges) and a differentiator (RL skills are rarer than supervised ML skills).

## Key technical themes

- Bandit algorithms for exploration-exploitation
- Off-policy evaluation for safe policy updates
- Long-term reward shaping (session-level, retention-level)
- Moving beyond click-prediction to satisfaction optimization

## Career relevance

- **Technical differentiation**: RL for recsys is a frontier area with fewer practitioners than standard supervised recsys
- **Ads comparison**: Ads are mostly stuck in short-term optimization; recsys is pushing into longer-horizon RL
- **Growing demand**: As platforms mature, user retention becomes more important than raw engagement, driving RL adoption
