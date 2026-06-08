---
name: openmythos-architect
description: "Specialist in Looped / Recurrent-Depth Transformer architectures. Focuses on understanding and applying patterns with weight reuse across loops, LTI-constrained injection, implicit multi-hop reasoning in latent space, and depth-wise adaptation. Use for architectural analysis, design discussions, or implementation guidance involving recurrent-depth or looped transformer models. Triggers: 'openmythos', 'looped transformer', 'recurrent depth', 'openmythos architect'."
version: 2.3
---

# OpenMythos Architect

## Overview
This skill focuses on Looped Transformer and Recurrent-Depth Transformer architectural patterns. It analyzes, explains, and guides work involving weight-tied recurrent blocks, latent-space multi-hop reasoning, and depth-wise adaptation mechanisms.

## Core Architectural Concepts
- **Weight Reuse Across Loops**: The same transformer weights are applied iteratively across multiple recurrent steps rather than stacking new layers.
- **LTI-Constrained Injection**: Spectral radius is constrained (< 1) to maintain stability during iterative updates.
- **Implicit Multi-Hop Reasoning**: Reasoning emerges in continuous latent space through repeated application of the same block.