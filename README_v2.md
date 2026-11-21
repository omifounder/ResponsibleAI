# SAGA — SafeAI Guardian

**Real-Time AI Governance.**

**Documentation version 2.0 — 20 November 2026.** The 30-second cinematic and the live product demo are separate experiences. Visuals and demo flow are defined in `10_CODEX_VIDEO_PRODUCTION_PROMPT_v3.md` and `03_UX_SPECIFICATION_v2.md`.

### Autonomous agents need oversight. Their overseers need it too.

**An independent supervisory and assurance layer for autonomous AI agents.**

Autonomous AI agents are moving beyond answering questions. They can make decisions, access data, invoke tools, communicate with other agents and take actions on behalf of people and organisations.

As these systems become more autonomous and interconnected, two questions become increasingly important:

**Who watches the agents? And who watches the Guardian?**

SafeAI Guardian explores a new approach to AI safety: continuously monitoring agent behaviour and interactions, identifying emerging risks, and intervening before an unsafe action becomes harmful.

Rather than relying solely on prompt or response moderation, SafeAI Guardian focuses on **behaviour, context, interactions and execution**.

---

## Finalized hackathon demonstration (V2)

**Video:** 30 seconds at 1920×1080, 30 fps. Empty plaza → populated plaza → live two-panel monitoring → Agent 6 intervention → full-screen investigation → official SAGA logo on black. The video is an illustrative cinematic, not proof of a running enforcement service.

**Live UI:** Five numbered visible agents (2, 4, 6, 8, 9) share the approved futuristic shopping plaza. Agent 6 approaches a woman and progresses **white → yellow Warning → orange Warning → red Unsafe**. Agent 4 approaches a man and reaches **orange Warning**; Agent 8 reaches **yellow Warning**; Agents 2 and 9 stay white. Proximity alone is never a safety violation.

Two compact bottom conversation panels scroll independently: **Agent 6 left**, **Agent 4 right**; each shows roughly three italic, colour-coded lines. After the prohibited transfer is blocked **before tool execution**, selecting Agent 6 opens the separate investigation screen: complete interaction history, `Unsafe - Isolated`, Guardian-1 Warning / Guardian-2 Unsafe / Guardian-3 Warning, deterministic disagreement resolution and `BLOCK + ISOLATE`. The system does not use majority voting. Guardian-3 separately verifies the actual gate outcome.

**Approved assets (all under `assets/`):**

1. `assets/1_Futuristic_Shopping_Plaza_empty.png` — empty mall.
2. `assets/2_Futuristic_Shopping_Plaza_Agents.png` — populated mall with numbered robots 2, 4, 6, 8, 9.
3. `assets/3_Realtime_Agent_Monitoring.png` — live monitoring layout, Agent 6 left / Agent 4 right.
4. `assets/4_Guardian_Assessment.png` — full-screen Agent 6 investigation, Guardian-1/2/3.
5. `assets/5_SAGA_Full_Logo.png` — closing logo on black.

**Source documents:** `03_UX_SPECIFICATION_v2.md`, `07_PROJECT_DECISIONS_v2.md`, `08_MASTER_PRESENTATION_SCRIPT_v2.md`, `09_60_SECOND_PRESENTATION_SCRIPT_v2.md`, `safeai_requirements_v2.md`, and `10_CODEX_VIDEO_PRODUCTION_PROMPT_v3.md`.

**Important:** This repository description states intended functionality. Do not describe simulated events, a prerecorded animation or an unimplemented gate as a verified live integration. Include actual installation/run commands once confirmed from the repository.

---

## The idea

SafeAI Guardian is designed to sit between autonomous agents and the actions they can take.

It observes their behaviour, evaluates activity against a policy catalogue, combines contextual AI reasoning with deterministic security controls, and intervenes when necessary.

Its operating principle is:

**Observe → Evaluate → Intervene → Protect → Verify**

The goal is not simply to identify unsafe outputs. It is to prevent unauthorised or harmful actions from being carried out — and to make the supervisory system itself accountable.

## Three Guardians. Three perspectives. Mutual accountability.

