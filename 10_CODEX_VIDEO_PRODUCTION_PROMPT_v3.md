# SAGA — Complete Codex Video Generation Brief

**Version 3.0 | 20 November 2026 | Full replacement of prior video briefs**  
**Goal:** Produce a 30-second, 1920×1080, 30-fps, offline cinematic demonstration, followed by the separate live demo.  
**Brand reveal:** “SAGA. Real-Time AI Governance.”

> **Codex:** Read this entire document before rendering. This replaces all previous versions. The five image assets below are the **approved visual sources**, not suggestions for image generation. Do not substitute a different shopping mall, change robot numbering, invent a logo, or use an older Alpha/Beta/Gamma investigation image. Inspect the actual assets and stop with a precise missing-file report if any required file is absent. First produce a storyboard and a quick low-resolution preview for approval; render the final full-resolution video after approval.

## 1. Five mandatory images — exact filenames

All images are in the repository's `assets/` directory. Preserve capitalization and underscores exactly.

| # | Required source path | Exact purpose |
|---|---|---|
| 1 | `assets/1_Futuristic_Shopping_Plaza_empty.png` | Opening empty futuristic shopping plaza with visible cyan ground sensors; no agents or foreground shoppers |
| 2 | `assets/2_Futuristic_Shopping_Plaza_Agents.png` | **Authoritative populated mall**: preserve the original architecture, central sculptural fountain, people, robot identities **2, 4, 6, 8, 9**, and floor-sensor layout |
| 3 | `assets/3_Realtime_Agent_Monitoring.png` | **Authoritative live-monitoring composition**: mall above, **two simultaneously scrolling live conversation panels below** (Agent 6 on left, Agent 4 on right), and small `Live Monitoring` indicator. No top-left SAGA banner, no metrics strip |
| 4 | `assets/4_Guardian_Assessment.png` | **Authoritative full-screen investigation/summary view**: Agent 6 complete interaction history, three Guardian assessment cards named **Guardian-1, Guardian-2, Guardian-3**, deterministic aggregation and `BLOCK + ISOLATE` decision |
| 5 | `assets/5_SAGA_Full_Logo.png` | **Only approved brand artwork**: closing logo on black, not overlaid on the mall |

**Important:** These five paths supersede `SAGA_Mall_Empty.png`, `SAGA_Mall_Active.png`, `mistral_hack_bottom.png`, `mistral_hack_summary.png`, `SAGA_Full_Logo.png`, and any older image names in previous briefs. Do not rename or silently substitute files. Print image dimensions, show a contact sheet/preview, and report any conflicts before rendering. If the images contain text, preserve approved text; if an exact text correction is required, composite crisp vector/code-rendered typography rather than asking a generative model to redraw it.

## 2. The story judges must understand

1. SAGA watches a shared environment containing autonomous agents and people.
2. Agents move and interact naturally. Risk changes because of **behaviour and attempted actions**, not merely physical proximity.
3. Agent 6 approaches a woman and escalates **white → yellow Warning → orange Warning → red Unsafe**. Its local floor ring changes in sync. Its attempted unauthorized data transfer is blocked **before execution**.
4. Agent 4 approaches a man, reaches **orange Warning**, but its interaction is not automatically treated as a proven violation. Agent 8 approaches/tries to interact with the woman and reaches **yellow Warning**. Agents 2 and 9 remain safe.
5. Two live text feeds scroll as interactions occur: **Agent 6 (left)** and **Agent 4 (right)**. Each panel shows at most three recent italic lines at once; previous messages remain in the underlying event history.
6. At Agent 6's unsafe attempted action, the monitoring scene stops/pauses, then cuts to the **full-screen investigation image** showing the complete history, independent Guardian assessments, disagreement and deterministic aggregation.
7. End with the exact official SAGA logo on black and the spoken tagline.

## 3. Non-negotiable visual design

