# claude-c4-architecture-skill

A Claude Code skill for documenting software architecture with C4 diagrams and clear written context.

## Overview

The C4 model describes software systems at different levels of abstraction. This skill helps inspect a codebase, identify system boundaries, and create diagrams that communicate architecture to different audiences.

It supports context, container, component, deployment, and dynamic views using Mermaid-compatible C4 diagram syntax.

## C4 Diagram Levels

| Level | Diagram | Audience | Shows |
|---|---|---|---|
| 1 | Context | Broad audience | System and external actors |
| 2 | Container | Technical stakeholders | Applications, services, and data stores |
| 3 | Component | Developers | Internal components and dependencies |
| 4 | Deployment | Operations | Runtime infrastructure and deployment nodes |
| Dynamic | Dynamic | Technical teams | Interactions for a specific scenario |

Start with context and container views when documenting a system. Add component or deployment diagrams when they answer a specific question.

## Main Capabilities

- Inspect a codebase to identify system boundaries.
- Identify users and external dependencies.
- Map applications, services, and data stores.
- Document internal components.
- Describe deployment topology.
- Visualize important request or event flows.
- Generate Mermaid C4 diagrams.
- Add explanatory text and assumptions.
- Keep diagrams aligned with implementation changes.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-c4-architecture-skill.git ~/.claude/skills/c4-architecture
```

## Usage

Invoke the skill when documenting or reviewing software architecture:

```text
/c4-architecture
```

Provide the repository, system scope, intended audience, deployment context, and the architecture questions the diagrams should answer.

## Recommended Workflow

1. Define the system boundary and audience.
2. Inspect application entry points and deployment configuration.
3. Identify users and external systems.
4. Map containers and their responsibilities.
5. Identify important components where additional detail is useful.
6. Document deployment nodes and runtime relationships.
7. Create dynamic diagrams for complex interactions.
8. Add explanatory context and assumptions.
9. Validate names and relationships against the codebase.
10. Update diagrams when architecture changes.

## Documentation Structure

A project may organize its architecture documentation as:

```text
docs/
└── architecture/
    ├── overview.md
    ├── context.md
    ├── containers.md
    ├── components.md
    └── deployment.md
```

Use the structure that fits the project. Avoid creating every diagram type if the extra detail does not help readers.

## Quality Checklist

- Diagram level matches the audience.
- System boundary is explicit.
- External dependencies are identified.
- Containers and components have clear responsibilities.
- Relationships are labeled.
- Deployment details reflect the real environment.
- Diagram names match implementation terminology.
- Assumptions and unknowns are stated.
- Diagrams are readable and not overloaded.

## Repository Contents

- `SKILL.md`: Main C4 architecture documentation workflow.
- `README.md`: Diagram levels, workflow, and quality checklist.

## Practical Principle

A C4 diagram is useful when it helps someone understand the system. Do not confuse diagram count with documentation quality.
