# Tight Prompting — 16 rules for token-efficient prompts

A living cheat sheet for writing prompts that cost less and do more. Each rule was earned the hard way: a real prompt went wrong, the failure got diagnosed, and the fix became a rule. Open `prompting-cheat-sheet.html` in a browser for the interactive version with demos.

## The 16 rules

Rules are listed in numeric order. Efficiency = structure & brevity; Behavior = model psychology.

1. Lead with the verb — Efficiency
2. Dictate the output shape — Efficiency
3. Cut politeness padding — Efficiency
4. Show, don't describe — Efficiency
5. Never restate — Efficiency
6. Split big tasks — Efficiency
7. Describe fully: goal, audience, format, constraints — Behavior
8. Discern before you ship — Behavior
9. One persona per prompt — Behavior
10. No fake-precision scores — Behavior
11. Demand replacement text, not advice — Behavior
12. Prohibitions need an outlet — Behavior
13. One job per prompt — but different readers count as different jobs — Efficiency
14. Structure beats adjectives — Efficiency
15. Cut the theater, keep the forcing function — Behavior
16. Ask for two variants — Efficiency

## How it's used

Every prompt shared under this workflow gets a what's-wrong / how-to-fix review, and each fix plus its rule lands here. The rules are currently being pressure-tested against new models (Gemini 4 Argon) to graduate them from "worked on Claude" to "holds across models."

## Why it matters for prompt engineering

This is prompt engineering as a discipline, not a bag of tricks: diagnose the failure mode, name the rule, verify it transfers. That's the whole job.

---
*Rules and coaching by Vince Pham, with Muse (Meta's AI assistant). The 30-prompt commercial pack built on these rules is a separate product — this repo is the free methodology.*