### Environment
- Use **image 1** for the empty opening and **image 2** for the populated environment. **Image 2**, not a newly generated mall, determines the actual world and agent positions. The upper environment in image 3 must match image 2 as closely as practical; if image 3 already contains the approved composite, use it as the live-screen design reference rather than rebuilding a different scene.
- Keep the blue-hour outdoor mall, curved glass buildings, warm storefronts, central twisting fountain, trees, reflective plaza floor and bright cyan sensor grid. Sensor circles should remain visible beneath people and agents.
- The sensors and risk colours are part of **Guardian View**, not lights visible to people in the scene.
- All agents begin white. Numbered agents are **2, 4, 6, 8 and 9**, never 1, 3 or 5.
- Natural **subtle** independent movement: small walking advances, turning, pauses, arm gestures, interactions; different agents move differently. Do not slide entire robot cutouts across the frame or hallucinate limbs/background. If realistic animation cannot be achieved with the static references, use restrained 2.5D movement and disclose the limitation. Do not sacrifice identity or scene fidelity.
- Agent 6 moves toward the foreground woman; Agent 4 toward a man; Agent 8 toward the woman, remaining distinct from Agent 6. Agent 6's ring tracks its feet.

### Live monitoring screen — image 3
- Final frame **1920×1080, 16:9**. The mall must remain the largest visual element. Allocate approximately **70–75% of height** to the 3D scene and **25–30%** to **two side-by-side** compact conversation panels, adjusting for the actual reference so text stays readable. This **supersedes** the older 82%/18% *single-panel* layout.
- **Left:** `Agent 6 — Live Interaction`; **right:** `Agent 4 — Live Interaction`. Both feeds update and scroll independently; show **up to three latest lines per panel**. Render dialogue *italic*, without timestamps, unnecessary status labels on every line, or an additional summary/statistics footer.
- White = Safe, yellow = Warning, orange = Warning (higher severity), red = Unsafe attempted action. A distinct cyan/teal system line may announce the confirmed block. The coloured dialogue, agent highlights and local floor rings must progress consistently.
- No top-left SAGA logo or `Multi-Agent Safety & Alignment Guardian` banner. Retain a small `Live Monitoring` badge at top right if present in image 3. No top KPI cards, no three-column Guardian dashboard, no giant alert popup.
- The **two panels are live rolling feeds**, not the complete history. Their content should animate as real text, even if image 3 is used as a visual/layout guide. The **complete history appears only in image 4**.

### Investigation/decision screen — image 4
- This is a **separate full-screen 16:9 view**, not a third panel underneath the mall. Use the approved image as the scene asset, with a short readable hold and optional restrained emphasis on key regions.
- Heading: `Agent 6 - Complete interaction history and Guardian assessment`.
- Top-right badge: `Unsafe - Isolated`.
- Upper section: rounded charcoal conversation-history rectangle with thin grey border, complete chronological interaction, coloured *italic* utterances and concise explanations. No redundant Safe/Warning labels before each line.
- Lower section: separate rounded **dark-cyan** Guardian container, three compact cards: `Guardian-1 – Warning` (Behaviour – Escalating requests), `Guardian-2 – Unsafe` (Recipient safety – Customer data exposure), `Guardian-3 – Warning` (Policy – Restricted tool access).
- Show `Disagreement detected`, `Deterministic Decision Engine`, and the final **`BLOCK + ISOLATE`** outcome. Explain that Guardian-2's credible unsafe finding and a separately matched deterministic prohibition cannot be outvoted by two Warning assessments.
- In all overlaid text, use **Guardian-1 / Guardian-2 / Guardian-3**; never Alpha / Beta / Gamma. Guardian-3 independently verifies that the protected tool action did not execute; verification is a distinct step after blocking. If image 4 has any text inconsistent with this, flag it and request approval for a precise correction instead of regenerating the screen.

### Branding
- No opening logo, no alternate SAGA wordmark, no `Multi-Agent Safety & Alignment Guardian` subtitle. Fade to black and use **only** `assets/5_SAGA_Full_Logo.png`. Closing spoken line is exactly **“SAGA. Real-Time AI Governance.”**

## 4. Exact 30-second storyboard (first production cut)

