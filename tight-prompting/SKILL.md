---
name: tight-prompting
description: Rewrite bloated prompts into tight, token-efficient ones using 16 proven rules. Use when the user asks to tighten a prompt, fix a prompt, review a prompt, cut tokens, or says "make this prompt better".
user-invocable: true
---

# Tight Prompting

Turn a bloated prompt into one where every token earns its place. Apply the 16 rules below, in order, then show the before/after.

## The 16 rules

1. **Lead with the verb.** Start with what you want, not background. Cut openers like "Hi, I was wondering if you could please help me…".
2. **Dictate the output shape.** Constrain length and format up front ("Reply in 5 bullets, max 15 words each") — it prevents rambling you pay to trim later.
3. **Cut politeness padding.** "Please", "thank you so much", "I'd really appreciate it" cost tokens and change nothing about quality.
4. **Show, don't describe.** One 3-line example of the desired format beats 100 words explaining it.
5. **Never restate.** In an ongoing chat, "same format as above" replaces a whole paragraph of repeated instructions.
6. **Split big tasks.** One mega-prompt with 8 requirements produces a bloated answer. Chain it: draft → "tighten" → "check X".
7. **Describe fully: goal, audience, format, constraints.** The model can't see what you don't say. Every missing detail (who it's for, how long, what tone, what to avoid) gets filled with a guess — and you pay to fix the guess.
8. **Discern before you ship.** Delegation decides *before* (what to hand off); discernment judges *after* (is this output actually right?). AI is fluent, not honest — it states guesses with total confidence. Verify facts and numbers before anything goes out.
9. **One persona per prompt.** "Strict ATS" and "senior recruiter" in one prompt pull opposite directions — a keyword parser and a human judge score differently. Sequence them or pick one.
10. **No fake-precision scores.** A 0–100% "match score" is invented authority — a confident guess dressed as measurement. Ask for the decision the score was supposed to inform instead ("list the 5 gaps that would actually cost me the interview").
11. **Demand replacement text, not advice.** "Suggest how to fix it" leaves the writing on you. Make the model quote the offending line and hand back the rewritten fix.
12. **Prohibitions need an outlet.** "Don't invent metrics" fighting "be measurable" — under pressure the model quietly invents anyway. Give the approved alternative: "Where a metric would help, write [ADD NUMBER: what to measure]."
13. **One job per prompt — but different readers count as different jobs.** Two prompts with the same inputs aren't duplicates if they model different judges. An ATS parser and a senior recruiter reading the same resume-vs-JD are two stages of the real pipeline, not one question asked twice.
14. **Structure beats adjectives.** A sentence-by-sentence spec ("Sentence 2: biggest achievement with data") outperforms adjective stacking ("high-impact, measurable, results-focused"). Tell it the shape, not the vibe.
15. **Cut the theater, keep the forcing function.** The model can't "look for 10 seconds" — it's stage direction. The "single biggest doubt" constraint is what actually does the work. Keep the constraint, drop the play-acting.
16. **Ask for two variants.** Choosing between options beats editing one draft. Two versions cost little and give you something to react against.

## How to apply

1. Read the user's draft prompt.
2. Name which rules it violates (cite rule numbers).
3. Rewrite it applying all 16 rules.
4. Show the rewrite, then one line per rule explaining what changed and why.

## Worked example

Bloated: "Hello! I hope you're well. Could you please write me a short story about a robot? Maybe ~300 words, kind of sad but hopeful? Thank you so much!"

Tight: "Write a 300-word story: a robot, sad but hopeful tone."

Same result, a third of the tokens. (Rules 1, 2, 3, 7 did the work.)

---
*Rules and coaching by Vince Pham, with Muse (Meta's AI assistant). Based on the 16-rule Tight Prompting cheat sheet in this repo.*
