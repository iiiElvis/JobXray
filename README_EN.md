# JobXray — See through the JD.

English | [中文](README.md)

Your interview recon assistant. Before you apply, see the full picture — how well you match, what you'll be asked, and whether the role has hidden risks.

## Who is this for

| You are... | JobXray helps you... |
|------------|---------------------|
| A job seeker about to apply | Scan the role against your resume before submitting, avoid blind applications |
| A candidate with an upcoming interview | Predict what the interviewer will ask and prepare targeted responses |
| Someone unfamiliar with the company | Infer company pain points from the JD and public info, show initiative in interviews |
| Evaluating multiple opportunities | Quickly scan each JD for risk signals, filter out problematic roles |

## Problems we solve

| Traditional approach | JobXray approach |
|---------------------|-----------------|
| Guessing "does this role fit me" by gut feeling | Line-by-line comparison of JD requirements vs. resume evidence |
| Walking into interviews blind | Predicting targeted questions based on your gaps and resume weak points |
| Not understanding what the company actually needs | Inferring real pain points from JD wording + public information |
| Not knowing what to ask the interviewer | Generating targeted reverse questions to evaluate the employer |
| Can't tell normal JD descriptions from warning signs | Systematic scan of 7 risk signal types, each citing JD source text |

## Core capabilities

\`\`\`
Input (JD + Resume)
    │
    ▼
┌─────────────────────────────────────────────┐
│  Overview — overall assessment + key advice   │
├─────────────────────────────────────────────┤
│  Module 1: JD breakdown                       │
│  → Hard requirements / Responsibilities /     │
│    Skills / Soft requirements                 │
├─────────────────────────────────────────────┤
│  Module 2: Company pain point analysis        │
│  → JD text analysis + public info search      │
├─────────────────────────────────────────────┤
│  Module 3: Line-by-line matching              │
│  → ✅Match / ⚠️Gap / ❌Missing +              │
│    confidence tags                            │
├─────────────────────────────────────────────┤
│  Module 4: Risk assessment                    │
│  → Risk level (framework-derived) + advice    │
├─────────────────────────────────────────────┤
│  Module 5: Interview prediction               │
│  → Predicted Qs + why they'll ask + angles    │
├─────────────────────────────────────────────┤
│  Module 6: JD risk signals                    │
│  → 7 risk signal types                        │
├─────────────────────────────────────────────┤
│  Module 7: Reverse questions                  │
│  → What to ask + purpose + what to listen for │
└─────────────────────────────────────────────┘
    │
    ▼
Output (Full scan report)
\`\`\`

## Quick Start

1. Install the Skill: \`/install JobXray\`
2. Start a conversation — JobXray sends an intro automatically
3. Send a JD + your resume (text / image / PDF)
4. Get a full 7-module scan report

## Supported roles

JobXray works with any role that has a clear JD. Typical coverage:

| Category | Example roles |
|----------|--------------|
| Product | Product Manager, AI PM, Data PM, B2B/B2C Product |
| Engineering | Frontend / Backend / Fullstack, Algorithm Engineer, Data Engineer, Architect |
| Data | Data Analyst, Data Scientist, BI Analyst |
| Design | UI/UX Designer, Interaction Designer, Visual Designer |
| Operations | User Ops, Content Ops, Growth, Community Ops |
| Marketing / Sales | Marketing Manager, Brand, Enterprise Sales, BD |
| Management | Project Manager, Team Lead, Director |

Applicable to: new grads, experienced hires, internships, and career changers

## Scientific framework

JobXray's analysis is rule-based, not vibes-based.

### Match criteria

| Marker | Criteria |
|--------|---------|
| ✅ Match | Resume **explicitly mentions** the skill/experience/qualification with concrete evidence |
| ⚠️ Gap | Resume has **related but not exact** content, or **insufficient detail** |
| ❌ Missing | Resume has **no relevant evidence** whatsoever |

### Confidence tags

| Tag | Meaning |
|-----|---------|
| \`[Resume text]\` | Directly stated in the resume |
| \`[Inferred]\` | Deduced from resume context |
| \`[Unknown]\` | Resume provides no information on this |

### Risk level framework

Determined by crossing JD wording strength × resume coverage — no subjective judgment:

| | JD says "required" | JD says "preferred/bonus" |
|---|---|---|
| **Resume has nothing** | 🔴 High risk | 🟡 Medium risk |
| **Resume has partial match** | 🟠 Medium-high risk | 🟢 Low risk |

## What we don't do

| Won't do | Why |
|----------|-----|
| Rewrite or optimize your resume | At the application stage, you need to see the opportunity clearly, not edit your resume |
| Give a composite score or success prediction | Can't be scientifically quantified — giving one would mislead |
| Decide "will you pass" for you | The decision belongs to you — we lay out the information |
| Search anonymous employee reviews | Not public info, outside our search boundary |
| Benchmark salary levels | Requires specialized data sources, not in current scope |
| Generate ATS formats / outreach scripts | Not part of interview recon |

## Search boundary

The company pain point module searches public information within clear boundaries:

| We search | We don't search |
|-----------|----------------|
| Company's core business and business lines | Anonymous employee reviews (Blind, Glassdoor) |
| Recent developments (hiring, product launches, funding) | Specific salary data |
| Public tech blogs, product announcements | Internal org structure or non-public info |

## JD risk signal types

| Signal type | What it looks like |
|-------------|-------------------|
| Vague responsibilities | Core duties described too broadly — unclear what you'd actually do |
| Unrealistic requirements | Too many skills or experience years for the level |
| Blurred boundaries | One role covering work that belongs to multiple positions |
| Overtime hints | "Thrives under pressure", "fast-paced", "flexible hours", "startup mentality" |
| Salary anomalies | No salary listed, range too wide, or clearly below market |
| Frequent reposting | Same role posted repeatedly (if posting date is visible) |
| Title-responsibility mismatch | Senior responsibilities with junior title/pay, or vice versa |

## File structure

\`\`\`
jobxray/
├── README.md              # Project overview — Chinese
├── README_EN.md           # Project overview — English (this file)
├── jobxray_skill.md       # Core Skill rules
\`\`\`

## Integrity principles

- All match assessments are based on what the resume actually states — no subjective speculation
- Every assessment includes a confidence tag (\`[Resume text]\` / \`[Inferred]\` / \`[Unknown]\`) to distinguish fact from inference
- Risk levels are derived through the framework, not gut feeling
- JD risk signals must cite source text, no guessing
- Company information is based on public sources with attribution
- When information can't be found, fall back to JD text analysis — never fabricate

## Roadmap

- [ ] Salary benchmarking (integrate market salary data sources)
- [ ] Multi-JD comparison (scan multiple opportunities side by side)
- [ ] Mock interview practice (simulate interviews based on predicted questions)
- [ ] Industry insights (interview trends and common assessment criteria by industry)

## License

MIT
