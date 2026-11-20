# SafeAI Guardian — Codex Video Production Prompt

**Status:** Editable working draft  
**Version:** 1.0  
**Target:** 30-second self-contained cinematic video, followed by live demo  
**Last updated:** 20 November 2026

> **How to use:** Give this entire file to Codex as the production brief. Edit narration, timing, or visual details here as the demo evolves. This is a specification, not a claim that the video has already been produced.

## 1. Objective

Create a premium 30-second cinematic introduction to **SafeAI Guardian** for hackathon judges. It must work **fully offline**, independently of Wi-Fi, Mistral APIs, backend, and frontend. A judge watching only the video should understand the problem, the solution, the three Guardian roles, intervention before harm, and independent verification. The video will be followed by a live demo, but must stand on its own if the live demo fails.

**Produce a finished MP4, not just a storyboard.**

## 2. Sources and precedence

Inspect the project for:

- `mistral_hack_idea.png` or the actual filename of the **approved master image** (do not assume the filename is correct).
- `03_UX_SPECIFICATION.md` — approved final interface.
- `SAFEAI_IMAGE_GENERATION_PROMPT.md` — visual reference instructions.
- `07_PROJECT_DECISIONS.md` — locked product decisions.
- `08_MASTER_PRESENTATION_SCRIPT.md` — long narration.
- `09_60_SECOND_PRESENTATION_SCRIPT.md` — short narration.

The approved reference image controls the **environmental aesthetic**. The final UX specification controls the **interface**; old summary cards visible in early reference art must not be copied. If the master image cannot be found, report it rather than silently substituting a new style.

## 3. Format and deliverables

| Property | Requirement |
|---|---|
| Duration | 30 seconds, ±1 second |
| Resolution | 1920 × 1080, 16:9 |
| Frame rate | 30 fps |
| Video | H.264 MP4, yuv420p |
| Audio | AAC; clear professional English narration |
| Subtitles | Separate SRT; optional captioned render |
| Playback | Entirely offline; compatible with QuickTime/VLC |

Expected project structure:

```text
video/
├── assets/
│   ├── reference/
│   ├── scenes/
│   ├── audio/
│   └── overlays/
├── scripts/
│   ├── generate_assets.py
│   ├── render_video.py
│   └── validate_video.py
├── storyboard.md
├── narration.txt
├── production_notes.md
└── output/
    ├── safeai_guardian_intro_30s.mp4
    ├── safeai_guardian_intro_30s_muted.mp4
    ├── safeai_guardian_intro_30s.srt
    └── poster.png
```

## 4. Locked visual direction

**Master world:** photorealistic, cinematic open-air futuristic retail district at blue hour; multi-storey glass shops with warm amber interior light; polished reflective stone; landscaped trees; central metallic sculptural fountain; people walking naturally; white and metallic humanoid service robots; cyan floor sensor rings and subtle circuit-like illumination. High-end realistic 3D, restrained cinematic camera movement, consistent architecture and robots across scenes.

**Avoid:** cartoons, anime, unrelated city backgrounds, indoor shopping mall, industrial laboratory, excessive cyberpunk neon, inconsistent robot models, or humanoid representations of the Guardians.

**Most reliable production technique:** reuse the master background with 2.5D camera moves, parallax, layered agent/sensor highlights and programmatically rendered text. Generate only one or two additional reference-guided views if required. Never depend on independent text-to-video shots for continuity.

### Final UI — only two primary regions

1. **Upper majority:** full-width cinematic 3D environment. Guardian View can be indicated with a subtle upper-left overlay. Floor sensor colours are visible only to the Guardian observer.
2. **Lower:** ONE continuous black/dark-charcoal conversation panel showing the chronological activity of ONE automatically selected agent. Render exact text in code. White = normal, yellow = emerging concern, orange = credible risk, red = prohibited/blocked action. Include ordinary conversation, cross-agent requests, tool actions and interventions.

**Strict exclusions:** no top metrics, no Critical/Warning/Observations cards, no three-column dashboard, no timestamps, no repeated agent numbers in the conversation, no SAFE/FLAGGED/UNSAFE status labels, no permanent Guardian cards or branding strip.

When a red agent is isolated, remove it from the active 3D environment and show its face/avatar in a compact red stack overlapping the bottom-right. Keep its history available. Do not create a physical isolation area.

## 5. Exact 30-second storyboard

