# How to Get the Most From These Skills

Skills in Claude Code are passive — they're loaded as context and activate automatically when their trigger conditions match. This guide explains when each skill fires, how to get better results, and how to combine skills effectively.

---

## How Skills Work

A skill is a markdown file with a YAML frontmatter block:

```yaml
---
name: skill-name
description: Trigger conditions and use cases
---
```

The `description` field defines **when Claude activates the skill**. Claude reads it and decides whether the current task matches. You don't invoke skills manually — you just work naturally, and relevant skills activate.

**To force a skill**: explicitly mention its name or describe its use case: `"optimize this resume for ATS"`, `"apply karpathy guidelines here"`.

---

## Coding: karpathy-guidelines

**Best for:** Any coding task where you want Claude to stay disciplined.

**Auto-triggers when:** Writing, reviewing, or refactoring code.

**What it does:** Enforces 4 principles:
1. Think Before Coding — surface assumptions before implementing
2. Simplicity First — no speculative features or abstractions
3. Surgical Changes — touch only what the task requires
4. Goal-Driven Execution — define success criteria upfront

**Pro tips:**
- Before a complex task, say: "Before coding, list your assumptions and the success criteria." This forces step 1 explicitly.
- For refactors: "Apply karpathy surgical-changes rule — only touch what I asked, note any unrelated issues you see but don't fix them."
- For code review: "Review this with karpathy-guidelines lens — flag overcomplication and untraceable changes."

**When NOT to use it:** Trivial one-liners. The skill itself says "for trivial tasks, use judgment."

---

## Startup & Strategy Skills

These activate when discussing company building, AI strategy, product decisions, fundraising, or hiring.

### yc-startup-fundamentals
**Best for:** Early-stage founders making foundational decisions.

Covers: team formation (2-4 co-founders, 50%+ engineers), MVP timeline (2 months max), growth strategy (usage = sharing), fundraising FOMO tactics, frugality mindset.

**Pro tip:** Use the checklists explicitly: "Run me through the YC pre-launch checklist for my situation."

---

### ai-startup-insights-altman / ai-scaling-laws-amodei / agi-framework-chollet

**Best for:** Strategic thinking about AI product direction.

**When to invoke:** "What's the right AI strategy for [product]?", "How should we think about moats?", "What does the scaling curve mean for us?"

**Pro tip:** Combine these three for a multi-perspective strategy session: "Apply Altman, Amodei, and Chollet frameworks to evaluate our AI product roadmap."

---

### software-paradigms-karpathy

**Best for:** Understanding where to use ML vs. traditional code.

**Pro tip:** "Apply the Software 1.0/2.0/3.0 framework to decide which parts of our system should be model-driven."

---

### first-principles-thinking-musk

**Best for:** Breaking down a problem you're over-engineering.

**Pro tip:** "Apply first-principles to our current architecture — what assumptions are we holding that we shouldn't be?"

---

### claude-code-guidance-cherny

**Best for:** Getting Claude Code to work better on your project.

Covers: structuring tasks for Claude, good vs. bad prompts for coding agents, when to use subagents.

**Pro tip:** Invoke before starting a large multi-file task: "Apply claude-code-guidance to help structure this implementation."

---

## Career & Resume Skills

These activate when you provide resume text, a job description, or ask about job search topics.

### The Core Workflow

For a new job application, use skills in this order:

1. **`job-description-analyzer`** — decode what the JD really wants
2. **`resume-tailor`** — align your resume to the decoded requirements
3. **`resume-ats-optimizer`** — verify ATS score (target 80%+)
4. **`resume-bullet-writer`** + **`resume-quantifier`** — strengthen weak bullets
5. **`cover-letter-generator`** — write a targeted cover letter
6. **`interview-prep-generator`** — prepare for the interview

---

### resume-ats-optimizer

**What it does:** Calculates keyword match %, flags formatting issues, gives an ATS Compatibility Report with a score out of 100.

**Pro tip:** "Give me a full ATS compatibility report for this resume against this job description. Target 80%+ match."

**Common issues it catches:** Contact info in header, columns/tables, non-standard section names, missing keywords.

---

### resume-tailor

**Pro tip:** Provide both resume and JD. "Tailor my resume for this role — show me exactly what to change, don't rewrite everything."

---

### resume-bullet-writer + resume-quantifier

These work together. `resume-quantifier` adds metrics; `resume-bullet-writer` rewrites structure.

**Pro tip:** "Rewrite these bullets with the STAR format and add metrics where possible — ask me if you need numbers."

---

### job-description-analyzer

**Pro tip:** "Analyze this JD: what are the real must-haves vs. nice-to-haves? What does this role actually care about beyond what's listed?"

---

### interview-prep-generator

**Pro tip:** "Generate 15 interview questions for this [role/company] — include behavioral, technical, and culture-fit questions. Then give model answers using my background."

---

### salary-negotiation-prep

**Pro tip:** Provide the offer details. "Help me negotiate this offer. I have [X competing offers / Y years experience / Z market data]."

---

### linkedin-profile-optimizer

**Pro tip:** "Optimize my LinkedIn headline and About section for [target role] recruiter searches. Use SEO-style keyword placement."

---

### career-changer-translator

**Best for:** Moving between industries (e.g., finance → tech, academic → industry).

**Pro tip:** "I'm moving from [industry A] to [industry B]. Translate my experience — reframe, don't hide it."

---

## Combining Skills

Skills stack — Claude uses all active/relevant skills simultaneously.

**Useful combinations:**

| Goal | Skills to invoke |
|------|-----------------|
| Disciplined AI product development | `karpathy-guidelines` + `software-paradigms-karpathy` |
| Job application end-to-end | `job-description-analyzer` → `resume-tailor` → `resume-ats-optimizer` → `cover-letter-generator` |
| AI startup strategy session | `ai-startup-insights-altman` + `first-principles-thinking-musk` + `yc-startup-fundamentals` |
| Code with AI product context | `karpathy-guidelines` + `claude-code-guidance-cherny` |
| Career pivot | `career-changer-translator` + `resume-tailor` + `linkedin-profile-optimizer` |

---

## Customizing Skills

All skills are plain markdown in `skills/<name>/SKILL.md`. Edit freely:

- **Change trigger conditions** — modify the `description:` frontmatter to control when the skill activates
- **Add personal context** — append your preferred frameworks, company context, or style preferences
- **Remove sections** — cut parts of the skill that don't apply to your use case
- **Combine skills** — merge two SKILL.md files into one if you always want them together

After editing, Claude picks up changes automatically — no reinstall needed.
