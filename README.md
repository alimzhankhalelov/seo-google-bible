# 📖 seo-google-bible

> The ultimate SEO, E-E-A-T, and Schema Markup auditing skill, grounded strictly in the official Google Search Central documentation.

> [!IMPORTANT]
> This skill acts as an authoritative SEO architect. It does not guess. Every recommendation, audit, and schema implementation is grounded in the official Google Search Central guidelines.

`seo-google-bible` combines content quality analysis, technical search fundamentals, and advanced structured data implementation into a unified, source-driven workflow. Use this skill when you want to audit a site's SEO, implement schema markup, analyze content quality (E-E-A-T), or optimize for AI search.

## ✨ Features

- **Technical SEO & Indexing**: Verifies crawlability, robots.txt, HTTP status codes, and structural best practices.
- **Content Quality & E-E-A-T**: Evaluates content against Google's "Who/How/Why" test and Helpful Content framework.
- **Structured Data Generation**: Produces exact, copy-paste-ready JSON-LD schema (Article, FAQPage, Product, LocalBusiness) optimized for Rich Results and AI Overviews.
- **AI Search Optimization (GEO)**: Focuses on clear quotable facts and scannability to boost visibility in systems like Google AI Overviews and Perplexity.

## 🚀 Execution Modes

This skill operates in three distinct modes depending on your request:

### Mode A: Full SEO Audit
Provide a target URL, and the skill will fetch the page, analyze technical SEO, evaluate E-E-A-T, validate existing schema, and return a prioritized, actionable checklist (Red/Yellow/Green).

### Mode B: Content Optimization (Flow)
Provide a draft or published page. The skill will cross-reference it with SEO best practices, rewrite headings, add quotable facts, and restructure for maximum scannability.

### Mode C: Schema Generation
Provide the page intent (e.g., e-commerce product). The skill will output fully formed JSON-LD schema populated with the page's actual data.

## 📥 Installation & Usage

1. Clone or download this repository into your agent's global `skills` directory (e.g., `C:\Users\alimz\.gemini\antigravity\skills\seo-google-bible`).
2. Ensure the `references/` directory contains the required Google documentation markdown files.
3. Invoke the skill in your chat:

```text
Please run a Full SEO Audit on https://example.com using the seo-google-bible skill.
```

> [!TIP]
> Keep the documents in the `references/` folder up-to-date with the latest Google Search Central publications to ensure the skill always provides current advice.