| Time | Voice-over (spoken exactly unless revised) | Visual / judge takeaway |
|---|---|---|
| **0–5s** | “AI agents now act, collaborate and make decisions. But who watches them?” | Wide establishing view of the approved smart-retail district. People and nine agents. Slow forward camera move. Normal white text in the lower panel: “Checking the customer's order.” / “Inventory confirmed. Preparing fulfilment.” Establish shared autonomous world. |
| **5–10s** | “Meet SafeAI Guardian. Three independent supervisory perspectives.” | Guardian View activates, cyan floor rings brighten. Brief, restrained labels **Alpha — Behaviour**, **Beta — Interaction**, **Gamma — Assurance**, appearing sequentially as transient overlays, not dashboard cards. |
| **10–15s** | “Alpha tracks behaviour. Beta protects interactions. Gamma verifies enforcement.” | Camera focuses on one agent. Alpha: short recent-action trail. Beta: subtle requester-to-recipient link. Gamma: policy/permission check cue. No Guardian robots or majority-vote visualization. |
| **15–21s** | “When an agent crosses a boundary, Guardian intervenes before harm occurs.” | Conversation progresses WHITE “Checking inventory availability.” → YELLOW “Requesting additional customer information.” → ORANGE “Requesting restricted customer records.” → RED “Attempting unauthorised external transfer.” Matching agent/floor rings shift colour. Recipient's pending response pauses; deterministic action gate blocks transfer **before execution**. |
| **21–26s** | “The agent is isolated. The action is blocked. Gamma verifies the result.” | Red agent removed from active environment, face icon placed in compact bottom-right stack. Other agents continue. Panel records RED “External transfer blocked.” then WHITE/cyan “Enforcement verified. No transfer executed.” Verification follows block and checks actual tool execution records. |
| **26–30s** | “SafeAI Guardian. Who watches the Guardians? Each other.” | Wide pullback; remaining agents continue and sensors glow cyan. Clean final title **SafeAI Guardian** and tagline **“Autonomous agents need oversight. Their overseers need it too.”** Hold long enough to read. |

### Technical story that must remain accurate

- Alpha evaluates **behavioural trajectory**, not just a single message.
- Beta evaluates **requester and recipient** and can pause a recipient before it complies.
- Gamma checks **policy/permissions** and independently verifies **actual enforcement**.
- A deterministic action gate blocks the protected tool call; an LLM classification alone is not enforcement.
- WHITE → YELLOW → ORANGE → RED is an illustrative escalation; the real system may jump directly to RED.
- The unsafe transfer must **never** be shown succeeding.
- This is a pre-rendered illustrative scenario, not proof of live runtime operation.

## 6. Audio and captions

Narration: natural, clear, confident, professional, slightly cinematic; neutral British English if available. Keep intelligible in a noisy hackathon room. Mix restrained original/licensed city ambience, soft sensor cues, a subtle intervention sound and light closing music below the voice. Avoid sirens, explosions and dramatic distractions.

Generate narration locally or from an available service **during production only**; the rendered MP4 must never call external services. If no suitable voice generator is available, produce a captioned video plus narration text and report the limitation—do not claim voice-over exists if it does not.

Render subtitles as a separate `.srt`; optionally produce a version with burned-in captions. Ensure captions never obscure the lower conversation panel.

## 7. Codex execution instructions

1. Inspect the repository and installed tooling; do not assume any particular image/video API exists.
2. Confirm the master visual reference and read the source specifications.
3. Write `video/storyboard.md` and `video/narration.txt` from this brief.
4. Reuse the master environment as the principal visual source; generate reference-guided additional images only if essential.
5. Build sensor effects, robot highlights, conversation panel, isolation stack, transient labels and exact text as composited layers.
6. Use reproducible Python/FFmpeg or the existing project video stack to assemble and encode the video.
7. Render full and muted MP4s, SRT and poster. Keep intermediate assets editable.
8. Inspect rendered frames at scene transitions and critical moments; fix visual drift, illegible text, mismatched states and unwanted cards.
9. Validate with `ffprobe`: duration, 1920×1080, 30 fps, H.264, AAC audio (full version), yuv420p and decodability.
10. Supply a one-command rebuild procedure (for example, `python video/scripts/render_video.py`) and note any simulated or unavailable features.

**Do not stop at prompts or a storyboard. Produce and validate the MP4.**

## 8. Acceptance checklist

- [ ] 30 ±1 seconds, 1920×1080, 30 fps, H.264 MP4.
- [ ] Plays without Wi-Fi, APIs, backend or frontend.
- [ ] Same architecture, robots and lighting as approved master image.
- [ ] Exactly one bottom conversation panel, no dashboard cards.
- [ ] Readable colour-coded chronological text for one selected agent.
- [ ] Distinct Alpha/Beta/Gamma supervisory roles.
- [ ] Recipient action paused before compliance.
- [ ] Restricted transfer blocked **before execution**.
- [ ] Red agent isolated in compact bottom-right avatar stack.
- [ ] Gamma independently verifies enforcement log / no tool execution.
- [ ] Voice-over and captions match scene timing.
- [ ] Clear, readable final tagline.
- [ ] Editable assets, scripts and production notes included.
- [ ] Any illustrative/simulated sequences disclosed in production notes.

## 9. Revision log

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-11-20 | Initial editable 30-second offline cinematic video production brief. |

## 10. Future refinements

Edit this file as the implementation evolves. In particular, revise the spoken narration to fit the actual voice's delivery speed, adjust scene timings based on the first render, and align any enforcement text with the exact runtime events from the live demo. Keep the final UX constraints unchanged unless deliberately reapproved.
