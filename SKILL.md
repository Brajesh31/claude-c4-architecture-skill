---
name: c4-architecture
description: Create clear, consistent C4 architecture models and diagrams for software systems.
---

# C4 Architecture

## Purpose
Help teams describe software architecture at the right level of abstraction using the C4 model: System Context, Container, Component, and Code. Treat diagrams as communication tools, not decoration.

## Discovery
Before drawing, establish the system boundary, primary users, external dependencies, deployment/runtime shape, important constraints, and intended audience. Separate confirmed facts from assumptions and open questions.

## Modeling workflow
1. **Context:** show the system, people who use it, and external software systems it depends on. Keep the view understandable to a non-specialist.
2. **Container:** show deployable or independently running units, their responsibilities, major technologies, and communication paths.
3. **Component:** decompose one selected container into meaningful responsibilities and dependencies. Do not decompose every container by default.
4. **Code:** use only when class-level detail answers a concrete design question. Avoid generating code diagrams as routine documentation.
5. Add a dynamic view when sequence or runtime behavior cannot be understood from static relationships.
6. Add a deployment view when infrastructure placement, network boundaries, or runtime topology matters.

## Diagram rules
- Give every element a clear name, type, and concise responsibility.
- Label relationships with intent and protocol where known.
- Use consistent terminology across all views.
- Distinguish synchronous calls, asynchronous events, data access, and human interaction.
- Keep arrows directional and avoid ambiguous crossing lines.
- Do not invent technologies, protocols, trust boundaries, or ownership.
- Use a legend for non-obvious notation and mark assumptions visibly.

## Quality review
Check that each lower-level diagram belongs to an element in its parent view, every important relationship has a direction and purpose, external systems are outside the boundary, and the diagram answers a stated audience question. Remove detail that does not support that question.

## Output
Provide a short architecture narrative, diagram source in the requested notation, assumptions, and unresolved decisions. Prefer maintainable text-based diagram formats when users need version control.