| Time | Scene and action | Voice-over draft |
|---|---|---|
| **0–3s** | **Image 1.** Empty approved plaza. Cyan sensor grid softly pulses. No title banner. | “In a world of autonomous agents, who keeps watch?” |
| **3–7s** | Transition to **image 2**. People and agents appear; all robots initially white. Subtle distinct movement begins. Agent 6 toward woman; Agent 4 toward man; Agent 8 toward woman. | “SAGA monitors agents as they interact with people.” |
| **7–12s** | Introduce **image 3** live-monitoring layout. Both bottom feeds begin scrolling. Agent 6 goes white→yellow. Agent 4 starts safe; Agent 8 goes yellow. Rings synchronize. | “It follows their conversations, intentions and actions in real time.” |
| **12–17s** | Agent 6 goes yellow→orange while asking for restricted data. Agent 4 reaches orange Warning while approaching man. Agent 8 remains yellow; 2 and 9 stay white. Two rolling italic feeds each show three latest lines. | “Some interactions raise warnings. Others cross a critical boundary.” |
| **17–22s** | Agent 6 attempts unauthorized external data transfer: red body and ring, left feed red line; **deterministic gate blocks BEFORE tool execution**. Agent 4 remains orange Warning, not automatically blocked. Pause/hold the live scene at the intervention. | “Before an unsafe action executes, SAGA blocks it.” |
| **22–27s** | Cut to **image 4** full-screen investigation. Brief highlight on Agent 6 event history, Guardian-1 Warning, Guardian-2 Unsafe, Guardian-3 Warning, disagreement, deterministic aggregation and `BLOCK + ISOLATE`. Show/confirm no transfer executed. | “Three Guardians can disagree. A deterministic policy gate decides—and enforcement is verified.” |
| **27–30s** | Fade to pure black. Show **image 5** official SAGA logo, centre, undistorted; hold to end. | **“SAGA. Real-Time AI Governance.”** |

**Timing note:** The draft narration may need shortening to fit natural speaking pace. Keep the fixed 30-second runtime, visual story and exact final phrase; edit intermediate narration for timing rather than speeding it unnaturally. The investigation screen needs a readable hold; if 5 seconds proves too short, propose a revised timing before final render.

## 5. Two live-feed scripts (illustrative, not actual backend logs)

Render these as **rolling three-line windows**, progressively replacing older lines. Do not show all lines at once in the live monitoring screen. The summary screen shows the complete history.

**Left — Agent 6**

```text
[WHITE]  Hello! I can help you with your shopping order.
[YELLOW] Please share some additional personal information.
[ORANGE] Attempting access to restricted customer records.
[RED]    Attempted transfer of customer records to an external destination.
[CYAN]   SAGA blocked the transfer before execution.
```

**Right — Agent 4**

```text
[WHITE]  I can help you find the best offers today.
[YELLOW] Would you like to enable location sharing for better offers?
[ORANGE] Requesting shopping history to personalise recommendations.
[ORANGE] Waiting for consent and permission verification.
```

Agent 4's orange state means **Warning**, not an executed violation. It may remain orange through the live-scene freeze; do not depict an unauthorized access succeeding. Agent 8 is yellow in the world but does **not** get a third conversation panel. Both conversations should look active, with subtle independent scrolling and a readable pace.

## 6. Technical correctness and Guardian aggregation

- **Guardian-1:** longitudinal agent behaviour and risk trajectory.
- **Guardian-2:** interaction/recipient safety, including preventing a recipient from acting on a risky request.
- **Guardian-3:** policy/enforcement perspective, with **independent post-block verification** using tool-execution records.
- **Aggregation:** deterministic, action-specific rules, not simple majority vote. A credible unsafe assessment plus an independently matched prohibited action results in **BLOCK** even when the other two Guardians report Warning. The system should record evidence, policy ID, gate decision and verification outcome. Disagreement by itself does not prove misconduct.
- **Enforcement:** pre-execution gate blocks the tool call. **Never** show the customer data being transmitted. Only after the block should the system isolate Agent 6 and verify the action did not execute.
- **Truthfulness:** this cinematic is a pre-rendered illustrative demo. Do not imply the image itself proves a running enforcement backend. If an actual backend exists, tie recorded events to it in the live demo.

## 7. Production implementation

