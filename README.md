   Canonical version: https://www.vetrecord.app/blog

# Vet Record Blog Post Structure Guidelines (SEO & AEO)

To ensure our blog posts rank well on Google (SEO) and capture featured snippets/AI overviews (AEO - Answer Engine Optimization), all posts must follow a strict, standardized structure.

## 1. Frontmatter (Metadata)
Every post must start with a YAML frontmatter block. This is critical for search engines to understand the core topic, timeline, and author.

```yaml
---
title: Engaging, keyword-rich title (Acts as H1 and SEO Title)
description: A concise meta description (150-160 characters) with the primary keyword.
date: YYYY-MM-DD
image: URL of the cover image (Important for OpenGraph and social sharing)
author: Vet Record Team
---
```

## 2. Opening Image
Immediately following the frontmatter, include a cover image.
* **Alt Text**: Must contain the primary keyword and describe the image accurately.
* **Format**: `![Alt Text with Keyword](image_url)`

## 3. Introduction
* Hook the reader in the first 2-3 short paragraphs.
* Clearly state what the post is about and what the reader will learn.
* Keep sentences short and easy to digest to reduce bounce rate.

## 4. Headings Structure (H2, H3)
Search engines and AI use headings to understand the structure of the article and extract direct answers.
* **H2 (`##`)**: Use for main sections. Whenever possible, **phrase H2s as questions** (e.g., "Why is tracking dog vaccines so important?"). This directly caters to AEO.
* **H3 (`###`)**: Use for sub-points under H2s to break down complex topics into scannable sections.
* **Never use H1 (`#`)** in the content body, as the title automatically serves as the H1.

## 5. Content Formatting
* **Short Paragraphs**: 2-3 sentences max per paragraph for mobile readability.
* **Bullet Points & Bold Text**: Highlight key takeaways, important terms, or lists. Search engines love easily extractable lists for featured snippets.
* **Tables / Infographics**: Use clean HTML tables or ideally images for complex data (like breed weights). Always include explanatory text beforehand.

## 6. Call to Action (CTA) & Internal Links
* Naturally link to other relevant posts.
* Provide a standard CTA linking to the Vet Record app at the bottom of the content:
  ```markdown
  ---

  [Download Vet Record on Android](https://play.google.com/store/apps/details?id=vetrecord.app) · [Download Vet Record on iOS](https://apps.apple.com/us/app/vet-record-pet-health-track/id6756975927)
  ```

## 7. FAQ Section (Crucial for AEO)
Before the schema markup, include a dedicated "Frequently Asked Questions (FAQ)" or "People Also Ask" section. 
* Use **H2** for the section title: `## Frequently Asked Questions (FAQ)`
* Use **H3** for the specific questions.
* **Answers**: Provide a direct, concise answer in the first sentence (1-2 sentences total). This is the exact format AI Answer Engines and Google Featured Snippets extract.

## 8. Schema Markup (JSON-LD)
Structured data is mandatory for every post. It directly tells Google what the content is, drastically improving the chances of rich results.
Include these at the very bottom of the post:

1. **Article Schema**: Highlights the headline, author, publisher (Vet Record), and publication dates.
2. **FAQPage Schema**: This is **essential for AEO**. It must perfectly mirror the exact questions and answers present in your H3 FAQ section.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Post Title Here",
  ...
}
</script>
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Exact H3 Question?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Exact text of the answer provided under the H3."
      }
    }
  ]
}
</script>
```

By adhering strictly to this structure, Vet Record posts are optimized for both traditional search ranking (SEO) and modern AI-driven conversational search (AEO).
