---
description: Find a screen in the BetterDesign library and build from it. Use when the person asks for a BetterDesign screen, or wants a real, human-made design to base a screen on.
argument-hint: "[what you're looking for, e.g. iOS onboarding]"
---

Find a BetterDesign screen for: $ARGUMENTS

Use the BetterDesign library tools (`search_screens`, `get_screen`, `get_account`).

1. Call `search_screens` with a few keywords from the request. Pass `device`, `platform` or `theme` only when the person named one. Searching is free.
2. Show the results as a numbered list: title, app, device, and the image link for each. Ask which one they want. Do not choose for them unless they asked you to.
3. When they pick one, call `get_screen` with its `screenId`. This uses 1 of their credits, so call it once, for the screen they chose. Fetching the same screen again in the same billing cycle is free. Ask before fetching more than one.
4. `get_screen` returns the screen image and the design.md of the project it belongs to. Tell them whether a credit was used and how many are left.
5. If they asked you to build something, use the image for layout and the design.md for exact values: colours, type, spacing, radii and components. Build in the stack already used in their project. Match the visual direction; do not claim a pixel copy.

If nothing matches, say so and suggest broader keywords. If a tool reports that the plan or the credits don't allow the request, pass that message on as it is.
