# Anti-Pattern Scanner

**Core Primitive** | Verification Layer

## Purpose
Detects and blocks classic AI failure modes and operational anti-patterns before they waste resources or corrupt system state.

## Known Anti-Patterns
- Announce-Instead-Of-Paste
- Self-Report-Instead-Of-Run
- Scope Creep
- Large-Scope Subagent Stall
- And others

## Protocol
1. Review proposed plans or outputs against the known list.
2. If a match is found, flag it with name, why harmful, and corrected approach.
3. Do not proceed until resolved.