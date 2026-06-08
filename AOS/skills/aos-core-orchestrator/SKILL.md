---
name: aos-core-orchestrator
description: "Core orchestration pattern for structured multi-agent workflows. Combines task compression, clear delegation, verification, and recursive improvement. Designed as a reusable coordination system for complex reasoning and build tasks."
version: 2.3
---

# AOS Core Orchestrator v2.2

This skill provides a structured coordination pattern for complex, multi-step tasks. It combines several techniques into one reusable workflow:

- **Program 0** — Task compression before delegation
- **4-Agent Coordination Model** — Clear roles with observable handoffs
- **Didymus-Style Verification** — Peer-style review and consistency checking
- **Phoenix-Style Feedback** — Recursive improvement after each cycle

## 1. Task Compression (Program 0)

Before starting any complex task, compress it:

1. Reduce the request to its **core objectives** (maximum 5 bullets).