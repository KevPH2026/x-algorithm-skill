name: x-algorithm
description: X (Twitter) Algorithm Optimization Expert. Uses the open-sourced X algorithm (Jan 2026) to analyze, score, and optimize content for maximum reach on X. Use when user asks to "optimize for X", "check my tweet", "X算法优化", "帮我写推文", or when content strategy for X is needed.
version: 1.0.0
metadata:
  openclaw:
    homepage: local-skill

# X Algorithm Optimization Skill (v1.0)

## Core Knowledge: X Algorithm 2026

X open-sourced its recommendation algorithm on January 19-20, 2026. This skill is built on the actual open-sourced code and official documentation.

### The Three-Stage Pipeline

```
For You Feed = Candidate Sources → Ranking → Mixer
```

**Stage 1: Candidate Sources**
- In-Network (60%): Posts from accounts you follow
- Out-of-Network (40%): Posts from accounts you don't follow (discovered via GraphJet, search, etc.)

**Stage 2: Ranking (heavy ML scoring)**
- Each candidate gets a virtual "likely to engage" score
- ML model predicts: reply, retweet, like, click, share, etc.

**Stage 3: Mixer**
- Combines ranked candidates with diversity constraints
- Author diversity: limits how many posts from same author appear consecutively
- Topic diversity: balances content types

---

## Engagement Weights (from open-sourced code)

| Action | Weight | Notes |
|--------|--------|-------|
| Reply | 150x like | Hardest engagement, highest value |
| Retweet with comment | 100x like | Quote tweet > plain RT |
| Retweet | 50x like | Amplification signal |
| Like | 1x baseline | Weakest signal |
| Click (link/media) | ~20x like | Indicates intent |
| Profile visit | ~20x like | Interest signal |
| Follow | ~100x like | Strong relationship signal |

**Key insight: Replies are worth 150x likes. Write to spark conversations.**

---

## Golden Rules for Reach

### 1. Early Engagement is Life or Death
- Posts with no engagement in first **1-2 hours** age out completely
- Your posting time must match when your audience is active
- In-network content gets priority → post when followers are online

### 2. First Line is Everything
- The system matches your post to viewers based on the first line
- Make your topic/obinion **obvious immediately**
- Don't hide your point in setup text
- No clickbait mystery headers

### 3. Write for Replies & Shares, Not Likes
- Replies = 150x the value of likes
- Shares = 50x the value of likes
- Ask questions, take stances, create tension
- End with invitations: "What's your take?", "A or B?", "Agree?"

### 4. Avoid These Filter Triggers
- Rage bait patterns (excessive ALL CAPS, outrage punctuation)
- Spam signals (too many hashtags, repetitive keywords, external links in main tweet)
- Duplicate content detection (don't repost the same content)

### 5. Author Diversity Limits
- The algorithm limits how many of YOUR posts appear in someone's feed at once
- Space out your best content
- Don't flood the feed with multiple posts at once

### 6. Self-Contained Content
- If your tweet needs context from previous tweets, it's harder to share and match to new viewers
- Each tweet should stand alone and make sense without thread context
- Exceptions: intentional threads (but make each tweet independently valuable)

### 7. No External Links in Main Tweet (for organic reach)
- Links dilute reach signal
- If you need to share a link, put it in a reply or thread

---

## Content Format Guidelines

### Best Performing (highest organic):
- Text-only tweets with strong opinion/stance
- Short, punchy, no thread needed
- Clear topic in first 10 words

### Good:
- Tweet + single image (image carries engagement)
- Tweet + single short video

### Avoid:
- Tweet with link (huge reach penalty)
- Tweet with multiple images
- Tweet with video + link combo

---

## When Analyzing Content

Run this checklist:

```
□ Topic/obinion clear in first line?
□ Ends with question or call-to-action for engagement?
□ No rage bait / spam filter triggers?
□ No external links in main tweet?
□ Self-contained (understandable without thread context)?
□ Posting time matches target audience active hours?
□ Spaced out from my other recent posts?
□ Takes a stance / creates conversation potential?
□ Not duplicating recent posts?
```

---

## When Generating Content

Apply these rules:

1. **Hook in first 10 words** - State the opinion/topic immediately
2. **Add tension/stakes** - Don't just inform, create reason to respond
3. **End with engagement prompt** - Question, choice, "agree?"
4. **No link in main tweet** - Put links in replies
5. **Match length to content type**:
   - Hot take: 1-3 sentences
   - Thread opener: 1 sentence + "🧵"
   - Long-form insight: Lead tweet = 1 sentence hook, thread for depth

---

## Engagement Window

- **Critical window**: First 1-2 hours after posting
- If post doesn't get early traction, it is effectively dead
- This means timing + audience activity = everything
- In-network early engagement is the #1 priority

---

## Skill Execution

This skill provides analysis and generation only (no posting). For posting, use the `post-to-x` skill.

**Analysis mode**: When user pastes content and asks to check/optimize
**Generation mode**: When user asks to write a tweet/post

---

## References

- Algorithm source code: https://github.com/twitter/the-algorithm
- Typefully analysis: https://typefully.com/blog/x-algorithm-open-source
- TechCrunch confirmation: https://techcrunch.com/2026/01/20/x-open-sources-its-algorithm