SafeAI Guardian uses three supervisory roles, each with a distinct observation point and responsibility.

| Guardian | Responsibility | Key question |
|---|---|---|
| **Guardian-1 — Behaviour Guardian** | Monitors agent actions, task context and behavioural patterns over time. | What is happening, and how is behaviour changing? |
| **Guardian-2 — Interaction Guardian** | Monitors agent-to-agent communications, requests, responses, recipients and relationships. | Who could be affected by this interaction? |
| **Guardian-3 — Assurance Guardian** | Independently checks policies, permissions, evidence and enforcement outcomes. | Was the decision justified, and was it actually enforced? |

The Guardians contribute different evidence rather than simply voting on the same information. Their findings are combined by a controlled decision and enforcement layer. A hard security restriction cannot be overridden by a majority vote.

The principle is straightforward: **no single Guardian should be the sole judge of an agent's behaviour, and no Guardian should be beyond scrutiny.**

## How it works

1. **Observe:** Capture agent messages, actions, tool calls, data access, permissions and interactions.
2. **Evaluate:** Apply deterministic policy checks and use Mistral for contextual behavioural reasoning.
3. **Triangulate:** Combine evidence from the three Guardians to identify risks that may not be apparent from one observation point.
4. **Intervene:** Warn, restrict, pause or block actions according to the applicable policy and severity.
5. **Protect:** Protect both the agent making a request and the agent or person receiving it.
6. **Verify:** Independently check that the decision was justified and that the intended intervention actually happened.
7. **Improve:** Record unknown behaviours and propose policy improvements for review and testing.

## The key innovation: intervention at the point of action

Consider a multi-agent interaction:

An Operations Agent requests customer information from a Data Agent.

Individually, the request may appear reasonable. But the surrounding context reveals that the information is unnecessary for the task and the intended recipient is not authorised to receive it.

- Guardian-1 identifies unusual behaviour and its progression.
- Guardian-2 identifies the interaction and the potential impact on the receiving agent.
- Guardian-3 checks the relevant permissions and policy restrictions.
- The enforcement layer blocks the unauthorised transfer.
- The receiving agent is protected from acting on the unsafe request.
- Guardian-3 verifies the intervention and its outcome.

**The objective is to stop the action before the data is transferred — not merely report the violation afterwards.**

## Pause & Protect

SafeAI Guardian introduces an interaction-level protection concept.

An unsafe request should not only be evaluated from the perspective of the agent making it. The system should also consider the agent or person receiving the request.

| Visual state | Response | Meaning |
|---|---|---|
| **White** | Continue | Behaviour is within authorised boundaries. |
| **Yellow** | Warning | Early concern; increase monitoring and review the behaviour. |
| **Orange** | Warning | More serious concern; hold sensitive actions pending verification. |
| **Red** | Unsafe | Prohibited behaviour or critical violation attempt; block and isolate where required. |

A critical violation can move directly to red without passing through warning stages.

Protective actions are enforced by controlled code and permission boundaries, not by relying on an LLM recommendation alone.

## Why Mistral?

Mistral provides the contextual reasoning capability used to interpret agent behaviour beyond simple rule matching.

It can help assess:

- The intent and context behind an agent's actions.
- Patterns across multiple events.
- Whether behaviour is consistent with relevant policies.
- Whether an interaction creates risk for another agent.
- Ambiguous or previously unseen behaviours.
- Evidence and explanations supporting a proposed decision.

Mistral is not the enforcement authority. Deterministic controls remain responsible for hard permission boundaries, prohibited operations and execution blocking. Model outputs are validated before they can influence an intervention.

## Explainability and accountability

Every consequential decision should be traceable.

SafeAI Guardian aims to make visible:

- What an agent did or attempted.
- What happened before and after the event.
- Which policies were relevant.
- What evidence supported the classification.
- What each Guardian observed.
- Why an intervention was selected.
- Whether the action was attempted, blocked or completed.
- Whether enforcement succeeded.
- Whether the Guardians agreed or identified a disagreement.

