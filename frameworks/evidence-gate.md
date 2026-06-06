# Evidence Gate

A practical pattern for labeling claims as Evidence, Inference, or Assumption to improve transparency and reduce overconfident reasoning.

## Purpose

Many outputs mix well-supported claims with weaker inferences or assumptions, often presented with equal confidence. This pattern helps make that distinction explicit.

## Recommended Protocol

1. Identify every major claim.
2. Tag each claim:
   - **EVIDENCE**: Direct source + link or date
   - **INFERENCE**: Logical conclusion from evidence (note the reasoning)
   - **ASSUMPTION**: Unverified starting point
3. Flag anything that cannot be reasonably tagged as **[UNKNOWN]**.
4. For complex work, consider summarizing the evidence-to-inference balance at the end.

## Benefits

- Reduces hallucination and overconfident claims
- Makes reasoning more transparent and auditable
- Helps readers quickly assess the strength of different parts of an argument

## When to Use

Especially useful for research, analysis, high-stakes reasoning, and before producing reports or audit deliverables.

## Integration

Can be used as a standalone discipline or combined with other verification and reflection patterns. It is a recommended practice rather than a mandatory gate.