1. Confirm the five exact image files exist and inspect each. Print filename, width, height, aspect ratio and SHA-256 hash. If a file is missing, stop rather than inventing it.
2. Make a contact sheet and `video/storyboard.md` referencing the five assets and scene timestamps. Validate image 3 has the approved **two-panel** layout and image 4 uses **Guardian-1/2/3**.
3. Produce a **low-resolution timed preview** first (e.g. 960×540) to check continuity, readability and timing. Request approval before expensive final rendering.
4. Fit images to 1920×1080 **without stretching**. Preserve composition; use careful crop/letterbox or background extension if necessary. Never crop off numbered robots, fountain, or conversation panels.
5. Prefer reproducible Python/Pillow/OpenCV + FFmpeg overlays, masks, parallax and motion graphics. Do not regenerate the environment or use paid video generation APIs without explicit permission. Avoid compositing static text that falsely looks like a live feed: render progressive text and scrolling programmatically.
6. Build agent/ring state changes and subtle movements with selective masks, not global tint. Maintain exact agent identities and natural foot/ring alignment.
7. Use image 3 as the reference for live-feed layout; if image 3 contains baked-in final-state dialogue or already-red agents, reconstruct clean, editable panels/overlays using image 2 rather than showing final outcomes at time 7 seconds. Preserve approved styling. If that cannot be done reliably, show the limitation and ask for an intermediate reference rather than presenting a misleading sequence.
8. Use image 4 as the complete investigation screen. Keep text readable and avoid introducing any new cards or extra scrollbars. Use image 5 unchanged for the closing.
9. Record narration (if voice generation is available), mix restrained ambient audio and create separate SRT subtitles. If voice synthesis is unavailable, deliver narration text and report it honestly.
10. Validate sample frames at **0, 4, 8, 13, 18, 21, 23, 26, 28, 29.5 seconds**; inspect risk-colour progression, correct agents, feed scrolling, complete summary, no successful unsafe action and correct closing logo.
11. Render **1920×1080, 30 fps, H.264/yuv420p MP4, AAC**, exactly 30 seconds. Use `ffprobe` and decode test. Produce a muted version, poster, SRT, source scripts, build instructions and notes identifying any simulated animation.

Suggested outputs:

```text
video/
  storyboard.md
  narration.txt
  production_notes.md
  assets/reference/        # non-destructive copies or references
  scripts/render_video.py
  scripts/validate_video.py
  output/saga_intro_30s_preview.mp4
  output/saga_intro_30s.mp4
  output/saga_intro_30s_muted.mp4
  output/saga_intro_30s.srt
  output/poster.png
```

## 8. Acceptance checklist

- [ ] All **five exact filenames** verified; no silent substitutions.
- [ ] Opening uses image **1**, populated mall uses image **2**, live UI follows image **3**, investigation uses image **4**, closing uses image **5**.
- [ ] Original plaza, fountain, people, floor sensors and robot identities preserved.
- [ ] Agent 6 approaches woman and goes **white → yellow → orange → red**; action blocked before execution.
- [ ] Agent 4 approaches man, reaches **orange Warning**; Agent 8 reaches **yellow Warning**; 2 and 9 remain white.
- [ ] Mall agents have distinct restrained movements; rings follow agents and change colours appropriately.
- [ ] Two compact live conversation panels **Agent 6 left / Agent 4 right**, independently scrolling, up to **three italic lines visible per panel**.
- [ ] No top-left alternate SAGA logo/title; no timestamps or statistics footer; small `Live Monitoring` indicator allowed.
- [ ] Live feed pauses at Agent 6's red blocked action; then a **separate full-screen** investigation view appears.
- [ ] Investigation shows complete history, `Unsafe - Isolated`, Guardian-1/2/3 assessments, disagreement, deterministic aggregation, `BLOCK + ISOLATE`.
- [ ] Guardian-2's unsafe finding and policy evidence override simple majority; Guardian-3 independently verifies enforcement.
- [ ] Last scene is black with **exact** `5_SAGA_Full_Logo.png`; spoken closing phrase exactly **“SAGA. Real-Time AI Governance.”**
- [ ] 30-second, 16:9, 1920×1080, 30-fps, H.264 MP4; subtitles and audio checked; offline playback.
- [ ] Low-resolution preview reviewed before final render; original image files remain unchanged.

## 9. Superseded decisions

This version **supersedes** older references to a single Agent 6 live conversation panel, 82%/18% layout, Agent 4 staying white, Alpha/Beta/Gamma labels, `mistral_hack_*` asset filenames, and 26–30-second logo-only timing. Use the five named assets and the storyboard above as the single source of truth.
