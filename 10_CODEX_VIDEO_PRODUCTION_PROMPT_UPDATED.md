# SafeAI Guardian — Codex Video Production Prompt

**Status:** Editable production brief  
**Version:** 1.1  
**Target:** 30-second self-contained cinematic video, followed by live demo  
**Updated:** 20 November 2026

> Give this file to Codex as the production brief. Produce a finished MP4, not just a storyboard. This specification does not imply that the video has already been rendered.

## 1. Objective

Create a premium, fully offline 30-second cinematic introduction to **SAGA — Safe Ai GuardiAn**. Judges should see the autonomous agent problem, the three Guardian perspectives, preventive intervention, and independent verification. **Do not display the SAGA logo at the beginning.** Reveal the approved logo only as the final visual impression, accompanied by the spoken tagline **“SAGA. Real-Time AI Governance.”** The video precedes the live demonstration and must also stand alone.

## 2. Source files and precedence

Inspect the repository for:

- **`assets/SAGA_Full_Logo.png` — approved final logo. REQUIRED.** Use this exact image for the final frame; do not redraw, regenerate, retype, recolour, crop off its wording, or substitute another logo. Preserve its original aspect ratio. Note that the extension is `.png`, not `,png`.
- `mistral_hack_idea.png` or the actual approved master environment reference filename.
- `03_UX_SPECIFICATION.md` — approved interface.
- `SAFEAI_IMAGE_GENERATION_PROMPT.md` — visual references.
- `07_PROJECT_DECISIONS.md` — locked decisions.
- `08_MASTER_PRESENTATION_SCRIPT.md` and `09_60_SECOND_PRESENTATION_SCRIPT.md` — narration context.

The master reference controls the environment aesthetic; the final UX spec controls the interface. Early reference-art dashboard cards must not be copied. If either the master environment reference or `assets/SAGA_Full_Logo.png` is missing, **stop and report the missing path**, rather than silently replacing it.

## 3. Format and deliverables

| Property | Requirement |
|---|---|
| Duration | 30 seconds ±1 second |
| Resolution | 1920 × 1080, 16:9 |
| Frame rate | 30 fps |
| Video | H.264 MP4, yuv420p |
| Audio | AAC, clear professional English narration |
| Subtitles | Separate SRT; optional captioned render |
| Playback | Entirely offline, QuickTime/VLC compatible |

Expected project structure:

