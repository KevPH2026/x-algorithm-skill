# X Algorithm Optimization Skill

> Optimize your tweets for maximum reach using X's open-sourced algorithm (January 2026).

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://github.com/openclaw)
[![X Algorithm Open Source](https://img.shields.io/badge/X%20Algorithm-Open%20Source%202026-green)](https://github.com/twitter/the-algorithm)

## What is this?

An [OpenClaw](https://github.com/openclaw/openclaw) skill that uses the **actually open-sourced X recommendation algorithm** (January 19-20, 2026) to analyze and optimize content before posting.

No guessing. No "best practices" myths. Just code-grounded insights from X's actual ranking system.

## Features

- **Engagement weight analysis** — replies are worth 150x likes. Learn which actions actually move the algorithm
- **Content scoring checklist** — run any tweet through a 9-point filter based on real algorithm rules
- **Optimal timing guidance** — understand why early engagement is life-or-death for your posts
- **Format recommendations** — what actually gets penalized (hint: links in main tweet)
- **Generation mode** — write new content that is algorithm-aware from the start

## Based on Real Code

This skill is built on X's actually-open-sourced algorithm:
- Main recommendation code: [`twitter/the-algorithm`](https://github.com/twitter/the-algorithm)
- Engagement weights confirmed from source
- Three-stage pipeline: Candidate Sources → Ranking → Mixer

## Installation

### Automatic (via Clawhub)

```bash
npx clawhub@latest install x-algorithm
```

### Manual

```bash
git clone https://github.com/KevPH2026/x-algorithm-skill ~/.openclaw/skills/x-algorithm
```

## Usage

### Optimize existing content

Paste your tweet and ask:
- "optimize this for X"
- "check if this follows the algorithm"
- "帮我看看这条"

### Generate new content

Ask for algorithm-aware content:
- "write me a tweet about [topic]"
- "帮我写一条关于AI的推文，要符合X算法"

## The Algorithm in 30 Seconds

X's feed runs posts through 3 stages:

```
For You = Candidate Sources → ML Ranking → Mixer
```

**Candidate Sources:**
- 60% In-Network: posts from accounts you follow
- 40% Out-of-Network: discovered through search, engagement graphs, etc.

**Ranking:** ML model predicts how likely each post is to generate specific engagement actions.

**Mixer:** Applies diversity constraints (author diversity, topic balance) and serves the final feed.

## Engagement Weights (from open-sourced code)

| Action | Relative Weight |
|--------|----------------|
| Reply | 150x |
| Retweet with comment | 100x |
| Retweet | 50x |
| Like | 1x |
| Click | ~20x |
| Profile visit | ~20x |

**Bottom line: Write to spark replies. Every reply is worth 150 likes.**

## Golden Rules

1. **First line is everything** — the algorithm matches your post to viewers based on the opening words. State your topic immediately.
2. **Early engagement is everything** — posts with no engagement in the first 1-2 hours age out permanently
3. **Write for replies, not likes** — replies are 150x more valuable
4. **No links in main tweet** — external links trigger reach penalties
5. **Don't duplicate** — repost detection will shadowban your reach
6. **Space your posts** — author diversity limits how many of your posts appear in one feed
7. **Self-contained content** — if it needs thread context to understand, it won't get shared

## Example

**Before (violates algorithm):**
> "Hey everyone! I wanted to share some thoughts on AI tools for business. Check out my latest post at [link]! #AI #productivity"

Problems: Weak opener, link in main tweet, hashtag spam, no engagement trigger

**After (algorithm-aware):**
> "AI tools are making junior employees better than senior employees were 5 years ago. Not a bad thing. But if you're a senior who hasn't adapted yet, the gap is widening."
>
> "What's your take?"

First line: Clear, opinionated topic
Engagement: Ends with "What's your take?" → invites replies
No links. No hashtags. Stands alone.

## Credits

Built from:
- [twitter/the-algorithm](https://github.com/twitter/the-algorithm) — X's actual open-sourced code
- [Typefully](https://typefully.com/blog/x-algorithm-open-source) — detailed analysis of Jan 2026 open source
- [TechCrunch](https://techcrunch.com/2026/01/20/x-open-sources-its-algorithm) — coverage confirming the release

## License

MIT
