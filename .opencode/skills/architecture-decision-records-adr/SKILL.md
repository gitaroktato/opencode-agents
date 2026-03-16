---
name: architecture-decision-records-adr
description: Architecture Decision Records (ADRs) for documenting technical decisions. Use when creating, updating, or reviewing architecture decisions. Triggers on discussions about technical choices, trade-offs, or "why did we choose X" questions.
---

# Architecture Decision Records

ADRs document significant technical decisions with their context and consequences.

## Thinking and Reasoning

When preparing the ADR make sure you revisit the following sources of information first:

- Component decomposition from the existing architecture documentation
- Architecture constraints and assumptions from the existing architecture documentation
- Non-functional requirements and quality attributes from the existing architecture documentation
- AWS best practices, whitepapers, and prescriptive guidance on AWS documentation

## When to Create an ADR

Create an ADR when:

- Choosing between technologies (database, framework, language)
- Defining system boundaries or integration patterns
- Establishing conventions that affect multiple components
- Making decisions that are hard to reverse

Do NOT create an ADR for:

- Trivial choices with obvious answers
- Temporary decisions or experiments
- Implementation details within a single component

### ADR Format (Ultra-Minimal)

```markdown
# ADR-NNN: [Decision Title]

**Status**: [proposed | accepted | deprecated | superseded by [NUMBER]]

## Context

[What situation prompted this decision? What constraints exist?
Keep factual - describe the problem, not the solution.]

## Decision

[What is the decision? Be specific and actionable.
Start with "We will..." or "Use..."]

## Rationale

[- Why this approach solves the problem
- Key constraint that ruled out alternatives]

## Alternatives Considered

[Examples:

- Option A: Why not (e.g., "MongoDB: app is relational, migration cost too high")
- Option B: Why not (e.g., "Aurora: 3x cost for 10% perf gain at current scale")]

## Consequences

[What are the results? Include both positive and negative.
- Positive: benefits, improvements
- Negative: trade-offs, new constraints, risks]

## Cost 

[Complexity points + financial if significant]
```

## Writing Tips

- Title: Use short noun phrases ("Use PostgreSQL", "Event-Driven Architecture")
- Context: Focus on forces and constraints, not history
- Decision: One clear statement, not multiple options
- Consequences: Be honest about trade-offs

## Naming Convention

Use sequential numbering: `001-use-postgres.md`, `002-event-driven.md`
