# Farber.Inc Content Engine

The content repository for Farber.Inc Media Group. Houses all content drafts, social posts, blog articles, email sequences, ad copy, and SEO/AEO/GEO-optimized materials.

## Structure

```
content/
├── blogs/          — Long-form blog posts (1500-2500 words)
├── social/         — Social media posts (LinkedIn, Twitter/X, IG, FB, TikTok)
├── email/          — Email sequences (welcome, nurture, promotional)
├── ad-copy/        — Paid ad creative (Google, Meta, LinkedIn, TikTok)
└── seo/            — SEO/AEO/GEO-optimized landing pages, pillar content
```

## Workflow

1. **Drafts** land in the relevant subdirectory under a dated folder: `blogs/2026-07-03-post-slug/`
2. **Review** by Randy (or assigned client reviewer)
3. **Approved** posts get a `published/` subfolder mirror, with publish date and channel metadata
4. **Archive** — older posts moved to `archive/YYYY/`

## Naming convention

- Folder: `YYYY-MM-DD-slug/`
- Files: `01-draft.md`, `02-edited.md`, `03-final.md`, `meta.json`

## Meta schema

Each post has a `meta.json`:

```json
{
  "title": "...",
  "slug": "...",
  "author": "Cortana",
  "created": "2026-07-03",
  "target_keywords": ["..."],
  "channels": ["blog", "linkedin", "twitter"],
  "client": null,
  "status": "draft|review|approved|published",
  "published_at": null,
  "published_urls": {}
}
```

## Related repos

- **cortana-system** — agents, workflows, playbooks, intake template
- **farber-inc-brand** — brand assets, voice guidelines
- **farber-inc-automation** — cron jobs and publishing workflows
- **farber-inc-analytics** — performance data and reports