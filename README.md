# betterdesign.ai for AI tools

Connects AI tools to betterdesign.ai, a library of app and website screens designed by people.

## Claude Code

Inside Claude Code, run:

```
/plugin install betterdesign-ai --marketplace the-betterlabs/betterdesign-mcp
```

Choose **Install for you**. Claude Code then asks for your API key. Generate
one at betterdesign.ai under Settings → API keys (paid plans). The key is kept
in your system's secure storage.

On older versions of Claude Code, use two steps instead:

```
/plugin marketplace add the-betterlabs/betterdesign-mcp
/plugin install betterdesign-ai@betterdesign-ai
```

Then ask for a screen, or run `/betterdesign-ai:find iOS onboarding`.

- Searching is free.
- Fetching a screen uses 1 credit and returns its image and its project's
  design.md. Fetching the same screen again in the same billing cycle is free.

To change the key later: `/plugin configure betterdesign-ai@betterdesign-ai`.
To get a new version: `/plugin update betterdesign-ai@betterdesign-ai`.

See [claude-code/README.md](claude-code/README.md) for what the plugin does and sends.
