# Awesome GEO [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources for **Generative Engine Optimization (GEO)** — optimizing content so generative AI systems like ChatGPT, Perplexity, Google AI Overviews, Gemini, and Copilot retrieve, synthesize, and cite it in their answers.

GEO is the term academic research settled on for this discipline, and the one Wikipedia treats as canonical (with AEO, LLMO, AIO, and "AI SEO" redirecting to it). This list collects the research, official documentation, tools, and communities that define the field as it stands in mid-2026. Contributions welcome — see [Contributing](#contributing).

## Contents

- [What Is GEO?](#what-is-geo)
- [Foundational Research](#foundational-research)
- [Official Platform Documentation](#official-platform-documentation)
- [Guides & Explainers](#guides--explainers)
- [Tools & Platforms](#tools--platforms)
  - [AI Visibility Platforms](#ai-visibility-platforms)
  - [Open-Source Tools](#open-source-tools)
- [Technical Implementation](#technical-implementation)
- [Books](#books)
- [Courses & Training](#courses--training)
- [Newsletters, Blogs & People](#newsletters-blogs--people)
- [Communities](#communities)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)
- [License](#license)

## What Is GEO?

Generative Engine Optimization is the practice of shaping content, structure, and distribution so that generative AI systems select, trust, and cite it when synthesizing an answer — rather than simply ranking it in a list of links. It was defined as an academic discipline before it became a marketing buzzword, which is part of why it has the clearest research foundation of the AI-search terms in circulation.

Naming in this space is still a little tangled:

- **GEO (Generative Engine Optimization)** — the term coined in the founding Princeton/Georgia Tech/Allen Institute/IIT Delhi research; Wikipedia standardizes on GEO, with AEO, LLMO, AIO, and "AI SEO" all redirecting to it.
- **AEO (Answer Engine Optimization)** — the term most marketers and content teams reach for; used more or less interchangeably with GEO in practice.
- **LLMO (LLM Optimization)** — favored by some developer-tool builders.
- Google's own Search Central documentation maintains that none of this is a distinct discipline — it's still SEO, applied to a new answer surface.

Functionally, the work is the same regardless of label: structure content around clear, evidence-backed answers, and make sure the AI systems that matter can actually reach and parse your pages.

## Foundational Research

- [**GEO: Generative Engine Optimization**](https://arxiv.org/abs/2311.09735) — The paper that defined the field. Researchers from Princeton, Georgia Tech, the Allen Institute for AI, and IIT Delhi (Aggarwal et al., KDD 2024) ran ~10,000 queries through generative engines, tested nine content-modification strategies, and introduced the "impression score" and **GEO-BENCH** benchmark for measuring visibility inside AI-generated answers. The strongest tactics — citing sources, adding statistics, including quotations — lifted visibility by up to 40%.
- [**AgentGEO — Diagnosing and Repairing Citation Failures in GEO**](https://arxiv.org/abs/2603.09296) — Introduces the first taxonomy of *why* a document fails to get cited (rather than just measuring influence) and an agentic system that diagnoses and repairs those failures, improving citation rates by 40%+ while touching only ~5% of content.
- **AutoGEO** *(ICLR 2026)* — A framework that automatically learns what a given generative engine prefers, rather than relying on a fixed set of heuristics, and rewrites content accordingly.
- [**E-GEO: A Testbed for GEO in E-Commerce**](https://arxiv.org/abs/2511.20867) — The first e-commerce-specific GEO benchmark, evaluating rewriting heuristics across 7,000+ product queries.
- **Multi-Source Corroboration in GEO** *(Rankfor.AI, 2026)* — Empirical study on cross-platform citation optimization, finding large citation-rate gains when consistent information appears across 5–10 independent, high-authority sources.
- [**Awesome-GEO** by DavidHuji](https://github.com/DavidHuji/Awesome-GEO) — An actively maintained, deeper research-paper collection covering adversarial GEO topics (ranking manipulation, prompt injection risks) alongside the core visibility literature — a good companion for anyone going past the practitioner layer.

## Official Platform Documentation

- [Google Search Central — AI features & Search](https://developers.google.com/search) — Google's own guidance for AI Overviews, grounded in its existing indexing and E-E-A-T framework; Google has publicly stated it does not treat GEO as a separate discipline from SEO.
- [OpenAI — Crawlers documentation](https://platform.openai.com/docs/bots) — Documents `GPTBot` (model training), `OAI-SearchBot` (ChatGPT search indexing), and `ChatGPT-User` (user-triggered browsing) as independently controllable crawlers.
- [Perplexity — Bots & crawling](https://docs.perplexity.ai/) — Distinguishes `PerplexityBot` (indexing for answers) from `Perplexity-User` (real-time, user-triggered fetches).
- [Schema.org](https://schema.org/) — The structured-data vocabulary (`FAQPage`, `HowTo`, `Article`, `Product`, etc.) generative engines and rich-result systems parse.
- [Bing Webmaster Tools / Copilot documentation](https://www.bing.com/webmasters) — Microsoft's crawler and indexing guidance relevant to Copilot's generated answers.

## Guides & Explainers

- [Search Engine Land — GEO coverage](https://searchengineland.com/) — Trade-press coverage of generative-search shifts as they happen.
- [Backlinko — Generative Engine Optimization (GEO) guide](https://backlinko.com/) — Data-backed tactics for winning citations in AI search.
- [Search Engine Journal — Beginner's guide to GEO](https://www.searchenginejournal.com/) — An accessible starting point for people new to the field.
- [CXL — Answer/Generative Engine Optimization guide](https://cxl.com/blog/answer-engine-optimization-aeo-the-comprehensive-guide/) — Covers fundamentals plus emerging territory like agentic and voice search.
- [HubSpot — Answer/generative engine optimization trends](https://blog.hubspot.com/marketing/answer-engine-optimization-trends) — Focused on unifying GEO with existing SEO tooling and workflows.
- **Platform-specific breakdowns** — Multiple 2026 analyses document real differences in how each engine sources answers: Perplexity performs live retrieval on every query and rewards fresh, dated content (its heaviest citation source is community content, especially Reddit); ChatGPT leans on Wikipedia and established brand authority, with less consistent citation formatting; Google AI Overviews correlates strongly with existing top-10 organic rankings.

## Tools & Platforms

### AI Visibility Platforms

Commercial tools that monitor how often and how favorably a brand is mentioned or cited across generative engines. Evaluate on AI-engine coverage, whether insights connect to a content workflow, and pricing transparency — this category is broad and consolidating fast.

- [Profound](https://www.tryprofound.com/) — Enterprise-focused GEO analytics with strong publisher-partnership research.
- [Scrunch](https://scrunch.com/) — Combines monitoring, auditing, and content-delivery features in one platform.
- [Otterly.AI](https://otterly.ai/) — Straightforward AI-visibility tracking aimed at small and mid-size teams.
- [Peec AI](https://peec.ai/) — European-market generative-search monitoring platform.
- [AirOps](https://www.airops.com/) — Connects visibility data directly to content briefing and production.
- [AthenaHQ](https://www.athenahq.ai/) — Known for large-scale AI-response analysis and free visibility reports.
- [Conductor](https://www.conductor.com/) — Unified SEO + GEO platform for teams that don't want a separate tool.
- [Nightwatch](https://nightwatch.io/) / [SE Ranking](https://seranking.com/) — Established SEO tools that added generative-engine citation tracking modules.
- [Screpy](https://screpy.com/feature/ai-visibility/) — Tracks selected AI-search prompts, brand mentions, citations, source URLs, sentiment, and competitor visibility.

### Open-Source Tools

- [**Elmo**](https://github.com/elmohq/elmo) — Self-hosted, MIT-licensed AI-visibility tracker. Runs prompts against ChatGPT, Claude, Perplexity, Gemini, Copilot, and Google AI Overviews via your own API keys, so prompt history and data stay on your infrastructure. Widely regarded as the most actively maintained open-source option in this space.
- [**geo-aeo-tracker**](https://github.com/danishashko/geo-aeo-tracker) — Local-first, Next.js-based AI-visibility dashboard tracking six AI models via scraping APIs; includes a built-in site-audit crawler for AI-readiness checks.
- [**GEO topic pages on GitHub**](https://github.com/topics/generative-engine-optimization) — Browse the `generative-engine-optimization` and `ai-visibility` topic pages directly for the newest CLI tools, MCP-based skills, and citation-testing frameworks — this corner of the ecosystem changes fast enough that a static list goes stale within months.

## Technical Implementation

Practical, engine-agnostic groundwork that most GEO research and guides converge on:

- **Cite sources for claims** — The single most consistently effective tactic in the founding Princeton GEO study; treat every verifiable assertion as something that needs an attributed source.
- **Replace vague claims with specific numbers** — "Many companies struggle with this" is far weaker GEO material than a named study with a precise figure.
- **Structured data** — Implement `FAQPage`, `HowTo`, `Article`, and `Product` schema (JSON-LD) so generative engines get explicit entity and relationship data; schema should reflect what's actually visible on the page.
- **Freshness signals** — Real-time engines like Perplexity disproportionately cite recently published or updated content; visible date signals in titles and headings measurably improve citation rates.
- **`llms.txt`** — A proposed (not yet standardized) Markdown file at a site's root pointing AI systems to its most important content. Adoption is genuinely mixed — Google has said it doesn't use it and has no plans to — so treat it as low-cost hygiene, not core GEO strategy.
- **Crawler access management** — Deliberately allow or block AI bots in `robots.txt`: `GPTBot` / `OAI-SearchBot` (OpenAI), `PerplexityBot` (Perplexity), `ClaudeBot` (Anthropic), `Google-Extended` (Google's AI training, separate from the `Googlebot` that powers AI Overviews), and `Bytespider` (ByteDance). Blocking the wrong one can make a site invisible to an entire generative engine.
- **Wide corroboration** — Consistent information repeated across several independent, high-authority sources measurably improves citation odds versus a single, isolated mention.

## Books

- [**Answer Engine Optimization: A Field Guide for Navigating AI-Driven Search**](https://www.oreilly.com/library/view/answer-engine-optimization/0642572275549/) by Rodrigo Stockebrand (O'Reilly) — Published under the AEO label but squarely about the same generative-engine mechanics; explains how LLMs retrieve, evaluate, and decide which sources to include in an answer. Written by an 18-year search practitioner who has taught the subject at the University of Miami since 2009.

## Courses & Training

- [NoGood — AI Search & Answer/Generative Engine Optimization Course](https://nogood.io/aeo-course/) — Live cohort-based course on Maven, taught by NoGood's founder.
- [Class Central — Answer/Generative Engine Optimization courses](https://www.classcentral.com/subject/answer-engine-optimization) — Aggregates free and paid GEO/AEO courses across Coursera, Udemy, YouTube, and other platforms.
- Semrush Academy and Moz Academy have both folded generative/AI-search-visibility modules into their existing (free/paid) SEO certification tracks.

## Newsletters, Blogs & People

- [**The Marketing Newsletter**](https://themarketingnewsletter.org/) — Weekly marketing-growth newsletter covering AI, SEO, and content strategy for marketers and creators.
- [**Lead Generators**](https://leadgenerators.substack.com/) — Newsletter focused on lead-generation tactics and demand-gen strategy for growth teams.
- [**Aleyda Solis — SEOFOMO**](https://seofomo.co/) — Weekly SEO/AI-search newsletter with 45,000+ subscribers; covers AI Overviews and LLM citation shifts as they happen.
- [**Marie Haynes**](https://mariehaynes.com/newsletter) — Research-first newsletter with a strong quality/E-E-A-T lens applied to generative search.
- [**Mike King — Rank Report (iPullRank)**](https://ipullrank.com/blog) — Technical research blog and newsletter on how LLMs select and cite sources; one of the more rigorous technical voices in the space.
- [**The GTM Index — AI Search & GEO resource hub**](https://thegtmindex.com/geo/) — Curated, quarterly-updated round-up of tools, newsletters, and communities.

## Communities

- [Gen Engine Optimizers](https://genengineoptimizers.com/) — GEO-focused Slack community (via the "Grow Your Agency" network) with a dedicated `#llm-visibility` channel and active case-study sharing.
- [The AEO Community](https://theaeocommunity.com/) — Free Slack community for AEO/GEO practitioners; expects members to share real experiments rather than generic advice.
- [The SEO Community](https://theseocommunity.com/) — Large, long-running general SEO Slack (5,000+ members) with active AI/generative-search channels.

## Related Awesome Lists

For the deeper academic side of this specifically, these are worth a look:

- [DavidHuji/Awesome-GEO](https://github.com/DavidHuji/Awesome-GEO) — Research-paper-focused, including adversarial/manipulation-risk literature.
- [luka2chat/awesome-geo](https://github.com/luka2chat/awesome-geo) — General GEO resource collection.
- [amplifying-ai/awesome-generative-engine-optimization](https://github.com/amplifying-ai/awesome-generative-engine-optimization) — Guides, tools, and research with an agency/practitioner lean.

And for the wider marketing/AI-tooling ground this list doesn't cover:

- [marketingtoolslist/awesome-marketing](https://github.com/marketingtoolslist/awesome-marketing) — Broad marketing-tools list spanning SEO, content, email, CRM, and analytics, with GEO/AI-search as one slice of a much bigger picture.
- [alternbits/awesome-ai-marketing](https://github.com/alternbits/awesome-ai-marketing) — AI tools across the full marketing stack — content, personalization, lead gen, ads — not limited to AI search.
- [alternbits/awesome-ai-visibility](https://github.com/alternbits/awesome-ai-visibility) — A companion list dedicated specifically to the measurement/tracking side: how brands monitor their presence in AI-generated answers.
- [best-of-ai/awesome-ai-seo](https://github.com/best-of-ai/awesome-ai-seo) — AI-powered tools for classic SEO work — content generation, keyword clustering, audits, SERP tracking — adjacent to but distinct from GEO's focus on generative-answer citations.
- [marketinguys/awesome-gtm-engineering](https://github.com/marketinguys/awesome-gtm-engineering) — Tools and frameworks for the engineering side of go-to-market: attribution, event tracking, growth infrastructure, and experimentation.
- [marketinguys/awesome-content-marketing](https://github.com/marketinguys/awesome-content-marketing) — Content creation, distribution, and optimization resources — the broader discipline that GEO-oriented content strategy draws on.
- [marketinguys/awesome-dev-marketing](https://github.com/marketinguys/awesome-dev-marketing) — Developer marketing and DX resources, relevant if your GEO targets technical/developer audiences and platforms like Dev.to or Stack Overflow.
- [marketinguys/awesome-email-marketing](https://github.com/marketinguys/awesome-email-marketing) — Email and newsletter tooling — platforms, automation, deliverability, and AI copywriting.
- [marketingtoolslist/awesome-newsletter-ad-networks](https://github.com/marketingtoolslist/awesome-newsletter-ad-networks) — Ad networks and sponsorship marketplaces specifically for monetizing newsletters.
- [marketinguys/awesome-marketing-newsletters](https://github.com/marketinguys/awesome-marketing-newsletters) — A directory of marketing newsletters across SEO, growth, copywriting, and AI — a good source for more picks beyond the two featured above.

## Contributing

Contributions are welcome — this field moves fast and links go stale quickly. Please:

1. Check the resource isn't already listed.
2. Add it to the most relevant section, keeping descriptions to one concise, original sentence.
3. Open a pull request with a short note on why it belongs.

Please avoid pure marketing pages with no substantive content, and prefer primary sources (official docs, original research, first-party tool pages) over aggregator articles. See [CONTRIBUTING.md](CONTRIBUTING.md) for the full guidelines.

## License

[CC0](LICENSE) — To the extent possible under law, this list is released into the public domain.
