---
description: Delete a published htmldrop site by id
argument-hint: "[site id]"
---

Delete a htmldrop site using the `htmldrop_delete` MCP tool.

- The target site id may be in `$ARGUMENTS`. If it is missing or ambiguous, first call `htmldrop_list` and ask the user which site to delete.
- Show the title, slug, and URL of the site you are about to delete and confirm with the user before calling `htmldrop_delete`.
- After deletion, confirm which site was removed.
