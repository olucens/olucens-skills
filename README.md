# olucens-skills

Personal curated Claude Code skill collection. 40 skills across three domains:

- **Coding** — Karpathy LLM coding guidelines (1 skill)
- **Startup & Strategy** — YC founder frameworks (19 skills)
- **Career & Resume** — Resume and job search tools (20 skills)

## Install

```bash
/plugin marketplace add olucens/olucens-skills
```

Or clone locally and install from path:

```bash
git clone https://github.com/olucens/olucens-skills ~/.claude/plugins/olucens-skills
```

## Skills Reference

### Coding

| Skill | Trigger |
|-------|---------|
| `karpathy-guidelines` => `olucens-code-workflow` | Writing, reviewing, or refactoring code — reduces LLM overcomplications |

### Startup & Strategy (YC Frameworks)

| Skill | Description |
|-------|-------------|
| `yc-startup-fundamentals` | Team formation, MVP, fundraising, growth, operations |
| `ai-startup-insights-altman` | Sam Altman on AI startups, moats, and product strategy |
| `ai-scaling-laws-amodei` | Dario Amodei on AI scaling and capabilities |
| `ai-product-building-heller` | AI product building (from $650M exit story) |
| `ai-accelerated-building-ng` | Andrew Ng frameworks for AI-accelerated development |
| `agi-framework-chollet` | François Chollet on AGI and intelligence measurement |
| `ai-scientific-discovery-jumper` | AI for scientific discovery (AlphaFold methodology) |
| `ai-search-strategy-srinivas` | Perplexity CEO on AI search strategy |
| `ai-startup-questions-fisher` | YC partner questions for evaluating startups |
| `b2b-ai-startup-levie` | Aaron Levie on B2B AI strategy and enterprise |
| `claude-code-guidance-cherny` | Boris Cherny on Claude Code best practices |
| `design-tool-scaling-field` | Figma COO on scaling a design tool |
| `developer-tools-strategy-truell` | Codeium CEO on developer tools and AI coding |
| `enterprise-ai-strategy-nadella` | Satya Nadella on enterprise AI adoption |
| `first-principles-thinking-musk` | Elon Musk first-principles reasoning framework |
| `robotics-ai-learning-finn` | Chelsea Finn on robotics and meta-learning |
| `software-democratization-masad` | Replit CEO on democratizing software creation |
| `software-paradigms-karpathy` | Andrej Karpathy on software 1.0 vs 2.0 vs 3.0 |
| `spatial-intelligence-li` | Fei-Fei Li on spatial intelligence and embodied AI |

### Career & Resume

| Skill | Description |
|-------|-------------|
| `resume-ats-optimizer` | ATS compatibility check + keyword match scoring |
| `resume-tailor` | Tailor resume to a specific job description |
| `resume-bullet-writer` | Rewrite bullets with metrics and impact |
| `job-description-analyzer` | Decode what JDs really want |
| `cover-letter-generator` | Generate targeted cover letters |
| `linkedin-profile-optimizer` | Optimize LinkedIn for recruiters and search |
| `interview-prep-generator` | Generate likely interview questions + answers |
| `salary-negotiation-prep` | Negotiation frameworks and scripts |
| `tech-resume-optimizer` | Tech-specific resume for engineering roles |
| `executive-resume-writer` | Senior/exec level resume strategy |
| `academic-cv-builder` | Academic CV for research roles |
| `career-changer-translator` | Frame previous experience for new industry |
| `creative-portfolio-resume` | Resume for design/creative roles |
| `offer-comparison-analyzer` | Compare and evaluate multiple job offers |
| `resume-formatter` | Format cleanup + ATS-safe structure |
| `resume-quantifier` | Add metrics and numbers to vague bullets |
| `resume-section-builder` | Build missing resume sections from scratch |
| `resume-version-manager` | Manage multiple resume versions per role |
| `portfolio-case-study-writer` | Write case studies for portfolio |
| `reference-list-builder` | Prepare and format references |

## Sources

| Skills | Source Repo |
|--------|-------------|
| `karpathy-guidelines` | [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) |
| YC frameworks | [jona/ycombinator-skills](https://github.com/jona/ycombinator-skills) |
| Resume tools | [Paramchoudhary/ResumeSkills](https://github.com/Paramchoudhary/ResumeSkills) |

## Customize

Skills are plain markdown files. Edit `skills/<name>/SKILL.md` directly — change triggers, add steps, remove sections you don't need. See [USAGE.md](USAGE.md) for a deep-dive on getting the most out of each skill.
