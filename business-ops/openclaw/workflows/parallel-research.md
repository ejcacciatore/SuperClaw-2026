# Parallel Research Workflow

**How to research multiple topics/competitors simultaneously using sub-agents.**

---

## Use Case

You need to research 5 competitors, 10 topics, or multiple markets — and you want it done fast.

---

## Pattern

```javascript
// Spawn multiple research sub-agents
const topics = [
  "Fintech data fabric competitors",
  "Real estate transaction platforms",
  "Operational resilience consulting market",
  "E-commerce artisan marketplaces",
  "Political commentary monetization"
];

topics.forEach(topic => {
  sessions_spawn({
    task: `Research "${topic}". Find top 5 players, their pricing, strengths/weaknesses, and market position. Output: structured markdown report.`,
    label: `research-${topic.toLowerCase().replace(/\s+/g, '-')}`,
    mode: "run",  // One-shot
    model: "anthropic/claude-sonnet-4-6"
  });
});

// Results come back asynchronously
// Consolidate when all finish
```

---

## Workflow

1. **Define research questions** (clear, specific)
2. **Spawn sub-agents** (one per question)
3. **Wait for results** (they auto-announce when done)
4. **Consolidate** (main agent synthesizes)
5. **Make decision** (based on aggregated intel)

---

## Example: Competitive Analysis

```javascript
sessions_spawn({
  task: `Research CalcGuard's competitors in the institutional trading data space.

Find:
1. Top 5 competitors
2. Their products/features
3. Pricing (if public)
4. Customer segments
5. Strengths and weaknesses
6. Market positioning

Output: Markdown table + summary analysis.`,
  label: "research-calcguard-competitors",
  mode: "run",
  model: "anthropic/claude-sonnet-4-6"
});
```

**Result:** Structured report in ~5 minutes.

---

## Tips

- Keep research questions specific (not "tell me everything")
- Use `mode: "run"` for one-shot research
- Use `mode: "session"` if follow-up questions likely
- Spawn 3-5 agents max at once (avoid overwhelming)
- Consolidate results yourself or spawn a "synthesizer" agent

---

**Time savings:** 5 topics researched in parallel = 1/5th the time of serial research.
