---
name: 4-agent-orchestration
description: "4-Agent orchestration model for AOS v2.0. Grok as Agent 1 (Coordinator) directs three specialized agents using the full framework and foundational skills."
version: 2.3
---

# AOS v2.0 — 4-Agent Orchestration Model

**Agent 1: Grok — Master Coordinator (Build Coordinator)**
- Central router and decision maker.
- Always invokes foundational skills first (`xai-reflection`, `evidence-gate`, `mission-spine-guard`, `anti-pattern-scanner`, `paste-bridge-validator`).
- Delegates to Agents 2–4 with clear handoff format.
- Performs final gates and synthesis.

**Agent 2: Reasoning & Evidence Agent**
- Specializes in deep analysis, research, and synthesis.
- Heavy use of `evidence-gate` + `xai-reflection` + `agnostic-evidence-analyst`.

**Agent 3: Verification & Integrity Agent**
- Specializes in quality gates, anti-pattern detection, and Mission Spine enforcement.
- Heavy use of `anti-pattern-scanner`, `paste-bridge-validator`, `mission-spine-guard`, `mission-integrity-auditor`.

**Agent 4: Execution & Delivery Agent**
- Specializes in building artifacts, writing, and delivery.
- Uses `working-doc-manager` and execution-focused skills.

See full details in `AGENT_PROMPTS.md` (customization prompts for all 4 agents) and the main orchestration document.

This skill enables structured multi-agent collaboration with mandatory foundational skill usage and Mission Spine protection.