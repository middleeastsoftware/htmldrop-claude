---
name: htmldrop-publishing
description: Use when publishing HTML or Markdown to htmldrop — guidance for producing a clean, standalone page and choosing a good slug, title, and password.
---

# Publishing to htmldrop

htmldrop turns an HTML or Markdown document into a real hosted URL via the
`htmldrop_publish` MCP tool. Follow these practices so the published page looks
good and is easy to find.

## Build a self-contained page

- Prefer a single HTML file with inline CSS and JS. External relative assets
  will not resolve unless they are uploaded too, so inline what you can.
- Ensure the document has a `<title>`, a `<meta name="viewport">`, and sensible
  default typography so it renders well on mobile.
- For Markdown, keep it valid CommonMark; htmldrop renders it server-side.

## Choose slug and title

- `slug`: short, lowercase, hyphenated, URL-safe (e.g. `alex-rivera-cv`). It
  becomes part of the public URL.
- `title`: human-readable; used for the page/browser title.

## Passwords

- Suggest a password when the content is a private draft or a personal share
  not meant for public discovery.
- Do not password-protect content the user explicitly wants public.

## After publishing

- Always surface the returned public URL clearly so the user can click it.
- Mention the site id if the user may want to update or delete it later
  (via `/htmldrop:delete`).
