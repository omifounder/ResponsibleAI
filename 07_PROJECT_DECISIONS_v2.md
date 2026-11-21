# SAGA — Project Decisions Register

**Version 2.0 | 20 November 2026**

**Provenance:** This is a reconstructed decision register from the agreed conversation and the available video brief. The original `07_PROJECT_DECISIONS.md` could not be retrieved; do not treat this as a line-by-line revision of that file.

## Locked decisions
| ID | Decision | Consequence |
|---|---|---|
| D01 | Product is SAGA / SafeAI Guardian; public tagline “Real-Time AI Governance.” | No alternate opening wordmark; logo at end only |
| D02 | Video is 30 s, 1920×1080, 30 fps, offline H.264 | Preview before final render |
| D03 | Exactly five approved image references | Use paths listed below, no substitution |
| D04 | Opening empty plaza → populated plaza → live monitoring → investigation → logo | Fixed scene order |
| D05 | Five visible numbered robots: 2, 4, 6, 8, 9 | Preserve identities, natural distinct movement |
| D06 | Agent 6 white/yellow/orange/red; Agent 4 to orange; Agent 8 to yellow; 2 and 9 white | Ring/body/feed colour synchronisation |
| D07 | Live screen has two independently scrolling panels, Agent 6 left and Agent 4 right | Supersedes one-panel 82%/18% decision |
| D08 | Italic conversation text; roughly three lines per panel | No timestamps or metric footer |
| D09 | Yellow and orange are both called “Warning” | Internal four-step severity remains |
| D10 | Agent 6 attempted restricted-data transfer is blocked before execution | No successful transfer depicted |
| D11 | Full-screen Agent 6 investigation with history and three Guardian cards | Uses image 4, 16:9 |
| D12 | Guardian-1 behaviour, Guardian-2 recipient safety, Guardian-3 policy and assurance | Supersedes Alpha/Beta/Gamma user-facing names |
| D13 | Deterministic aggregation, not majority vote | Guardian-2 unsafe + confirmed prohibition ⇒ BLOCK |
| D14 | Guardian-3 verification is separately recorded after gate enforcement | Do not confuse assessment with verification |
| D15 | Last scene black with official SAGA logo and spoken tagline | No opening logo |

## Approved assets
1. `assets/1_Futuristic_Shopping_Plaza_empty.png` — empty mall.
2. `assets/2_Futuristic_Shopping_Plaza_Agents.png` — populated mall with numbered robots 2, 4, 6, 8, 9.
3. `assets/3_Realtime_Agent_Monitoring.png` — live monitoring layout, Agent 6 left / Agent 4 right.
4. `assets/4_Guardian_Assessment.png` — full-screen Agent 6 investigation, Guardian-1/2/3.
5. `assets/5_SAGA_Full_Logo.png` — closing logo on black.

## Cinematic timing
0–3 s empty; 3–7 s populated; 7–17 s two live feeds and escalation; 17–22 s Agent 6 block and freeze; 22–27 s investigation and disagreement; 27–30 s logo. Timing may be adjusted only with explicit approval if readability suffers.

## Superseded proposals
Single-agent live panel; Alpha/Beta/Gamma labels; Agent 4 permanently white; three dashboard summary cards; physical isolation zone; old `mistral_hack_*` filenames; an alternate top-left SAGA title; opening logo; video generated from unrelated mall images.

## Open engineering questions (not design approvals)
- Can the existing stills support credible independent walking animation without obvious artifacts? If not, limit movement and report constraints.
- Are live event/gate logs wired to real code or simulated? Label accurately.
- Are font sizes readable at 1080p when the investigation holds for five seconds? Validate preview.