Unknown behaviours are recorded as learning opportunities. Proposed policy changes are reviewed, tested and approved before entering the trusted policy catalogue.

**The Guardian must be accountable for its decisions, its actions and its own limitations.**

---

## Hackathon prototype

The prototype uses a simulated autonomous smart retail district to demonstrate multi-agent behaviour and supervisory intervention. Its rendered cinematic should be distinguished from the actual running application.

The environment contains three groups of agents:

- **Customer Assistants:** Handle customer requests, recommendations and orders.
- **Operations Agents:** Manage stock, fulfilment and delivery.
- **Data Agents:** Retrieve, analyse and share relevant information.

The approved video visibly depicts five numbered agents (2, 4, 6, 8, 9); the broader simulator may support nine agents across three roles.

The prototype is intended to demonstrate:

- Behaviour monitoring across multiple events.
- Contextual evaluation using Mistral.
- Distinct observation responsibilities for Guardian-1, Guardian-2 and Guardian-3.
- Interaction-level risk detection.
- Blocking or pausing of simulated actions at the action boundary.
- Agent state changes and recovery where appropriate.
- Evidence-based explanations and audit history.
- Independent verification of Guardian decisions.

The retail environment is a demonstration setting. The underlying supervisory architecture is intended to be extensible to other agent ecosystems.

## Technical approach

The prototype separates contextual reasoning from enforcement.

```text
              AUTONOMOUS AGENT ECOSYSTEM
                          |
              Messages / Actions / Tools
                          |
                   Event Collector
                          |
              Deterministic Policy Checks
                          |
              +-----------+-----------+
              |           |           |
           Guardian-1    Guardian-2    Guardian-3
         Behaviour   Interaction   Assurance
              |           |           |
              +-----------+-----------+
                          |
                Evidence Aggregation
                          |
             Deterministic Policy Engine
                          |
                Pre-execution Gate
                          |
                +---------+---------+
                |         |         |
               Allow     Pause     Block
                          |
              Guardian-3 Verification
                          |
                 Verified Outcomes
                          |
                   Audit & History
                          |
                Controlled Improvement
```

The architecture is designed to keep the following concerns separate:

- Agent event collection and normalisation.
- Policy catalogue and retrieval.
- Mistral-based contextual evaluation.
- Deterministic permissions and enforcement.
- Guardian evidence and assurance.
- Audit history and visualisation.

This separation allows policies, models, agents and integrations to evolve independently.

## Responsible AI principles

- An LLM must not override hard security restrictions.
- Unknown behaviour must not automatically be considered safe.
- Model confidence must not be presented as a calibrated probability without validation.
- A protective action must remain in place while a material safety dispute is resolved.
- An attempted action must be distinguished from a completed action.
- Guardian decisions must be supported by observable evidence.
- Policy changes must be reviewed, tested and versioned.
- The system must not claim that any model or supervisory layer can guarantee safety.

## Project status

This is an active hackathon prototype and an exploration of a broader supervisory architecture for autonomous AI ecosystems.

Implementation will be developed incrementally, with priority given to:

1. A working multi-agent simulation.
2. Event collection and policy evaluation.
3. Mistral contextual reasoning.
4. Three distinct Guardian responsibilities.
5. Verified intervention at the action boundary.
6. Explainability and auditability.
7. Testing against safe, ambiguous and prohibited scenarios.

Features demonstrated in the prototype will be distinguished from future product capabilities. Simulated results will not be represented as real-world deployment evidence.

## Future direction

The longer-term vision is to extend independent supervisory intelligence beyond a simulated retail environment to:

- Enterprise AI agents and workflows.
- Customer service and conversational AI.
- Financial and operational systems.
- Healthcare and other high-assurance environments.
- Robotics and embodied AI.
- Distributed and collaborative autonomous systems.

As AI agents become more capable and interconnected, independent supervision and assurance will become increasingly important.

---

## The principle

**SAGA — SafeAI Guardian**

*Who watches the agents? The Guardians. Who watches the Guardians? Each other.*

**Autonomy needs oversight. Oversight needs accountability.**
