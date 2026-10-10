# betterdesign.ai

betterdesign.ai is a library of app and website screens designed by people. This plugin lets Claude search that library and build from a screen you choose, using the screen's image for layout and its project's design.md for the exact colours, type, spacing and components.

## Install

Inside Claude Code, run:

```
/plugin install betterdesign-ai --marketplace the-betterlabs/betterdesign-mcp
```

Choose **Install for you**.

## What you need

A betterdesign.ai account on a paid plan, and an API key from Settings → API keys. Claude asks for the key when you install the plugin and keeps it in your system's secure storage. You can change it later with `/plugin configure`.

## How to use it

Ask for a screen in plain words, for example "find an iOS onboarding screen on betterdesign.ai", or run:

```
/betterdesign-ai:find iOS onboarding
```

Claude searches, shows the matches as a numbered list, and waits for you to pick one. It then fetches that screen and its design.md, and can build from them in your project's own stack.

## Credits

Searching is free. Fetching a screen uses 1 credit from your plan, the same credits as Copy to Figma on the site. Fetching the same screen again in the same billing cycle is free. Ask "how many betterdesign.ai credits do I have left" to check.

## What the plugin contains

- One skill, `find`, which is the `/betterdesign-ai:find` command.
- One connection to the betterdesign.ai MCP server at `https://betterdesign.ai/api/mcp`. It has three read-only tools: `search_screens`, `get_screen` and `get_account`.

## What it sends and receives

The plugin sends your API key and your search words or the chosen screen's id to betterdesign.ai, and nowhere else. It receives screen details, public image links, one screen image, and the text of a design.md. It does not read your files, run any code on your machine, or change anything in your betterdesign.ai account.

## Support

https://betterdesign.ai/contact
