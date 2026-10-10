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

## Examples

- "Find a pricing page on betterdesign.ai." Claude lists the matching screens with their images and asks which one you want.
- "Fetch number 2 and build it as a React component with Tailwind or generate a new frame in Figma from it." Claude fetches that screen and its design.md for 1 credit, then writes the component using the design.md's colours, type and spacing.
- "Show me dark mobile settings screens." Claude searches with the device and theme filters applied.
- "How many betterdesign.ai credits do I have left?" Claude reports your plan, your remaining credits and the date they reset.

## Credits

Searching is free. Fetching a screen uses 1 credit from your plan, the same credits as Copy to Figma on the site. Fetching the same screen again in the same billing cycle is free. Ask "how many betterdesign.ai credits do I have left" to check.

## What the plugin contains

- One skill, `find`, which is the `/betterdesign-ai:find` command.
- One connection to the betterdesign.ai MCP server at `https://betterdesign.ai/api/mcp`. It has three tools: `search_screens` and `get_account` only read, and `get_screen` reads a screen and uses 1 credit.

## What it sends and receives

The plugin sends your API key and your search words or the chosen screen's id to betterdesign.ai, and nowhere else. It receives screen details, public image links, one screen image, and the text of a design.md. It does not read your files or run any code on your machine. The only change it makes to your betterdesign.ai account is using a credit when it fetches a screen.

## Changing your API key

If you revoke a key or want to use a different one, run this inside Claude Code, in the terminal or in the desktop app's Code tab:

```
/plugin configure betterdesign-ai@betterdesign-ai
```

Paste the new key, save, and start a new session. If tools stop working with a message about an invalid or revoked key, this is the fix.

## Troubleshooting

- **"Invalid or revoked API key"**: generate a new key in Settings → API keys, then follow "Changing your API key" above.
- **"This API key is connected to …"**: each key works with one AI tool. Generate a separate key for Claude Code, or release the key in Settings → API keys.
- **"This account is on the free plan"**: the plugin works on paid plans only. Upgrade at https://betterdesign.ai/pricing; the same key then works.
- **"Out of credits"**: credits reset at the start of your next billing cycle. Searching stays free.
- **The tools do not appear**: start a new Claude Code session after installing or changing the key.

## Support

Questions and security reports: info@betterlabs.live

https://betterdesign.ai/contact
