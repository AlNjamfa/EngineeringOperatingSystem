# Engineering Operating System

A deliberate practice system for developing engineering judgment through structured questioning, evidence-based reasoning, tradeoff analysis, pre-mortems, debugging discipline, and after-action reviews.

---

## What This Is

The Engineering Operating System is a personal framework I use to improve how I think through technical problems.

It is not a DevOps cheat sheet.

It is not a collection of random notes.

It is not meant to replace official documentation.

It is a system for building better engineering judgment.

The goal is to practice the habits that strong engineers use before, during, and after technical work:

* Define the real problem.
* Understand the business context.
* Identify assumptions.
* Gather evidence.
* Evaluate tradeoffs.
* Consider cost, reliability, and ownership.
* Make intentional decisions.
* Reflect after implementation.
* Capture lessons that improve future work.

---

## Why I Built This

While learning DevOps and FinOps, I realized that learning tools alone is not enough.

Knowing Terraform, Docker, Kubernetes, AWS, CI/CD, or Linux is valuable, but tools change over time.

Good engineering judgment compounds.

This repository exists to help me build the habit of slowing down, asking better questions, reasoning from evidence, staying calm under uncertainty, and making decisions that are technically sound, financially responsible, and maintainable.

---

## Core Idea

Every engineering problem should become an opportunity to improve both the system being built and the engineer building it.

The workflow is simple:

```text
Problem
  ↓
Structured Thinking
  ↓
Evidence
  ↓
Tradeoff Analysis
  ↓
Decision
  ↓
Implementation
  ↓
After Action Review
  ↓
Lesson Learned
  ↓
Better Future Decisions
```

This is continuous improvement for engineering judgment.

---

## How The Repository Is Organized

```text
engineering-operating-system/

README.md
MISSION.md
PHILOSOPHY.md
SCOPE.md
OPERATING_RULES.md
VERSION.md
LICENSE

frameworks/
templates/
case-studies/
claude/
```

---

## Frameworks

The `frameworks/` folder contains the thinking systems used to approach engineering work.

| Framework                | Purpose                                                |
| ------------------------ | ------------------------------------------------------ |
| `problem-solving.md`     | Define the real problem before solving it.             |
| `premortem.md`           | Identify failure modes before implementation.          |
| `tradeoff-analysis.md`   | Compare multiple possible solutions.                   |
| `debugging.md`           | Investigate reality with evidence instead of guessing. |
| `after-action-review.md` | Convert experience into permanent improvement.         |

---

## Templates

The `templates/` folder turns the frameworks into repeatable practice.

| Template                          | Purpose                                                           |
| --------------------------------- | ----------------------------------------------------------------- |
| `problem-session-template.md`     | Use before and during engineering work.                           |
| `after-action-review-template.md` | Use after completing work.                                        |
| `case-study-template.md`          | Use to convert meaningful work into portfolio-ready case studies. |

---

## Case Studies

The `case-studies/` folder shows the Engineering Operating System in action.

Start here:

1. [`Building the Engineering Operating System`](case-studies/building-the-engineering-operating-system.md)
   A meta case study explaining why this system was created and how its architecture was designed.

2. [`Terraform Performance Case Study`](case-studies/terraform-performance-case-study.md)
   A realistic DevOps case study showing how the EOS can be used to reason through a Terraform deployment performance problem.

---

## Claude Integration

The `claude/PROJECT_INSTRUCTIONS.md` file turns Claude into an Engineering Operating System mentor.

Claude's role is not to simply give answers.

Claude's role is to:

* Ask better questions.
* Challenge assumptions.
* Recommend solutions when useful.
* Explain tradeoffs.
* Provide evidence-based reasoning.
* Help create After Action Reviews.
* Suggest improvements to the Engineering Operating System.

The goal is not dependence on AI.

The goal is to use AI mentorship to become more independent over time.

---

## How I Use This

When I encounter a technical problem, I use the EOS like this:

1. Open the `problem-session-template.md`.
2. Define the problem clearly.
3. Identify business context.
4. List assumptions and missing information.
5. Run a pre-mortem.
6. Compare solution options.
7. Make a decision.
8. Validate the result.
9. Complete an After Action Review.
10. Capture one lesson that improves future decisions.

If the work is meaningful, I turn it into a case study.

---

## What This Demonstrates

This repository is designed to show more than technical interest.

It demonstrates:

* Systems thinking
* DevOps mindset
* FinOps awareness
* Debugging discipline
* Business context awareness
* Tradeoff analysis
* Documentation discipline
* Continuous improvement
* Ownership mindset

The purpose is not to look impressive through complexity.

The purpose is to build and demonstrate disciplined engineering judgment.

---

## Operating Principle

I do not want to only learn tools.

I want to learn how to think clearly under uncertainty.

The systems I build may eventually be replaced.

The engineering judgment I develop will compound for the rest of my career.
