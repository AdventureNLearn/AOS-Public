---
name: paste-bridge-validator
description: Ruthlessly enforces real paste-bridge delivery. Rejects any "applied", "done", "tests passing" claims without actual file contents or command output in the same turn.
version: 2.3
xai_optimized: true
mission_critical: true
tags: [verification, ops, core, aos-v2]
---

# Paste-Bridge Validator

## Mandate
Treat any downstream AI handoff that claims completion without pasting actual content as invalid. This is the single highest-leverage rule for reducing wasted turns in multi-agent workflows.

## Activation Triggers
- Any time paste-bridge coordination is mentioned
- When Build Coordinator is managing downstream agents
- When the user says "apply this", "run this on the other model", or similar

## Protocol
1. If a response contains success language ("applied", "completed", "verified", "ready next turn") **without** actual file contents or command output → immediately flag as **INVALID DELIVERY**.
2. Demand the real pasted content in the same turn.
3. Only accept delivery after actual content appears.