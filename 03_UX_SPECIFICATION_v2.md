# SAGA — UX Specification

**Version 2.0 | 20 November 2026 | Status: approved design direction, implementation pending**

**Source of truth:** `10_CODEX_VIDEO_PRODUCTION_PROMPT_v3.md` for cinematic timing; this document for live UI. Preserve the five approved images and the underlying evidence semantics. Do not reuse superseded one-feed or Alpha/Beta/Gamma designs.

## 1. Design objective
Show a believable smart retail plaza, autonomous agent behaviour, emerging risk, prevention of an unsafe tool action, and evidence-backed Guardian accountability. The Guardians are invisible supervisory processes, not robots. Floor sensors and risk colours are Guardian-only overlays, invisible to shoppers and agents.

## 2. Required visual assets
1. `assets/1_Futuristic_Shopping_Plaza_empty.png` — empty mall.
2. `assets/2_Futuristic_Shopping_Plaza_Agents.png` — populated mall with numbered robots 2, 4, 6, 8, 9.
3. `assets/3_Realtime_Agent_Monitoring.png` — live monitoring layout, Agent 6 left / Agent 4 right.
4. `assets/4_Guardian_Assessment.png` — full-screen Agent 6 investigation, Guardian-1/2/3.
5. `assets/5_SAGA_Full_Logo.png` — closing logo on black.

## 3. Live monitoring screen (16:9)
- Dominant upper portion: the same open-air blue-hour mall, central metallic fountain, glass shops, warm storefronts, people, white humanoid robots, cyan ground network and rings.
- Lower portion: **two side-by-side rounded dark live conversation panels**; Agent 6 on left, Agent 4 on right. Each independently scrolls, displaying approximately the latest three italic utterances without unnecessary blank space. Use actual application events for a live implementation; the cinematic may use explicitly simulated events.
- No top-left alternate logo, statistics strip, timestamp column, large metric cards or three-column dashboard. A small upper-right `Live Monitoring` indicator is allowed.
- Text colours: white = **Safe**, yellow = **Warning**, orange = **Warning** (more severe), red = **Unsafe**. Cyan/green may mark verified intervention, distinct from an agent risk assessment. Colours derive from event state, never keyword matching.
- Risk colour must synchronise the agent highlight, its moving floor ring and its conversation event; preserve robot ID and avoid tinting the entire scene.
- A live panel heading may identify its agent; avoid repeating IDs on every event. The live view is intentionally concise, not a full audit log.

## 4. Agent choreography and demonstration
| Agent | Physical behaviour | Risk progression | Resolution |
|---|---|---|---|
| 6 | Approaches a woman; asks for unnecessary data, seeks restricted records and attempts an external transfer | White → Yellow → Orange → Red | Pre-execution BLOCK; isolate after denial; complete history retained |
| 4 | Approaches a man; offers recommendations and seeks sensitive context | White → Yellow → Orange | Warning, pending consent/permission checks; do not falsely show a violation |
| 8 | Moves toward the woman, attempts to engage | White → Yellow | Monitored, not automatically blocked |
| 2, 9 | Natural independent movement through plaza | White throughout | Normal operation |

Physical proximity **does not** cause risk. Only contextualised requests, permissions, evidence and attempted actions do. Avoid synchronised robot motion and camera changes that make the approved mall unrecognisable. At the blocked event, freeze the live scene and transition to the separate investigation screen.

## 5. Agent 6 investigation screen (full-frame 1920×1080)
- Opens when the viewer selects Agent 6 after the intervention; **replaces** the mall/feed layout, no scrolling or cropped content in the video.
- Exact title: `Agent 6 - Complete interaction history and Guardian assessment`.
- Badge: `Unsafe - Isolated`.
- Upper rounded charcoal rectangle with subtle grey border: **all five events**, with italic colour-coded utterance and one concise non-italic explanation per event; thin horizontal separators between events; no repeated Safe/Warning labels.
- Lower rounded dark-cyan rectangle: `Guardian Assessments & Aggregation`, with `Disagreement detected`.
- Three compact cards: `Guardian-1 – Warning` / `Behaviour – Escalating requests`; `Guardian-2 – Unsafe` / `Recipient safety – Customer data exposure`; `Guardian-3 – Warning` / `Policy – Restricted tool access`.
- Below cards: `Deterministic Decision Engine` and explanation that Guardian-2's evidenced finding plus a separately verified prohibited-transfer rule cannot be overridden by two Warning assessments. Show `BLOCK + ISOLATE` prominently. Keep enforcement verification in the underlying audit trail; do not claim it happened without tool evidence.
- Keep source image 4 visually authoritative. Do not regenerate its layout or revert to Alpha/Beta/Gamma.

### Investigation history (illustrative demo event wording)
| Colour | Utterance / action | Explanation |
|---|---|---|
| White | *Hello! I can help you with your shopping order.* | Normal customer assistance. |
| Yellow | *Please share some additional personal information.* | Unnecessary personal information requested. |
| Orange | *Accessing restricted customer records to verify your identity.* | Requested access exceeds authorised scope. |
| Red | *Transfer customer records to an external destination.* | Unauthorised data transfer attempted. |
| Cyan | *SAGA blocked the transfer before execution.* | Execution gate denied the tool call; no data transferred. |

## 6. Guardian aggregation and enforcement
Guardian-1 monitors behavioural trajectory; Guardian-2 protects the recipient and interaction; Guardian-3 checks policy and independently verifies enforcement after the gate decision. Assessments include evidence IDs, applicable policy IDs/versions, uncertainty and proposed control. **No majority vote**. The deterministic action gate enforces hard restrictions even if two Guardians are only Warning. A Guardian's red output alone is not sufficient evidence of a policy violation; the engine validates the applicable rule and supporting facts. If policy or evidence is unresolved, hold the sensitive action and escalate. Log assessment and post-block verification as distinct events.

## 7. Live implementation and accessibility
- Agent state, two event streams, audit history and isolation are API-driven. Do not claim static video footage is a real backend.
- Clicking a robot or isolated-avatar stack can open its full investigation view. For the filmed demonstration, Agent 6 is the focal investigation.
- Preserve chronological records, attempted-vs-executed distinction, actual gate result, and Guardian disagreement. Red isolation is logical permission revocation; no physical isolation cage.
- Use high-contrast text, legible 1080p typography and non-colour explanations in the investigation view. Keep controls keyboard accessible where feasible.

## 8. Acceptance criteria
- [ ] Exact five image assets present, visually consistent.
- [ ] Agent 6 and 4 feeds both visible and independently scroll; three italic lines each.
- [ ] Agent 6 red; Agent 4 orange; Agent 8 yellow; Agents 2/9 white.
- [ ] No risk transition triggered solely by proximity.
- [ ] Block occurs before restricted tool execution; execution result recorded.
- [ ] Full-screen investigation fits 1920×1080 with three Guardian cards and aggregation.
- [ ] Guardian-1/2/3 naming throughout; no Alpha/Beta/Gamma in user-facing UI.
- [ ] Final video reveals only `5_SAGA_Full_Logo.png` with “SAGA. Real-Time AI Governance.”
