# Multi-Agent Book Factory Architecture

**Target Audience:** Product Architect

Diagram source (draw.io): `docs/book-factory-architecture.drawio`

## Key design highlights
- Deterministic control plane owned by Program Manager
- Non-deterministic generation in Author stage (LLM drafting)
- Hybrid visual stage (Mermaid → PlantUML → draw.io)
- Deterministic QA gates before publishing
- Explicit human-in-the-loop approval and escalation

## Loop strategy
- **Loop A:** Draft ↔ Review ↔ Revise (max **3** iterations/chapter)
- **Loop B:** Visuals ↔ QA (max **2** iterations/chapter)

## Human-in-the-loop
- Stage-gate feedback at PM + QA checkpoints
- Approve / reject / request revision
- Escalation for risk, quality, or policy failures
