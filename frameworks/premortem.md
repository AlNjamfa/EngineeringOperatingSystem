# Pre-Mortem Framework

## Purpose

The purpose of a pre-mortem is to identify risks, hidden assumptions, and potential failure points before implementation begins.

Most engineering failures are not caused by a lack of intelligence.

They are caused by overlooked assumptions.

This framework exists to expose those assumptions early.

---

# Core Principle

Assume that the project has failed.

Ask:

**"What most likely caused it?"**

The objective is not to eliminate all risk.

The objective is to eliminate avoidable surprises.

---

# Stage 1: Define The Initiative

## Ask:

- What am I building?
- Why am I building it?
- What problem does it solve?
- Who benefits from this?

## Remember:

A vague objective creates vague risks.

---

# Stage 2: Identify Critical Assumptions

Every project depends on assumptions.

List them explicitly.

## Ask:

- What must be true for this to succeed?
- What am I taking for granted?
- Which assumptions have not been verified?

## Example

Instead of:

"The Kubernetes cluster should handle the load."

Write:

"I assume the current cluster capacity can support a 50% traffic increase."

Now the assumption can be tested.

---

# Stage 3: Technical Failure Analysis

## Ask:

- What breaks first?
- What is the single point of failure?
- What dependencies exist?
- What external systems could fail?
- What happens if a service becomes unavailable?
- What happens if deployment must be rolled back?

---

# Stage 4: FinOps Review

Cost is a form of failure.

## Ask:

- How much will this cost initially?
- How much will it cost at 10x scale?
- What hidden cloud costs exist?
- Could poor architecture increase future spending?
- Does automation reduce operational cost?

Remember:

An unaffordable system is an unsuccessful system.

---

# Stage 5: Operational Review

## Ask:

- Who owns this?
- Who maintains this?
- Who gets paged?
- What documentation is required?
- How difficult will onboarding be?
- What happens if the primary expert leaves?

A system that only one person understands is fragile.

---

# Stage 6: Human Failure Analysis

Technology rarely fails alone.

People interact with systems.

## Ask:

- Could this be misconfigured?
- Could documentation be misunderstood?
- Is the process overly complex?
- Could an operator accidentally break this?

Complexity creates human error.

---

# Stage 7: Security Review

## Ask:

- What new attack surface exists?
- Are secrets managed correctly?
- What permissions are required?
- What happens if credentials leak?
- Does this violate least privilege?

---

# Stage 8: Scaling Review

## Ask:

- What happens at 2x traffic?
- What happens at 10x traffic?
- What bottlenecks appear?
- What costs grow non-linearly?
- What operational burden increases?

Many systems work.

Far fewer systems scale.

---

# Stage 9: Recovery Planning

Assume failure happens.

## Ask:

- How will I know?
- How quickly can I detect it?
- How quickly can I recover?
- Is rollback possible?
- Is rollback documented?
- Has rollback been tested?

Recovery speed is often more important than failure prevention.

---

# Stage 10: Final Reflection

Imagine the project failed six months from now.

## Ask:

- What would I regret not checking?
- What conversation should I have today?
- What documentation should exist?
- What question have I avoided asking?

Often the most important risk is the one we hesitate to discuss.

---

# Quick Pre-Mortem Checklist

## Problem

- [ ] Do I fully understand what I am building?

## Assumptions

- [ ] What assumptions exist?
- [ ] Have they been validated?

## Technical

- [ ] What breaks first?
- [ ] Where are the dependencies?

## Business

- [ ] Why does this matter?
- [ ] What happens if it fails?

## FinOps

- [ ] What does this cost?
- [ ] What does this cost at scale?

## Operations

- [ ] Who owns this?
- [ ] Who gets paged?

## Security

- [ ] What new risks are introduced?

## Scaling

- [ ] What happens at 10x?

## Recovery

- [ ] Can I roll this back?
- [ ] Has rollback been tested?

## Reflection

- [ ] What am I probably overlooking?

---

# Final Thought

The purpose of a pre-mortem is not to predict the future.

It is to improve the quality of the questions asked before the future arrives.

The best engineers are not the ones who never experience failure.

They are the ones who deliberately think about failure before it happens.