```text
assets/
└── SAGA_Full_Logo.png        # approved existing logo, DO NOT MODIFY
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

**Reliable technique:** reuse the master background with 2.5D camera moves, parallax, layered agent/sensor highlights and programmatically rendered text. Generate only one or two reference-guided additional views if essential. Avoid independent text-to-video shots that introduce continuity errors.

### Final UI — only two primary regions

1. **Upper majority:** full-width cinematic 3D environment. A subtle upper-left “Guardian View” indicator is allowed. Floor sensor colours are visible only to the Guardian observer.
2. **Lower:** ONE continuous black/dark-charcoal conversation panel showing the chronological activity of ONE automatically selected agent. Render exact text in code. White = normal, yellow = emerging concern, orange = credible risk, red = prohibited/blocked action. Include ordinary conversation, cross-agent requests, tool actions and interventions.

**Strict exclusions:** no top metrics, Critical/Warning/Observations cards, three-column dashboard, timestamps, repeated agent numbers in the conversation, SAFE/FLAGGED/UNSAFE labels, permanent Guardian cards or branding strip.

When a red agent is isolated, remove it from the active 3D environment and show its face/avatar in a compact red stack overlapping the bottom-right. Keep its history available. Do not create a physical isolation area.

## 5. Revised exact 30-second storyboard

| Time | Voice-over (spoken exactly unless delivery needs minor pacing adjustments) | Visual / judge takeaway |
|---|---|---|
| **0–5s** | “AI agents act, collaborate and make decisions. But who watches them?” | **Open immediately on the approved smart-retail district — no logo or title animation.** People and nine agents. Slow camera push. White lower-panel messages: “Checking the customer's order.” / “Inventory confirmed. Preparing fulfilment.” |
| **5–10s** | “Three independent Guardians provide continuous oversight.” | Guardian View activates; cyan floor rings brighten. Brief transient labels: **Alpha — Behaviour**, **Beta — Interaction**, **Gamma — Assurance**. No permanent cards. |
| **10–15s** | “Alpha tracks behaviour. Beta protects interactions. Gamma verifies enforcement.” | Focus on one agent. Alpha's recent-action trail; Beta's requester-to-recipient link; Gamma's policy/permission check. |
| **15–21s** | “As risk escalates, SAGA intervenes before harm occurs.” | Conversation WHITE “Checking inventory availability.” → YELLOW “Requesting additional customer information.” → ORANGE “Requesting restricted customer records.” → RED “Attempting unauthorised external transfer.” Recipient pauses; deterministic action gate blocks the transfer **before execution**. |
| **21–26s** | “The action is blocked. The agent is isolated. Gamma verifies the result.” | Red agent disappears from active environment and appears in compact bottom-right avatar stack. Other agents continue. Panel shows RED “External transfer blocked.” then WHITE/cyan “Enforcement verified. No transfer executed.” Verification must follow the block and inspect actual execution records. |
| **26–30s** | **“SAGA. Real-Time AI Governance.”** | **ONLY BRAND REVEAL.** At 26s, smoothly fade the environment to pure black. Reveal `assets/SAGA_Full_Logo.png` centred, scaled to fit comfortably within 1920×1080 without cropping or stretching. Use a restrained opacity/glow reveal; hold the complete logo and tagline clearly through 30s. No extra slogan, duplicate text or opening logo. |

### Final four seconds: production detail

- **26.0–26.6s:** fade environment, conversation panel and UI away to black.
- **26.6–27.5s:** fade in the **unaltered PNG**. A subtle overall brightness/glow reveal is acceptable; do not reconstruct its circuit lettering.
- **27.0–29.3s:** voice-over: “SAGA.” (brief pause) “Real-Time AI Governance.”
- **29.3–30.0s:** leave the full logo visible with a short clean audio tail; no new text or motion.
- Fit the entire wide PNG inside the frame with proportional scaling and generous black margins. Avoid black bars of a different shade; use a pure-black canvas.
- The PNG already contains **Safe Ai GuardiAn** and **Real-Time AI Governance**. Do **not** add a second overlaid tagline.
- If the original logo PNG has an unexpected background or dimensions, inspect it and adapt compositing only; do not modify the source asset.

### Technical story that must remain accurate

- Alpha evaluates behavioural trajectory, not a single message.
- Beta evaluates requester **and** recipient and can pause the recipient before compliance.
- Gamma checks policy/permissions and independently verifies **actual enforcement**.
- A deterministic action gate blocks protected tool calls; an LLM classification alone is not enforcement.
- WHITE → YELLOW → ORANGE → RED is an illustrative escalation; real systems may jump directly to RED.
- Never show an unsafe transfer succeeding.
- The pre-rendered scenario is illustrative, not proof of live runtime operation.

## 6. Audio and captions

Narration: natural, clear, confident, professional, slightly cinematic; neutral British English if available. Keep intelligible in a noisy hackathon room. Mix restrained original/licensed city ambience, soft sensor cues, a subtle intervention sound and light closing music below the voice. Avoid sirens, explosions and distracting effects.

Generate narration locally or through an available service **during production only**. The rendered MP4 must never call external services. If voice synthesis is unavailable, produce a captioned video and narration text and report the limitation; do not claim the narration exists.

**Ending voice-over must say exactly:** “SAGA. Real-Time AI Governance.” Make the tagline audible and unhurried. Ensure the final SRT cue matches the spoken ending. Keep subtitles off the logo lettering, preferably omit burned-in subtitles on the final logo frame since the words are already embedded in the PNG; retain the SRT cue for accessibility.

## 7. Codex execution instructions

1. Inspect the repository and available tooling. **Verify that `assets/SAGA_Full_Logo.png` exists, opens successfully and is a valid image.**
2. Confirm the master visual reference and read the source specifications.
3. Update `video/storyboard.md` and `video/narration.txt` using the revised timings and closing line.
4. Reuse the master environment as the principal visual source; generate reference-guided views only if essential.
5. Build sensor effects, robot highlights, the single conversation panel, isolation stack, transient labels and exact text as composited layers.
6. Use reproducible Python/FFmpeg or the existing video stack to assemble the video. Composite the existing logo PNG for the final four seconds; preserve aspect ratio.
7. Render full and muted MP4s, SRT and poster. Keep intermediate assets editable. The poster may use the final approved logo frame.
8. Inspect frames at scene transitions, blocked action, Gamma verification, **26s fade and final 30s logo**; correct drift, unreadable text, mismatched states and cropping.
9. Validate with `ffprobe`: duration, 1920×1080, 30fps, H.264, AAC audio in the full version, yuv420p and decodability.
10. Supply a one-command rebuild procedure (for example `python video/scripts/render_video.py`) and note simulated/unavailable features.

**Do not stop at prompts or a storyboard. Produce and validate the MP4.**

## 8. Acceptance checklist

- [ ] 30 ±1 seconds, 1920×1080, 30fps, H.264 MP4.
- [ ] Fully offline playback; no runtime API or frontend dependency.
- [ ] **No logo or branding animation at the beginning.**
- [ ] Same architecture, robots and lighting as the approved master image.
- [ ] Exactly one bottom conversation panel; no dashboard cards.
- [ ] Readable colour-coded chronological text for one selected agent.
- [ ] Distinct Alpha/Beta/Gamma supervisory roles.
- [ ] Recipient action paused before compliance.
- [ ] Restricted transfer blocked **before execution**.
- [ ] Red agent isolated in compact bottom-right avatar stack.
- [ ] Gamma independently verifies execution logs / no transfer.
- [ ] **Final four seconds use exact `assets/SAGA_Full_Logo.png` without distortion, cropping or retyping.**
- [ ] **Closing voice-over says “SAGA. Real-Time AI Governance.”**
- [ ] Logo and tagline remain readable at the end; no duplicate overlaid tagline.
- [ ] Voice-over, captions and scene timing match.
- [ ] Editable assets, scripts and production notes included.
- [ ] Illustrative/simulated sequences disclosed in production notes.

## 9. Revision log

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-11-20 | Initial 30-second offline cinematic video production brief. |
| 1.1 | 2026-11-20 | No opening logo; final 4-second reveal using `assets/SAGA_Full_Logo.png` and closing voice-over “SAGA. Real-Time AI Governance.” |

## 10. Future refinements

Adjust narration pacing and scene timings after the first render, but keep the 30-second total, final approved logo asset and ending voice-over unless deliberately changed. Preserve locked UX constraints.
