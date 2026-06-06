# Worked Example: Ops Hardening + Anti-Pattern Scanner

This example shows how to combine the Ops Hardening Framework with the Anti-Pattern Scanner on an operational process.

## Query
"Review a state agency’s grant distribution process for potential operational failures, anti-patterns, and hardening opportunities."

## Step 1: Apply Anti-Pattern Scanner
Identified anti-patterns in the current process:
- Announce-Instead-Of-Paste (public announcements of “transparent” processes that lack clear documentation)
- Scope Creep (grant criteria changing mid-cycle without clear communication)
- Silent decision-making (internal review processes with no visible audit trail)

## Step 2: Apply Ops Hardening Framework
Using gate-first and process resilience principles:

**Key Weak Points:**
- Lack of early gates for application completeness and eligibility
- Poor feedback loops to applicants
- Limited auditability of scoring and selection decisions
- No structured mechanism to detect repeated low-quality or potentially coordinated applications

**Hardening Recommendations:**
- Implement clear, published gates at each stage of the grant process
- Create auditable scoring rubrics and decision logs
- Add early detection for anomalous application patterns
- Build continuous improvement mechanisms based on applicant feedback and outcome tracking

## Final Synthesized Output
The current grant process contains several operational anti-patterns and structural weaknesses that reduce both efficiency and public trust. Applying hardening principles (early gates, auditability, and feedback loops) would significantly improve resilience and accountability.

Key Takeaway:
The Anti-Pattern Scanner quickly surfaced common failure modes. The Ops Hardening Framework then provided concrete structural fixes to make the process more robust and transparent.