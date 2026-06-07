# Problem Solving Framework

## 1. Purpose

The purpose of this framework is to help me approach engineering problems with clarity before jumping into solutions.

This framework exists because many technical mistakes happen before implementation begins. The wrong problem gets solved, assumptions go unchallenged, business context gets ignored, and engineers start building before they fully understand what matters.

This framework trains the habit of slowing down, defining the real problem, understanding constraints, evaluating options, and documenting the reasoning behind the final decision.

The goal is not to find an answer quickly.

The goal is to make a better engineering decision.

---

## 2. When To Use

Use this framework when:

* Starting a new technical task.
* Reviewing a Jira ticket.
* Designing infrastructure.
* Writing Terraform.
* Building CI/CD pipelines.
* Debugging unclear system behavior.
* Optimizing cloud costs.
* Making architecture decisions.
* Planning automation.
* Explaining a solution to another engineer or stakeholder.

If the decision affects cost, reliability, maintainability, security, or another engineer’s future work, this framework should be used.

---

## 3. Core Principle

Define the problem before designing the solution.

A well-built solution to the wrong problem is still a failure.

The quality of the solution depends on the quality of the problem definition.

---

## 4. Thinking Model

Problem
→ Context
→ Assumptions
→ Constraints
→ Options
→ Tradeoffs
→ Decision
→ Validation
→ Reflection

This framework is not a checklist to rush through.

It is a thinking process that forces better questions before action.

---

## 5. Step-by-Step Framework

### Step 1 — Define The Problem

Before solving anything, write the problem in plain language.

Ask:

* What is happening?
* What should be happening instead?
* Who is affected?
* How do I know this problem exists?
* Is this the root problem or only a symptom?

Output:

A clear one-sentence problem statement.

Example:

"Terraform deployments are taking too long, causing slower release cycles and delayed infrastructure changes."

---

### Step 2 — Understand The Business Context

Technical work exists inside a business context.

Ask:

* Why does this matter?
* What business value is created by solving this?
* What risk is reduced?
* What cost is reduced?
* What happens if we do nothing?
* Who benefits from this work?

Output:

A short explanation of why the problem matters beyond the technical layer.

---

### Step 3 — Identify Assumptions

Most bad decisions come from hidden assumptions.

Ask:

* What am I assuming is true?
* What evidence supports this?
* What evidence is missing?
* What would prove this assumption wrong?
* Am I relying on experience, data, or guessing?

Output:

A list of assumptions that need to be validated.

---

### Step 4 — Identify Constraints

Every solution operates inside limits.

Ask:

* What is the timeline?
* What is the budget?
* What systems already exist?
* What cannot change?
* What reliability requirements exist?
* What security requirements exist?
* What skill level does the team have?
* Who will maintain this after implementation?

Output:

A list of constraints that shape the decision.

---

### Step 5 — Break Down The System

Large problems become easier when broken into components.

Ask:

* What systems are involved?
* What dependencies exist?
* What inputs and outputs exist?
* Where could failure happen?
* What systems communicate with each other?
* What external services are involved?

Output:

A simple system map or written breakdown of the components involved.

---

### Step 6 — Generate Multiple Options

Do not stop at the first solution.

Ask:

* What is the simplest solution?
* What is the fastest solution?
* What is the cheapest solution?
* What is the most reliable solution?
* What is the easiest solution to maintain?
* What would I do if I had half the budget?
* What would I do if I had half the time?

Output:

At least three possible solution options.

---

### Step 7 — Evaluate Tradeoffs

Every solution sacrifices something.

Compare each option across:

* Cost
* Reliability
* Complexity
* Security
* Maintainability
* Scalability
* Operational burden
* Team ownership

Ask:

* What does this option improve?
* What does this option make worse?
* What risk does this introduce?
* What future work does this create?
* Would I still choose this if I personally had to maintain it?

Output:

A clear explanation of the tradeoffs between options.

---

### Step 8 — Make The Decision

After analysis, choose a direction.

Document:

* What option was chosen.
* Why it was chosen.
* What alternatives were rejected.
* What tradeoffs were accepted.
* What risks remain.

Output:

A decision statement that future engineers can understand.

---

### Step 9 — Define Validation

A solution is not complete until it is validated.

Ask:

* How will I know this worked?
* What metric should improve?
* What metric should not get worse?
* What logs, alerts, or dashboards confirm success?
* How will I detect if this caused a new issue?

Output:

A validation plan.

---

### Step 10 — Reflect

After the work is complete, review the decision.

Ask:

* Did this solve the original problem?
* Were my assumptions correct?
* What surprised me?
* What did I misunderstand?
* What would I do differently?
* What should I remember next time?

Output:

A short lesson learned.

---

## 6. Critical Questions

* What problem am I actually solving?
* Is this the real problem or a symptom?
* Why does this matter to the business?
* What assumptions am I making?
* What constraints exist?
* What options have I considered?
* What are the tradeoffs?
* What could fail?
* What will this cost now?
* What will this cost at 10x scale?
* Who owns this after implementation?
* How will I know this worked?
* What should future me remember?

---

## 7. Common Mistakes

* Jumping to a solution before defining the problem.
* Solving symptoms instead of root causes.
* Ignoring business context.
* Choosing the first solution that seems reasonable.
* Forgetting cost impact.
* Forgetting operational ownership.
* Overengineering.
* Failing to document why a decision was made.
* Not validating the outcome.
* Not capturing lessons learned.

---

## 8. Senior Engineer Perspective

A senior engineer does not simply ask, “Can this be built?”

A senior engineer asks:

* Should this be built?
* Why does it matter?
* What tradeoffs are acceptable?
* Who owns it later?
* What happens when it fails?
* What does it cost?
* How does this affect the business?
* Can another engineer understand and maintain it?

The goal is not only technical correctness.

The goal is responsible engineering judgment.

---

## 9. Output

By the end of this framework, I should have:

* A clear problem statement.
* Business context.
* Assumptions.
* Constraints.
* Multiple solution options.
* Tradeoff analysis.
* Final decision.
* Validation plan.
* Lesson learned.

This output can later become:

* A problem-session note.
* A case study.
* An after-action review.
* A portfolio artifact.
* A future Claude-guided engineering session.

---

## 10. Framework Evolution

After using this framework, ask:

* What assumption was wrong?
* What question would have prevented a mistake?
* Should that question become permanent?
* Should this framework be updated?
* What would a Staff engineer have noticed earlier?
* What lesson should compound into future decisions?

The framework should improve through real use.

Every project, mistake, debugging session, and decision should make the Engineering Operating System stronger.
