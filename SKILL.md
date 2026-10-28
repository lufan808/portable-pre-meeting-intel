---
name: portable-pre-meeting-intel
description: Research a person before a meeting using recent public signals, their own voice, community reaction, third-party coverage, and verified identity anchors. Use for pre-meeting research, background briefing, or questions to ask someone.
---

# Portable Pre-Meeting Intel

Prepare a source-backed brief that helps the user walk into a first meeting with a clear view of what the person is doing and saying now. This is not a generic biography and not a dossier. The useful signal is the difference between the person's own framing and how other people interpret the same work.

## Operating principles

- Use the available web search, page-opening, browser, file, and writing tools in the current environment.
- If parallel agents are available, run the four research streams in parallel. If they are not, run the same streams sequentially; do not omit a stream silently.
- Deliver the finished brief as Markdown unless the user asks for another format.

## Trigger and inputs

Use for requests such as:

- “帮我准备和某人的会面”
- “研究某人最近在做什么”
- “会前了解一下某个人”
- `/portable-pre-meeting-intel [name] [company / role / meeting purpose]`

Extract:

- `name` — required person name;
- `context` — company, role, meeting purpose, or the user's own role when provided;
- `signal_window` — default to the last 90 days, unless the user specifies another period.

If the name is ambiguous, resolve it with the company, role, location, official bio, or another anchor. Ask the user to confirm rather than merging similarly named people.

State the exact signal window and generation date before research begins.

## Research workflow

### 1. Resolve identity before collecting claims

Find and open at least two independent identity anchors, preferably:

- official or employer bio;
- personal website, verified social account, LinkedIn, newsletter, podcast, or conference profile.

Record the URLs actually opened. Do not treat a search-result snippet as an opened source.

### 2. Collect four evidence streams

Search newest-first and prioritize dates over ranking. Use the user's context to choose relevant industry sources.

**A — Own voice**

Find recent posts, essays, interviews, podcasts, talks, newsletters, product announcements, or other first-person material. Capture the date, venue, concrete claim or action, and a short quote only when the source is accessible.

**B — Community reaction**

Look for practitioner discussion, replies, public comments, specialist forums, Reddit, Hacker News, or other relevant communities. Capture the trigger, sentiment, and one representative quote when available. Treat this as reaction evidence, not proof of an underlying fact.

**C — Third-party framing**

Find reputable journalism, trade press, analyst commentary, conference recaps, or expert commentary. Capture how others characterize the person's role, current move, strengths, risks, or omissions, and identify where the framing differs from the person's own account.

**D — Official baseline**

Gather the person's curated identity from an official bio, employer page, personal site, publisher, conference page, or verified profile. Note what the person consistently emphasizes and what third parties emphasize that the baseline omits.

For each usable signal, record:

- exact date and venue;
- the concrete event, statement, or behavior;
- source URL and source type;
- self-described versus externally described framing;
- confidence: `HIGH ✓`, `BREAKING ⚠`, or `LOW`.

### 3. Apply source discipline

- Only cite URLs that were actually opened successfully during the current research.
- Never invent a social-media post URL or status ID. If only the account page is verified, cite the account page and mark the specific post for manual location.
- Prefer primary sources for the person's own words and reputable sources for third-party claims.
- Separate fact, source-reported claim, community opinion, and the assistant's inference.
- Keep quotes short and paraphrase the rest. Do not reproduce long articles or posts.
- If recent evidence is thin, say so and lower the confidence instead of filling gaps with old biography.
- Do not infer private motives, sensitive traits, or confidential information from public traces.

### 4. Synthesize the current narrative

Answer these questions before drafting:

1. What is the strongest story in the signal window?
2. What does the person want the market or community to believe now?
3. What are they actively building, teaching, promoting, changing, or challenging?
4. Where does their own framing diverge from external framing?
5. What can the user ask that proves preparation and moves the meeting forward?

Write a coherent narrative rather than a dump of links. Treat any conclusion not directly stated by a source as an explicitly labeled inference.

### 5. Produce the brief

Use [references/output-template.md](references/output-template.md). Calibrate the detail and talking points to `context`.

Talking points must:

- refer to a specific recent signal or verified idea;
- be speakable rather than generic praise;
- end with a real question;
- include Chinese and English versions when the meeting is likely to be in English;
- avoid implying that the user agrees with an unverified criticism.

### 6. Deliver the brief

Write a Markdown artifact with a title such as:

`会前情报｜{name} @ {company or role}｜{YYYY-MM-DD}`

Save the brief where the user can reuse it. Keep the Markdown version as the source of truth when another delivery format is requested.

## Final quality gate

Before finishing, verify:

- identity is unambiguous;
- the exact signal window and generation date are visible;
- every material claim has an opened source or is labeled as inference;
- at least three dated recent signals are included when public evidence allows;
- self-versus-others comparison uses meaningful phrases, not isolated keywords;
- talking points are specific, contextual, and actionable;
- blocked sources, missing signals, and uncertain community claims are disclosed;
- the brief explains the research boundary and does not imply access to private information.
