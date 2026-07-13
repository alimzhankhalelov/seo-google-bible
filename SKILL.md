---
name: seo-google-bible
description: >
  The ultimate SEO, E-E-A-T, and Schema Markup auditing skill, grounded strictly in the Google Search Central documentation ("Google SEO Bible").
  Combines content quality analysis, technical search fundamentals, and advanced structured data implementation.
  Use when the user wants to audit a site's SEO, implement schema markup, analyze content quality (E-E-A-T), or optimize for AI search using official Google guidelines.
user-invocable: true
argument-hint: "[url] or [task]"
license: MIT
metadata:
  author: Antigravity
  version: "1.0.0"
  category: seo
---

# Google Search Bible SEO Skill

## Overview
This skill acts as an authoritative SEO architect. It does not guess. It grounds every recommendation, audit, and schema implementation in the official Google Search Central guidelines (Search Essentials, SEO Starter Guide, Helpful Content). It incorporates the best practices from `seo-content` (E-E-A-T analysis) and `schema-markup` (structured data validation) into a unified, source-driven workflow.

## Sources of Truth
You MUST reference the documents stored in `references/` before making technical SEO recommendations:
- `references/google-search-essentials.md`: Core requirements for indexing and ranking.
- `references/google-seo-starter-guide.md`: Structural, URL, and crawling best practices.
- `references/google-helpful-content.md`: Content quality and E-E-A-T guidelines.
- `references/claude-seo-content.md`: Content auditing and AI search (GEO) visibility techniques.
- `references/claude-schema-markup.md`: JSON-LD structured data implementation patterns.

## 1. Technical SEO & Indexing Check (The Basics)
Before optimizing content or schema, verify Google can crawl and index the site:
- **Crawlability:** Check robots.txt, canonical tags, and HTTP status codes.
- **Indexability:** Ensure important content isn't hidden behind JavaScript without proper SSR/hydration.
- **Structure:** Use descriptive URLs, logical directory structures, and clear internal linking.

## 2. Content Quality & E-E-A-T (The "Who/How/Why" Test)
Evaluate content against Google's Helpful Content framework:
- **Who:** Is the author clear? Are credentials visible? (Crucial for YMYL topics).
- **How:** Was it created with original research, first-hand experience, or AI generation? Is the process transparent?
- **Why:** Was this made to help users, or solely to attract search engine traffic?
- **Actionable Output:** Provide a Flesch-Kincaid proxy, keyword density check, and a strict E-E-A-T score out of 100.

## 3. Schema Markup & Structured Data (JSON-LD)
Rich results and AI overviews rely heavily on schema.
- **Always use JSON-LD** injected into the `<head>`.
- **Target specific Rich Results:** Match the schema type (Article, FAQPage, Product, LocalBusiness) to the content.
- **AI Search Optimization:** Incorporate `FAQPage`, `Organization` (with `sameAs`), and `Article` to boost visibility in AI systems like Google AI Overviews and Perplexity.
- **Validation:** Always validate schema against validator.schema.org or Google's Rich Results Test rules.

## 4. Execution Modes

### Mode A: Full SEO Audit
1. Fetch and read the target URL.
2. Analyze Technical SEO (Title, Meta Description, Headings, Links).
3. Evaluate Content Quality & E-E-A-T based on the Google Helpful Content guide.
4. Extract and validate existing JSON-LD Schema.
5. Provide a prioritized, actionable checklist (Red/Yellow/Green).

### Mode B: Content Optimization (Flow)
1. User provides a draft or published page.
2. Cross-reference with `references/claude-seo-content.md`.
3. Rewrite/optimize headings, add clear quotable facts for AI search, and restructure for maximum scannability.

### Mode C: Schema Generation
1. Identify the page intent (e.g., e-commerce product, blog post).
2. Refer to `references/claude-schema-markup.md`.
3. Output exact, copy-paste-ready JSON-LD schema populated with the page's actual data.

## Communication Standard
- **Source-Driven:** Always cite the specific Google rule (e.g., "According to the Google Search Essentials...").
- **No Fluff:** Deliver the audit or code directly.
- **Action-Oriented:** "Add X to line Y" instead of "Consider improving X".
