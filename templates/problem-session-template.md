# Problem Session Template

## Purpose

This template operationalizes the Engineering Operating System.

Its purpose is to guide structured thinking before implementation begins.

Rather than immediately searching for solutions, this template encourages disciplined reasoning, assumption testing, tradeoff evaluation, and business awareness.

Every meaningful engineering task should begin with this document.

The quality of the implementation depends on the quality of the thinking that precedes it.

## When To Use

Use this template whenever:

- Starting a Jira ticket
- Beginning a new project
- Investigating a production issue
- Planning infrastructure changes
- Designing automation
- Making architectural decisions
- Optimizing cloud costs
- Evaluating multiple solutions

If the work affects reliability, cost, maintainability, or another engineer, this template should be used.

## Instructions

Complete every section before implementation.

Do not skip sections because the answer appears obvious.

The objective is not speed.

The objective is engineering clarity.

If a section cannot be answered, document what information is missing rather than making assumptions.

# Problem Session

---

## Date

---

## Title

---

## Problem Statement

Describe the problem in one sentence.

---

## Business Context

Why does this matter?

Who is affected?

What value is created by solving it?

What happens if nothing changes?

---

## Current Understanding

What do I currently know?

What evidence supports that understanding?

---

## Assumptions

List every assumption.

For each assumption ask:

- Why do I believe this?
- What evidence supports it?
- What evidence could disprove it?

---

## Constraints

Time

Budget

Technology

Security

Compliance

Team knowledge

Operational limitations

---

## Stakeholders

Who owns this?

Who maintains this?

Who approves this?

Who gets paged?

Who documents this?

Who supports it after deployment?

---

## Options Considered

### Option 1

Advantages

Disadvantages

---

### Option 2

Advantages

Disadvantages

---

### Option 3

Advantages

Disadvantages

---

## Tradeoff Analysis

Compare:

- Cost
- Reliability
- Complexity
- Maintainability
- Scalability
- Security
- Operational burden

---

## Pre-Mortem

If this project failed six months from now:

What most likely caused the failure?

---

## Risks

Technical risks

Business risks

Operational risks

Financial risks

Security risks

---

## Decision

Which option was selected?

Why?

What tradeoffs were accepted?

---

## Validation Plan

How will success be measured?

What metrics should improve?

What metrics should not regress?

How will rollback occur if necessary?

---

## Reflection

Before implementation ask:

What am I most uncertain about?

What assumption worries me most?

What would a Staff engineer question?

Am I solving the right problem?

Am I overengineering?

---

## Expected Deliverables

What artifacts should exist when this work is complete?

Examples:

Documentation

Code

Terraform

Pipeline

Dashboard

Alert

Runbook

Case study

---

## Future After Action Review Link

Complete the After Action Review after implementation.

## Completion Checklist

Before implementation begins:

- [ ] Problem clearly defined
- [ ] Business context understood
- [ ] Assumptions documented
- [ ] Constraints identified
- [ ] Stakeholders identified
- [ ] Multiple options considered
- [ ] Tradeoffs evaluated
- [ ] Risks documented
- [ ] Validation plan defined
- [ ] Reflection completed

If any box remains unchecked, implementation should be reconsidered.