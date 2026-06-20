---
description: Publish HTML or Markdown to a hosted htmldrop URL
argument-hint: "[slug or title hint, optional]"
---

Publish content to htmldrop using the `htmldrop_publish` MCP tool.

Source of the content, in priority order:
1. If the user attached or referenced a specific file, publish that file's contents.
2. Otherwise, if there is HTML or Markdown produced earlier in this conversation, publish the most recent such document.
3. Otherwise, ask the user what to publish.

Before calling the tool:
- Choose a short, readable, URL-safe `slug` (lowercase, hyphenated). If the user passed a hint in `$ARGUMENTS`, use it to inform the slug and/or title.
- Choose a descriptive `title`.
- Prefer a single self-contained file (inline CSS/JS) so the page renders standalone.

After calling `htmldrop_publish`, report the returned public URL prominently, plus the site id and slug.
