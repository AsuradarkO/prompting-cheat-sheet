# Japanese Anime Studio — Model-Agnostic Animation Prompt

Adapted from the Awesome Opus 5.5 Videos collection, for use with any AI agent — not just Claude.
Nothing here has been published to GitHub.

## Source (honest attribution)

- Repo: yihui-dev/awesome-opus5-5-videos (MIT License)
- Closest match in that repo to "Japanese anime studio": **Anime Style Opening Teaser** by @rafiroutes
  - File: prompts/rafiroutes-596199.md
  - Original post: https://x.com/rafiroutes/status/2107465888622596199
- There is no prompt in that repo literally titled "Japanese anime studio." The anime-related prompts found are:
  - Anime Style Opening Teaser (@rafiroutes) — the closest title match
  - An anime-like AI battle trailer (@ishuagra02) — "Art style must be anime-like"
  - Sumi-e Ink Film (@pradeepXkapoor) — a 90-second Japanese ink-painting film, in code
  - Rain Station Animated Short (@zhu185178) — a 30-second 2D animation storyboard preview, in Chinese

## Original prompt, verbatim

> Implement all scenes, interactions/camera motions, and shader effects 100% in Three.js code (excluding character models from Blender, background sky from GPT imgen, and BGM from Google flow). Create an anime style opening teaser.

## Claude-specific elements flagged (and removed in the version below)

1. **Usage instruction, not the prompt itself:** the repo's How to use says "Paste it into Claude Opus 5.5 (Claude Code, the Claude app, or any agent running Opus 5.5)." That is the main Claude-only lock.
2. **Title / framing:** "Opus 5.5 video" — removed, so the prompt does not name a model.
3. **Tool-specific exclusions in the original:** "background sky from GPT imgen, and BGM from Google flow" — replaced with generic wording: you may supply your own character models, background, and music from any tool you already use. No agent should be forced to use a specific vendor's image or music tool.
4. **No Claude-only features remain:** the original prompt asks for standard Three.js code, which any capable coding agent can write. No Claude Code commands, no Anthropic-only formatting, and no model identity line are in the adapted version.

## Adapted prompt — paste this into any AI agent

> You are a production assistant for a Japanese anime studio. The studio's artists still draw by hand, frame by frame, and that constant hand work is the bottleneck — your job is to reduce redrawing, not to replace the artists' drawings.
>
> Input I will give you: [paste your keyframes, character sheets, storyboard panels, or a description of the scene — replace this bracketed line with your actual inputs].
>
> Build an anime-style opening teaser as a single, self-contained HTML file:
> - Render all scenes, camera motion, and shader / lighting effects in code (Three.js, Canvas, or SVG — use whichever the agent supports best, and say which one you used).
> - Preserve a hand-drawn anime look: cel shading, bold ink-like outlines, limited animation feel (holds, 2s and 3s timing where appropriate), and expressive key poses — do not turn it into smooth 3D-game motion unless I ask for that.
> - Use my supplied character art / models, background, and music if I provide them. If I do not provide them, use simple placeholder art and clearly mark every placeholder, so nothing fake is passed off as final studio art.
> - The file must open by double-clicking it, with no build step and no local files except public CDNs (Three.js, GSAP, etc.).
> - Include a simple timing sheet in the page or as comments: scene list, duration of each shot, and which keyframe each shot starts from, so an animator can check and correct it by hand.
> - Include an export option: a button or instructions to save individual frames, so the studio can print, trace, or clean up any frame by hand if needed.
> - If the code is too long for one reply, stop at a clean scene break, tell me the exact scene you stopped at, and continue from there in the next reply without restarting or rewriting earlier scenes.
>
> Deliver the full HTML in one code block, or as a downloadable file if your platform supports that. Do not describe the animation instead of building it.

## How to use it with any agent

1. Copy the adapted prompt above.
2. Paste it into ChatGPT, Gemini, Muse, Grok, Copilot, Claude, or any other coding agent — do not add "you are Claude" or any model name.
3. Replace the bracketed Input line with your actual keyframes / storyboard / scene description.
4. Ask for the single HTML file, open it in a browser, and record the page if you want a video.
5. If the agent truncates the code, tell it: "Continue from exactly where you stopped, in the same file, without restarting."
6. If the agent cannot save a file, ask it to output the full HTML in one code block, save it yourself as `index.html`, and open it.

## Why this fits Japanese anime studios, in your words

Most Japanese anime studios still do it by hand, working constantly. This prompt does not ask the studio to abandon hand drawing — it asks the agent to do the repetitive, code-able parts (camera moves, shader / lighting effects, timing, and frame assembly) around the artists' keyframes, so the hand work is concentrated on the drawings that actually need a human hand, and the in-between assembly is not redrawn from scratch every time.

---
*Adapted by Vince Pham, with Muse (Meta's AI assistant), from @rafiroutes' Anime Style Opening Teaser in yihui-dev/awesome-opus5-5-videos (MIT). The original prompt is credited in-file; this adaptation does not claim the original as Vince's work.*
