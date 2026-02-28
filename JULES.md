# Jules Task Instructions — GeminiDocs

## Purpose

This repository contains community-maintained documentation for the **Google Gemini AI ecosystem** — including Gemini models, Gemini API, and associated agentic coding tools. Jules is responsible for keeping it up-to-date with the official source.

## Documentation Source

| Field | Value |
|---|---|
| Start URL | `https://geminicli.com/docs/` |
| Base Path | `/docs/` |
| Official Domain | `geminicli.com`, `ai.google.dev` |

## Weekly Update Procedure

### 1. Crawl

```bash
python3 scripts/crawler.py \
  --start-url https://geminicli.com/docs/ \
  --base-path /docs/ \
  --output-repo . \
  --official-domains geminicli.com,ai.google.dev
```

This saves raw scraped text into `scraped_docs/`.

### 2. Review & Update

- Compare `scraped_docs/` content against existing files in `docs/`.
- Update any `docs/*.md` files where the official documentation has changed.
- Add new documentation files for any newly discovered pages.
- Remove documentation for pages that no longer exist upstream.

### 3. Validate

- Ensure all internal relative links resolve correctly.
- Ensure all external links point to `geminicli.com` or `ai.google.dev` (see Link Handling Policy below for third-party rules).
- Verify heading hierarchy (`#` → `##` → `###`, no skipped levels).
- Code blocks must specify a language (e.g., ` ```bash `).

### 4. Commit

Use this commit message format:

```
docs: weekly documentation update [automated]
```

## Formatting Standards

- **Markdown:** GitHub-flavored Markdown (`.md`).
- **Headings:** Strictly hierarchical — never skip levels.
- **Code:** Inline code uses single backticks. Code blocks use triple backticks with a language tag.
- **Callouts:** Use GitHub-style alerts (`> [!NOTE]`, `> [!TIP]`, `> [!WARNING]`, etc.).
- **Links:** Internal links use relative paths. External links point to verified official domains.

## Link Handling Policy

This is the most important section for autonomous operation. Follow these rules exactly:

### Reference File

Always consult `docs/official-links.md` as the single source of truth for verified URLs before writing any links.

### Official Links

- **Allowed domains:** `geminicli.com`, `ai.google.dev`
- When a link can be replaced with an official equivalent from `docs/official-links.md`, do so.

### Third-Party Links — Decision Rules

| Domain Type | Action | Example |
|---|---|---|
| GitHub repos (`github.com`) | ✅ **Keep** | `github.com/google-gemini/gemini-cli` |
| Package registries (`npmjs.com`, `pypi.org`) | ✅ **Keep** | `npmjs.com/package/@anthropic-ai/...` |
| Cloud provider docs (`cloud.google.com`) | ✅ **Keep** | Google Cloud setup guides |
| Personal blogs, Medium, Dev.to | ❌ **Remove** | Replace with official equivalent or remove entirely |
| Forums, Reddit, Stack Overflow | ❌ **Remove** | Not authoritative |
| Unofficial mirrors or aggregators | ❌ **Remove** | Not trustworthy |

### New Official Links

If the crawler discovers new official pages not yet in `docs/official-links.md`, add them to the file in the correct section.

### Dead Links

If a link returns 404 or is unreachable (check `scraped_docs/_link_audit.md`), remove it and note the removal in the commit message.

### Using the Link Audit Report

After crawling, the file `scraped_docs/_link_audit.md` contains a pre-classified list of all discovered links:
- ✅ **Official** — these are fine, no action needed
- ⚠️ **Third-party** — apply the decision rules table above
- ❌ **Dead** — remove from documentation

## Files to Ignore

Do not modify:
- `JULES.md` (this file)
- `scripts/crawler.py`
- `.gitignore`
