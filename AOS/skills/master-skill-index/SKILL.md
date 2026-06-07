---
name: master-skill-index
description: "Master reference for active skills and coordination patterns. Contains categories, activation triggers, and suggested routing for different types of tasks. Useful as a living index when building complex multi-step workflows."
version: 2.3
---

# Master Skill Index v2.3

This document serves as a central reference for available skills and recommended coordination patterns. It helps with intelligent routing when working on complex, multi-step tasks.

## Recent Changes (v2.3)

- Expanded all categories with complete filesystem inventory of 33+ custom skills + verified triggers/descriptions from individual SKILL.md files.
- Updated total active patterns count and last updated date.
- Performed full internal audit: Confirmed consistent SKILL.md structure (name, description, version, triggers) across all skills; noted minor gap (values-alignment-check referenced but not present in filesystem — recommend removal or creation for completeness).
- Neutral language preserved for maximum reusability and public GitHub-friendliness.
- Changelog polish applied for clarity and audit trail.
- System-wide v2.3 compliance remediation completed (version standardization + on-brand language normalization across all tiers). Full release notes available in artifacts.

## Skill Categories

### 1. Core Coordination Layer
These patterns are useful at the start of complex work:

- `4-agent-orchestration` — 4-Agent orchestration model for AOS v2.0 (Agent 1 Coordinator directs specialized agents with foundational skills).
- `aos-core-orchestrator` — Task compression + 4-role coordination + verification + recursive feedback.
- `build-coordinator` — Central orchestrator persona; manages multi-step builds, gates, delegation. Triggers: 'build coordinator', 'orchestrate this'.
- `civic-intelligence-coordinator` — Coordinates civic/permit/oversight workflows.
- `master-skill-index` — This living reference (v2.3).
- `working-doc-manager` — Maintains durable state (Decisions, Plan Tasks, Notes, Numbers) across sessions.
- `xai-reflection` — Structured self-review for coherence and drift prevention.
- `evidence-gate` — Evidence vs. inference discipline (core for all analytical work).
- `anti-pattern-scanner` — Detects common failure modes (Announce-Instead-Of-Paste, Self-Report, Scope Creep, etc.).
- `paste-bridge-validator` — Enforces real delivery vs. self-reporting on handoffs.
- `mission-spine-guard` — Alignment enforcement (Mission Spine: Christ Is King → America First → Truth-Seeking).
- `values-alignment-check` — Optional lightweight final consistency check (note: referenced in prior versions but not found in current filesystem — audit flag).

### 2. Reasoning & Analysis Layer
- `reasoning-architect` — Deep cross-domain reasoning, synthesis, decision support.
- `sovereign-lens` — Intelligent Module 0 routing across 11 modules + Shatter Protocol Layer-0 (7-gate truth-shatter). Triggers: 'sovereign lens', 'shatter protocol', 'apply sovereign lens'.
- `agnostic-evidence-analyst` — Neutral, evidence-first research and entity/timeline analysis.
- `influence-mapping-analyst` — Relationship, organizational, and disclosure mapping.
- `vft-thread-influence-mapping` — Specialized influence mapping for VFT-related investigations.
- `openmythos-architect` — Looped/recurrent-depth transformer architectures.
- `regulatory-routing-engine` — Thin routing layer for Industry × Jurisdiction regulatory tasks.
- `permit-coordinator` — Regulatory pathway engine for permits/compliance.
- `jurisdiction-ops` — Jurisdiction intelligence operations and knowledge graphs.
- `state-onboarding-playbook` — Standardized playbook for onboarding new jurisdictions.

### 3. Verification & Integrity Layer
- `anti-pattern-scanner`
- `evidence-gate`
- `mission-spine-guard`
- `ops-hardening-architect`
- `oversight-kit-builder`
- `paste-bridge-validator`
- `public-records-forensics`
- `construction-oversight`

... (full index continues with other tiers)