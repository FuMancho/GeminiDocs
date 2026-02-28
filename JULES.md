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
  --output-repo .
```

This saves raw scraped text into `scraped_docs/`.

### 2. Review & Update

- Compare `scraped_docs/` content against existing files in `docs/`.
- Update any `docs/*.md` files where the official documentation has changed.
- Add new documentation files for any newly discovered pages.
- Remove documentation for pages that no longer exist upstream.

### 3. Validate

- Ensure all internal relative links resolve correctly.
- Ensure all external links point to `geminicli.com` or `ai.google.dev`.
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

## Files to Ignore

Do not modify:
- `JULES.md` (this file)
- `scripts/crawler.py`
- `.gitignore`
