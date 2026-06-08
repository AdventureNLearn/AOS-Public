---
# Adventure OS (AOS) v2.x — Skill Ecosystem

**Public, replicable coordination patterns and frameworks for high-agency AI work.**

AOS v2.x is an Agnostic Edition skill system designed for **consistency, neutrality, and maximum reusability** across different environments and use cases.

## What is This?

This repository contains the complete AOS skill ecosystem — modular, versioned coordination patterns that can be used independently or together.

Each skill lives in its own folder and follows a standardized `SKILL.md` format with:
- Clear frontmatter (`name`, `description`, `version`)
- Activation triggers
- Structured guidance (Overview, Core Principles, Activation, etc.)
- Evidence-first and gate-oriented design where applicable

## Current Version: v2.3

This release focuses on **system-wide compliance**:

- All major skills standardized to `version: 2.3`
- Significant normalization of language toward neutral, pattern-focused descriptions
- Improved structural consistency across tiers
- Full internal audit completed

See the [v2.3 Compliance Release Notes](artifacts/AOS_Skill_Ecosystem_v2.3_Compliance_Release_Notes.md) for details.

## Repository Structure

```
AOS/
├── skills/                          # All individual skills (tiered)
│   ├── master-skill-index/          # The living central reference
│   ├── core-coordination/
│   ├── verification-integrity/      # ✅ Complete
│   ├── reasoning-analysis/          # ✅ Complete
│   ├── domain-execution/            # ✅ Complete
│   └── operational-playbooks/
├── artifacts/                       # Release notes, standards, archives
├── docs/                            # Additional documentation
└── README.md
```

## Key Documents

- **[Master Skill Index v2.3](AOS/skills/master-skill-index/SKILL.md)** — The central living reference for routing and capabilities
- **[Skill Compliance Standards v2.3](artifacts/Skill_Compliance_Standards_v2.3.md)** — Official standards + full audit log
- **[v2.3 Release Notes](artifacts/AOS_Skill_Ecosystem_v2.3_Compliance_Release_Notes.md)** — Clean summary of this release
- **[Archive Summary](artifacts/AOS_v2.3_Skill_Compliance_Archive_Summary.md)** — Complete record of the v2.3 compliance work

## How to Use These Skills

1. Browse the `skills/` directory or start with the **Master Skill Index**.
2. Each `SKILL.md` contains activation triggers and usage guidance.
3. Skills are designed to be composed — many reference foundational skills (`evidence-gate`, `anti-pattern-scanner`, `working-doc-manager`, etc.).
4. Use the index for intelligent routing on complex tasks.

## Philosophy

- **Agnostic & Replicable**: Minimal location/platform-specific assumptions.
- **Evidence-First**: Strong emphasis on gates, verification, and auditability.
- **Neutral Language**: Designed for broad reusability.
- **Mission Spine Aware**: High-stakes skills respect the core alignment (Christ Is King → America First → Truth-Seeking) without forcing it into every output.

## Status

The skill ecosystem is in a stable, well-documented state following the v2.3 compliance remediation.

**Completed Tiers (with full content)**:
- Verification & Integrity Layer ✅
- Reasoning & Analysis Layer ✅
- Domain & Execution Layer ✅

Ready for use, extension, and public/replicable deployment.

---

**Maintained as part of the Adventure OS project.**  
Public, open, and built for real work.