# betterdesign.ai plugins

Connects AI tools to betterdesign.ai, a library of app and website screens designed by people.
## Claude Code

```
/plugin marketplace add betterdesign/betterdesign-plugins
/plugin install betterdesign@betterdesign
```

Claude Code asks for your API key when the plugin is installed. Generate one at
betterdesign.ai under Settings → API keys (paid plans). The key is kept in your
system's secure storage.

Then ask for a screen, or run `/betterdesign:find iOS onboarding`.

- Searching is free.
- Fetching a screen uses 1 credit and returns its image and its project's
  design.md. Fetching the same screen again in the same billing cycle is free.

To change the key later: `/plugin configure betterdesign@betterdesign`.

## Development

`claude-code/.mcp.json` reads `BETTERDESIGN_MCP_URL` when it is set, so the
plugin can be pointed at a local server:

```
BETTERDESIGN_MCP_URL=http://localhost:3000/api/mcp claude
```
