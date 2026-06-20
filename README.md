# htmldrop for Claude Code

Publish HTML or Markdown to a real hosted URL — straight from Claude Code.
Authentication is a one-click browser login (OAuth); there is no API token to
copy or config to edit.

## Install

```
/plugin marketplace add middleeastsoftware/htmldrop-claude
/plugin install htmldrop@htmldrop
```

The first time you run a htmldrop command, Claude Code opens your browser to
sign in to htmldrop and authorize access. After you approve, the tools are
ready.

## Commands

| Command | What it does |
|---|---|
| `/htmldrop:publish` | Publish the current file or a document from the conversation; returns the public URL. |
| `/htmldrop:list` | List every site your account owns. |
| `/htmldrop:delete` | Delete a site by id (asks first). |

You can also just ask in natural language, e.g.
*"Make a one-page HTML CV for Alex Rivera and publish it to htmldrop."*

## How it works

The plugin registers a remote MCP server at `https://htmldrop.app/mcp`. Claude
Code discovers htmldrop's OAuth 2.1 authorization server automatically, registers
itself, and runs the PKCE login flow in your browser. Your token is stored and
refreshed by Claude Code — it never lives in this repo or your project files.

## Other clients

Using Claude Desktop, Cursor, or another MCP client instead of Claude Code? Use
the `@htmldrop.app/mcp` npm package — see
<https://htmldrop.app/agents/> for setup.

## Links

- htmldrop: <https://htmldrop.app>

## License

MIT — see [LICENSE](LICENSE).
