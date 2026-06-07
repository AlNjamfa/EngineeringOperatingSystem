# Problem Solving Framework

## Purpose

The purpose of this framework is to create a repeatable process for approaching engineering problems with clarity, discipline, and sound judgment.

The objective is not simply to find an answer.

The objective is to understand the problem deeply enough that the solution becomes obvious.

This framework should be used before making important technical decisions, designing systems, debugging failures, implementing automation, or proposing architectural changes.

---

# Core Principle

**Slow down before speeding up.**

Many engineering mistakes happen because solutions are proposed before the problem is fully understood.

The first answer is often an assumption.

The goal is to replace assumptions with evidence.

---

# Stage 1: Define The Problem

## Ask:

- What problem am I actually trying to solve?
- How do I know this problem exists?
- Who is experiencing this problem?
- Is this the root problem or merely a symptom?
- What evidence supports my understanding?

## Remember:

A perfectly engineered solution to the wrong problem is still a failure.

---

# Stage 2: Understand The Context

Technical problems exist inside business systems.

Before proposing solutions, understand the environment.

## Business Questions

- Why does this matter?
- What value is created by solving this?
- What happens if nothing changes?
- What is the opportunity cost?

## Human Questions

- Who owns this?
- Who maintains this?
- Who gets paged?
- Who depends on this system?
- Who will inherit this after deployment?

## Operational Questions

- Is this production?
- Is there an SLA?
- Is downtime acceptable?
- What systems depend on this?

---

# Stage 3: Define Success

A problem cannot be solved if success is undefined.

## Ask:

- What does success look like?
- How will I know I succeeded?
- What metrics improve?
- What metrics should not get worse?
- How will success be measured six months from now?

---

# Stage 4: Identify Constraints

Every engineering decision operates within limitations.

## Technical Constraints

- Existing architecture
- Compatibility requirements
- Performance requirements

## Business Constraints

- Budget
- Timeline
- Team size

## Operational Constraints

- Maintenance burden
- On-call responsibilities
- Skill level of the team

## Ask:

- What cannot change?
- What flexibility do I actually have?

---

# Stage 5: Challenge Assumptions

Assumptions create hidden risk.

List every assumption explicitly.

## Ask:

- What am I assuming?
- What evidence supports this?
- What if this assumption is wrong?
- How can I verify it?

## Example

Instead of saying:

"The database is slow."

Say:

"I believe database latency is causing the issue because query times have increased by 40%."

Now the assumption can be tested.

---

# Stage 6: Break Down The System

Large problems become manageable when divided into smaller pieces.

## Identify:

- Inputs
- Outputs
- Dependencies
- Failure points
- External systems

## Ask:

- What are the major components?
- How do they communicate?
- Where could the problem originate?
- What assumptions exist between components?

---

# Stage 7: Generate Multiple Solutions

Never stop at the first reasonable answer.

Force yourself to generate at least three possible approaches.

## Ask:

- What is the simplest solution?
- What is the cheapest solution?
- What is the most scalable solution?
- What would I do if I had half the budget?
- What would I do if I had half the time?

---

# Stage 8: Evaluate Tradeoffs

Every solution sacrifices something.

The objective is not perfection.

The objective is choosing the best compromise.

## Evaluate:

### Cost

- Infrastructure cost
- Engineering cost
- Maintenance cost

### Complexity

- Operational complexity
- Learning curve
- Future modifications

### Reliability

- Failure tolerance
- Recovery time
- Monitoring requirements

### Scalability

- User growth
- Traffic growth
- Team growth

### Ownership

- Who maintains this?
- Can a new engineer understand it?
- What happens if the primary expert leaves?

---

# Stage 9: Conduct A Pre-Mortem

Assume the project has failed.

Ask why.

## Questions

- What breaks first?
- What assumptions proved false?
- What security risks exist?
- What operational risks exist?
- What costs could unexpectedly increase?
- What documentation is missing?
- What happens at 10x scale?
- What happens during a production incident?

The purpose is not to create fear.

The purpose is to expose blind spots before they become outages.

---

# Stage 10: Make The Decision

Eventually analysis must end.

A decision should be made based on the best available evidence.

## Record:

- Problem Statement
- Chosen Solution
- Why it was chosen
- Alternatives considered
- Tradeoffs accepted

Future engineers should understand why this decision was made.

---

# Stage 11: Validate

After implementation, verify reality.

## Ask:

- Did this solve the original problem?
- Were my assumptions correct?
- Did any unexpected problems appear?
- What metrics changed?
- Would I make the same decision again?

---

# Stage 12: Capture The Lesson

Every project should improve future decision making.

## Reflection Questions

- What surprised me?
- What mistake did I almost make?
- What would I teach another engineer?
- What question should I add to my framework?
- How has my understanding changed?

Knowledge fades.

Lessons written down compound.

---

# Daily Engineering Checklist

Before making an important technical decision, ask:

## Problem

- [ ] What problem am I solving?
- [ ] Is this the real problem?

## Business

- [ ] Why does this matter?
- [ ] What happens if we do nothing?

## Assumptions

- [ ] What am I assuming?
- [ ] How can I verify it?

## Constraints

- [ ] What limitations exist?

## Solutions

- [ ] Have I considered multiple approaches?

## Tradeoffs

- [ ] What am I gaining?
- [ ] What am I sacrificing?

## Cost

- [ ] What does this cost today?
- [ ] What does this cost at 10x scale?

## Ownership

- [ ] Who maintains this?
- [ ] Who gets paged?
- [ ] What happens if the expert leaves?

## Failure

- [ ] What could break?
- [ ] How would I know?

## Reflection

- [ ] What lesson should I remember?

---

# Final Thought

Engineering is not the pursuit of perfect solutions.

It is the disciplined practice of making the best possible decisions with incomplete information.

The quality of those decisions is determined by the quality of the questions asked before the work begins.