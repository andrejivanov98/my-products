# Products I've built

Three live AI products I designed, built and run on my own, alongside my full-time job as a software engineer. Each folder explains one product: what it does, the end-to-end flow, how the AI is used, the architecture and the decisions behind it.

> The source code is private. This repository documents what each product does and how it is built. I'm happy to walk through the code in an interview.

| Product | What it does | AI at its core | Stack | |
|---|---|---|---|---|
| [**Nabrzinka**](https://nabrzinka.mk)<br/>Launched Jan 2026 | The day's news in Macedonia in one minute of scrolling. Short cards, a chat to dig deeper, local events, and one-tap image cards and video Reels for social media. | Seven Gemini agents pick, fact-check and write the news. A story needs two independent sources before it is written. | React PWA, Firebase, Gemini, Google Search grounding | [Read →](nabrzinka/README.md) |
| [**Triperco**](https://triperco.com)<br/>Launched Jul 2026 | Plan a whole trip in one sentence: the cheapest flight from your airport, a place to stay, things to do and where to eat, priced as one total. | One structured-output call turns the sentence into a trip brief. Code checks it against real airports and dates, and no model touches a price. | Next.js, Gemini, Postgres, Redis, Vercel | [Read →](triperco/README.md) |
| [**Resumco**](https://resumco.com)<br/>Launched Oct 2026 | Tailor a resume to a job with an honest match score first, build one in a short chat, or write a matching cover letter. ATS-friendly PDFs in English or German. | Seven single-purpose AI endpoints with validated structured output. A fast fit score runs before any rewrite, and shared rules stop the model inventing facts. | Next.js, Gemini, TypeScript, Vercel | [Read →](resumco/README.md) |

## What the three have in common

- **Business rules live in code, not in prompts.** The model reads, scores and writes. Deterministic code decides what ships: quotas and source counts in Nabrzinka, places and prices in Triperco, the match threshold and integrity checks in Resumco.
- **Structured output and validation everywhere.** Model answers are parsed into typed shapes and checked before anything reaches the user.
- **Cost and reliability by design.** Generate once and cache, cheap checks before expensive calls, fallbacks when the model fails or times out.
- **Privacy first.** No tracking, minimal data, and nothing kept that the product doesn't need.

## About me

**Andrej Ivanov**, software engineer with more than 8 years in the industry, from business analysis and product work to full-stack engineering and AI products.

[Portfolio](https://andrejivanov.com) · [LinkedIn](https://www.linkedin.com/in/andrejivanov98) · ivanovandrej10@yahoo.com
