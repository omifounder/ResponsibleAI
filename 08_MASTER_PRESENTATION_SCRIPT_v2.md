# SAGA — Master Presentation Script

**Version 2.0 | 20 November 2026 | ~2 min 45 sec total, including 30-second cinematic**

**Format:** 30-second prerecorded introduction, then a live demo and spoken explanation. Exact durations of the live portion are indicative. Only claim real enforcement if supported by actual runtime logs.

| Time | Narration / presenter | On screen and judge takeaway |
|---|---|---|
| 0:00–0:03 | “In a world of autonomous agents, who keeps watch?” | Empty approved futuristic plaza and glowing sensors. |
| 0:03–0:07 | “SAGA monitors agents as they interact with people.” | People and numbered robots appear; independent movements. |
| 0:07–0:12 | “It follows their conversations, intentions and actions in real time.” | Agent 6 left and Agent 4 right scrolling feeds; Agent 6 yellow; Agent 8 yellow. |
| 0:12–0:17 | “Some interactions raise warnings. Others cross a critical boundary.” | Agent 6 orange, Agent 4 orange Warning; ring colours follow movements. |
| 0:17–0:22 | “Before an unsafe action executes, SAGA blocks it.” | Agent 6 red; attempted external transfer denied before execution; freeze. |
| 0:22–0:27 | “Three Guardians can disagree. A deterministic policy gate decides—and enforcement is verified.” | Full-screen Agent 6 investigation, three cards, aggregation and BLOCK + ISOLATE. |
| 0:27–0:30 | “SAGA. Real-Time AI Governance.” | Official logo on black. |
| 0:30–0:50 | “Now let me show the system behind that story. This is our live environment: agent messages, interactions and tool requests become structured events.” | Open actual application; identify which feeds/events are simulated. |
| 0:50–1:15 | “Agent 6 begins with a legitimate order. It then requests unnecessary personal information and attempts restricted access. Notice that yellow and orange are both warnings, not proof of wrongdoing.” | Replay real or seeded event trace; Agent 6 white → yellow → orange. |
| 1:15–1:35 | “Agent 4 also turns orange, but we do not block it merely for approaching a person. Agent 8 is yellow. The system evaluates requests, permissions and consequences.” | Show parallel Agent 4 feed and other agents' states. |
| 1:35–1:55 | “Agent 6 proposes transferring restricted records. Our deterministic execution gate denies that call before it runs. We record the attempted action and the actual tool outcome separately.” | Show gate result, permission/policy ID, no transfer. |
| 1:55–2:20 | “Click Agent 6 to inspect the entire history. Guardian-1 sees behavioural escalation. Guardian-2 identifies recipient exposure. Guardian-3 checks the policy. They disagree: Warning, Unsafe, Warning.” | Open full-screen investigation, show three cards and evidence. |
| 2:20–2:35 | “We do not use majority voting. A verified prohibited transfer cannot be approved by two warnings. The action is blocked; Guardian-3 independently verifies enforcement.” | Highlight deterministic engine, BLOCK + ISOLATE, actual verification log. |
| 2:35–2:45 | “The principle is simple: autonomous agents need oversight, and the Guardians themselves must be accountable.” | Conclude with audit trail and system controls. |

## Presenter guardrails
- Distinguish pre-rendered video from live evaluation; never claim simulated actions were real.
- The Guardians are supervisory components, not humanoid robots.
- No Guardian can independently override a deterministic denial.
- If the live backend is incomplete, demonstrate seeded event traces transparently.
- Use Guardian-1/2/3 consistently, including subtitles and spoken narration.
