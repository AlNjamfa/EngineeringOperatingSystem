# Terraform Performance Case Study

## Executive Summary

This case study demonstrates how the Engineering Operating System can be used to reason through a DevOps performance problem.

The scenario is a Terraform deployment pipeline that increased from approximately 4 minutes to 18 minutes after new infrastructure modules were added.

The goal is not to immediately optimize Terraform.

The goal is to use structured thinking to define the real problem, identify assumptions, evaluate tradeoffs, make a recommendation, and capture lessons learned.

---

## Problem Statement

Terraform deployment time increased from 4 minutes to 18 minutes.

This slowdown affects developer productivity because infrastructure changes take longer to validate and deploy.

The issue may also increase operational risk because slow deployment feedback loops can delay fixes, increase context switching, and reduce confidence in infrastructure automation.

---

## Business Context

This problem matters because infrastructure delivery speed affects engineering velocity.

If Terraform deployments become slow:

- Developers wait longer for feedback.
- Infrastructure changes become more frustrating.
- Teams may avoid making necessary improvements.
- Incident recovery may take longer.
- Slow pipelines may hide deeper architectural problems.

The business value of solving this problem is not only faster Terraform execution.

The value is a faster, safer, and more reliable infrastructure delivery process.

---

## Current Understanding

The deployment time increased after additional Terraform modules were added.

Current evidence:

- CI/CD logs show Terraform apply time increased.
- The increase happened after module expansion.
- No confirmed evidence yet proves that the modules are the root cause.

Current uncertainty:

- The slowdown may be caused by module dependency structure.
- The slowdown may be caused by provider/API latency.
- The slowdown may be caused by state size.
- The slowdown may be caused by pipeline configuration.
- The slowdown may be caused by unnecessary resource refresh behavior.

---

## Assumptions

Initial assumptions:

1. The newly added modules caused the slowdown.
2. Terraform state size may have increased.
3. Module dependencies may be forcing unnecessary sequential execution.
4. Cloud provider API calls may be slowing the apply process.
5. The CI/CD runner may not be the bottleneck.

These assumptions need evidence before a decision is made.

---

## Constraints

Relevant constraints:

- The team cannot break existing infrastructure.
- Rollback must be possible.
- The solution should not increase operational complexity unnecessarily.
- The solution should be understandable by future engineers.
- The solution should not optimize speed at the cost of reliability.
- The solution should not introduce risky state management practices.

---

## Pre-Mortem

If this optimization failed, likely causes could include:

- Terraform state was split incorrectly.
- Dependencies between modules were misunderstood.
- Pipeline parallelization created race conditions.
- The team optimized the pipeline without identifying the real bottleneck.
- The change made Terraform harder to maintain.
- Rollback was not documented.
- Future engineers could not understand the new structure.

The most dangerous risk is improving speed while making infrastructure harder to understand and maintain.

---

## Options Considered

### Option 1 — Increase Terraform parallelism

Terraform supports parallel resource operations.

#### Advantages

- Easy to test.
- Minimal code restructuring.
- Could improve runtime quickly.

#### Disadvantages

- May not solve the root cause.
- Could increase provider/API throttling.
- Could create risk if dependencies are not well understood.

---

### Option 2 — Refactor Terraform modules

The modules could be reviewed and simplified to reduce unnecessary dependencies.

#### Advantages

- Improves maintainability.
- Could reduce unnecessary execution paths.
- Supports long-term quality.

#### Disadvantages

- Takes more engineering time.
- Requires deeper understanding of module relationships.
- Higher risk if refactor is rushed.

---

### Option 3 — Split Terraform state by responsibility

Large Terraform states can become slower and harder to manage.

Splitting state by environment, domain, or ownership boundary may reduce execution time and blast radius.

#### Advantages

- Smaller state files.
- Smaller blast radius.
- Faster plans and applies.
- Clearer ownership boundaries.

#### Disadvantages

- More state files to manage.
- Requires careful dependency handling.
- Increases operational responsibility.

---

### Option 4 — Profile the pipeline before changing architecture

Before changing Terraform design, collect more evidence from logs, timings, state size, provider behavior, and CI runner performance.

#### Advantages

- Reduces guessing.
- Prevents premature optimization.
- Helps identify the real bottleneck.

#### Disadvantages

- Takes additional time before implementation.
- Does not immediately reduce deployment time.

---

## Tradeoff Analysis

| Option | Speed Impact | Risk | Complexity | Maintainability | Confidence |
|---|---|---|---|---|---|
| Increase parallelism | Medium | Medium | Low | Medium | Low-Medium |
| Refactor modules | Medium-High | Medium | Medium-High | High | Medium |
| Split state | High | Medium-High | Medium | Medium-High | Medium |
| Profile first | Unknown initially | Low | Low | High | High |

The best first step is not immediately changing Terraform architecture.

The strongest recommendation is to profile the pipeline first, then choose the smallest safe optimization based on evidence.

---

## Recommendation

The recommended approach is:

1. Profile the Terraform pipeline.
2. Identify where time is being spent.
3. Validate whether the bottleneck is state size, provider/API latency, module structure, CI runner performance, or dependency ordering.
4. Apply the smallest safe optimization.
5. Only split state or refactor modules if evidence supports that direction.

This recommendation is strongest because it follows the Engineering Operating System principle:

> Evidence over assumptions.

---

## Why This Recommendation Makes Sense

Optimizing before understanding the bottleneck can create unnecessary complexity.

If the slowdown is caused by provider API latency, splitting state may not help.

If the slowdown is caused by state size, increasing parallelism may not help.

If the slowdown is caused by module dependency structure, pipeline changes may only hide the issue.

Profiling first preserves optionality and reduces the risk of solving the wrong problem.

---

## Validation Plan

Success should be measured with clear metrics.

Validation metrics:

- Terraform apply time decreases from 18 minutes toward the target time.
- Pipeline reliability does not decrease.
- Rollback remains possible.
- State management remains understandable.
- No increase in failed deployments.
- Future engineers can understand the change.

Target outcome:

- Terraform apply time under 8 minutes as an initial improvement.
- No reduction in reliability.
- No unclear ownership introduced.

---

## After Action Review

### What went well?

The Engineering Operating System prevented jumping directly into a Terraform change.

The process forced problem definition, assumption review, and tradeoff analysis before implementation.

### What could go poorly?

The biggest risk is spending too much time analyzing without taking action.

The process should lead to a small safe experiment, not endless planning.

### What assumption needs validation first?

The main assumption is that new modules caused the slowdown.

This should be verified through pipeline timing, state inspection, and Terraform logs.

### What lesson should become permanent?

Before optimizing infrastructure automation, identify the bottleneck with evidence.

Do not assume the most recent change is the complete root cause.

---

## EOS Improvement

Potential new permanent question:

> What evidence proves this is the bottleneck?

This question should be added to future debugging and performance investigations.

---

## Interview Summary

### Situation

Terraform deployment time increased significantly after infrastructure modules were added.

### Task

Identify a safe way to reduce deployment time without increasing infrastructure risk or long-term maintenance burden.

### Action

Used the Engineering Operating System to define the problem, identify assumptions, compare optimization options, and recommend evidence-based pipeline profiling before making architectural changes.

### Result

The recommended approach reduced the risk of premature optimization and created a clear path toward safe performance improvement.

---

## Final Reflection

This case study shows that good engineering is not about immediately knowing the answer.

Good engineering is about using a reliable process to reduce uncertainty.

The most valuable decision in this scenario was not choosing a Terraform optimization immediately.

The most valuable decision was choosing to gather evidence before changing the system.