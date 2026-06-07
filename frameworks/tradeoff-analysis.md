# Tradeoff Analysis Framework

## 1. Purpose

The purpose of this framework is to help me compare multiple possible solutions instead of rushing into the first answer that works.

In engineering, most meaningful decisions do not have one perfect solution.

They involve tradeoffs between cost, reliability, complexity, speed, security, scalability, and long-term maintenance.

This framework trains the habit of choosing intentionally instead of reacting quickly.

---

## 2. When To Use

Use this framework when:

* Choosing between multiple technical solutions.
* Designing infrastructure.
* Selecting cloud services.
* Building automation.
* Making Terraform, CI/CD, Docker, Kubernetes, or AWS decisions.
* Deciding whether to optimize cost, speed, reliability, or simplicity.
* Explaining a technical recommendation to a manager, teammate, or hiring manager.

If more than one reasonable solution exists, use this framework.

---

## 3. Core Principle

There are no free decisions.

Every solution improves something and makes something else worse.

The goal is not to find the perfect option.

The goal is to choose the best tradeoff for the situation.

---

## 4. Thinking Model

Options
→ Evaluation Criteria
→ Cost
→ Reliability
→ Complexity
→ Ownership
→ Risk
→ Decision
→ Accepted Tradeoffs

A good engineering decision clearly explains not only what was chosen, but what was intentionally not chosen.

---

## 5. Step-by-Step Framework

### Step 1 — Define The Decision

Clearly state the decision being made.

Ask:

* What am I deciding?
* Why does this decision matter?
* Who is affected by this decision?
* Is this decision reversible?

Output:

A one-sentence decision statement.

Example:

"Choose the best approach for reducing CI/CD pipeline runtime without increasing deployment risk."

---

### Step 2 — Generate Multiple Options

Do not evaluate only one solution.

Ask:

* What is the simplest option?
* What is the cheapest option?
* What is the fastest option?
* What is the most reliable option?
* What is the easiest option to maintain?
* What option would a senior engineer likely consider?

Output:

At least three possible options.

---

### Step 3 — Define Evaluation Criteria

Before choosing, define what matters most.

Possible criteria:

* Cost
* Reliability
* Security
* Complexity
* Speed of implementation
* Maintainability
* Scalability
* Team knowledge
* Operational burden
* Business urgency

Ask:

* Which criteria matter most for this situation?
* Which criteria matter least?
* What constraint cannot be violated?

Output:

A ranked list of decision criteria.

---

### Step 4 — Evaluate Cost

Cost includes more than cloud spend.

Ask:

* What is the infrastructure cost?
* What is the engineering time cost?
* What is the maintenance cost?
* What is the opportunity cost?
* What hidden costs exist?
* What will this cost at 10x scale?

Output:

A cost analysis for each option.

---

### Step 5 — Evaluate Reliability

Ask:

* Which option is most failure-resistant?
* Which option has the smallest blast radius?
* Which option is easiest to rollback?
* Which option is easiest to monitor?
* Which option creates the least incident risk?

Output:

A reliability comparison.

---

### Step 6 — Evaluate Complexity

Ask:

* Which option is easiest to understand?
* Which option creates the least cognitive load?
* Which option requires the least specialized knowledge?
* Which option introduces the fewest moving parts?
* Am I overengineering?

Output:

A complexity comparison.

---

### Step 7 — Evaluate Ownership

Ask:

* Who owns this?
* Who maintains this?
* Who gets paged?
* Who will document it?
* Could a new engineer understand this?
* What happens if the expert leaves?

Output:

An ownership and maintainability comparison.

---

### Step 8 — Evaluate Risk

Ask:

* What could go wrong?
* Which option has the largest blast radius?
* Which option is hardest to reverse?
* Which option creates security risk?
* Which option creates financial risk?
* Which option creates long-term technical debt?

Output:

A risk comparison.

---

### Step 9 — Choose And Document The Decision

Make the decision based on the criteria that matter most.

Document:

* Chosen option.
* Why it was chosen.
* Options rejected.
* Why they were rejected.
* Tradeoffs accepted.
* Risks remaining.

Output:

A clear decision record.

---

## 6. Critical Questions

* What decision am I actually making?
* What options exist?
* What criteria matter most?
* Which option is simplest?
* Which option is cheapest?
* Which option is safest?
* Which option is easiest to operate?
* What tradeoff am I accepting?
* What am I intentionally not optimizing for?
* Is this reversible?
* Would I still choose this if I had to maintain it myself?

---

## 7. Common Mistakes

* Comparing only one option.
* Choosing the most technically interesting solution.
* Ignoring business urgency.
* Ignoring long-term maintenance.
* Treating cost as an afterthought.
* Optimizing for scale before scale exists.
* Assuming complexity equals maturity.
* Failing to document rejected options.
* Forgetting who owns the system after implementation.

---

## 8. Senior Engineer Perspective

A senior engineer does not simply ask, “Which option works?”

A senior engineer asks:

* Which option fits the business context?
* Which option is easiest to operate?
* Which option has acceptable risk?
* Which option can the team maintain?
* Which option preserves future flexibility?
* Which option avoids unnecessary complexity?

The maturity of a decision is shown by how clearly the tradeoffs are understood.

---

## 9. Output

By the end of this framework, I should have:

* Decision statement.
* At least three options.
* Evaluation criteria.
* Cost comparison.
* Reliability comparison.
* Complexity comparison.
* Ownership comparison.
* Risk comparison.
* Final decision.
* Accepted tradeoffs.

This output can later become:

* A decision record.
* A case study section.
* An interview answer.
* A portfolio artifact.
* A future Claude-guided decision review.

---

## 10. Framework Evolution

After using this framework, ask:

* Did I compare the right options?
* Did I miss an important criterion?
* Did I underestimate cost?
* Did I underestimate complexity?
* Did I ignore ownership?
* What question would have improved the decision?
* Should that question become permanent?
* What would a Staff engineer have noticed earlier?
* What lesson should compound into future decisions?

The framework improves when real decisions expose better questions.

---

## Final Principle

The purpose of this framework is not to produce better answers.

The purpose of this framework is to produce better engineers through better questions.