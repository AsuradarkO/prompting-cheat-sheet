# Tight Prompting — 16 rules for token-efficient prompts

A living cheat sheet for writing prompts that cost less and do more. Each rule was earned the hard way: a real prompt went wrong, the failure got diagnosed, and the fix became a rule. Open `prompting-cheat-sheet.html` in a browser for the interactive version with demos. See `tight-prompting/SKILL.md` for a ready-to-use skill that applies these 16 rules to rewrite bloated prompts.

## The 16 rules

Split into two types. Efficiency rules keep their original numbers; Behavior rules are numbered 1–7 within their group.

### Efficiency (structure & brevity) — 9 rules
1. Lead with the verb
2. Dictate the output shape
3. Cut politeness padding
4. Show, don't describe
5. Never restate
6. Split big tasks
13. One job per prompt — but different readers count as different jobs
14. Structure beats adjectives
16. Ask for two variants

### Behavior (model psychology) — 7 rules
1. Describe fully: goal, audience, format, constraints
2. Discern before you ship
3. One persona per prompt
4. No fake-precision scores
5. Demand replacement text, not advice
6. Prohibitions need an outlet
7. Cut the theater, keep the forcing function

## How it's used

Every prompt shared under this workflow gets a what's-wrong / how-to-fix review, and each fix plus its rule lands here. The rules are currently being pressure-tested against new models (Gemini 4 Argon) to graduate them from "worked on Claude" to "holds across models."

## Why it matters for prompt engineering

This is prompt engineering as a discipline, not a bag of tricks: diagnose the failure mode, name the rule, verify it transfers. That's the whole job.

---
*Rules and coaching by Vince Pham, with Muse (Meta's AI assistant). The 30-prompt commercial pack built on these rules is a separate product — this repo is the free methodology.*
