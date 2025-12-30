[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![GitHub Stars](https://img.shields.io/github/stars/tobs-code/mechatronic-prompting?style=social)]

# Mechatronic Prompting

## Founding Document

**Established:** December 29, 2025

**Origin:** Mechatronics & Automation Engineering → AI Safety & Control Systems

**Author:** tobi (Germany)

**License:** Apache 2.0

---

## Definition

**Mechatronic Prompting** is a prompt engineering paradigm that applies safety-critical systems engineering principles from industrial automation to the design, validation, and operation of Large Language Model instructions.

Instead of treating prompts as conversational heuristics refined through intuition and trial-and-error, Mechatronic Prompting treats them as **engineered control systems** with explicit constraints, failure models, and verification loops.

A prompt, in this paradigm, is not prose.
It is a **control artifact**.

---

## Core Assumptions

* LLMs are deterministic optimizers under uncertainty, not reasoning agents
* Most prompt failures are **structural**, not linguistic
* Safety, reliability, and robustness must be designed *before* deployment
* Implicit intent is an anti-pattern in safety-relevant systems

---

## Core Principles

### 1. Failure Mode Analysis First (FMEA)

Prompt design starts with identifying how the system can fail:
hallucination, overconfidence, goal drift, constraint erosion, sycophancy.
Countermeasures are embedded directly into the prompt structure.

### 2. Adversarial Validation by Default

Every non-trivial prompt must include internal mechanisms to challenge itself:
false constraints, conflicting goals, or injected inconsistencies that must be detected and handled explicitly.

### 3. Explicit Constraint Enforcement

No hidden assumptions. No “understood context”.
Constraints, priorities, and prohibitions are expressed in structured, inspectable form.

This includes the use of **SoftPrompt-IR**
→ https://github.com/tobs-code/SoftPrompt-IR

### 4. State Machine Architecture

Prompts are modeled as state machines:
defined phases, transitions, validation gates, and terminal conditions.
Free-form execution is treated as an uncontrolled failure mode.

### 5. Reliability Scaling via SIL Thinking

The rigor of a prompt scales with the consequence of failure.
High-impact domains require stricter validation, redundancy, and conservative output behavior.

### 6. Mandatory Self-Audit Loops

Complex prompts must include explicit self-verification stages that:

* detect internal inconsistencies
* flag uncertainty
* prevent unjustified confidence inflation

### 7. Embedded Compliance Patterns

For regulated or safety-relevant domains (medical, legal, financial),
documentation, traceability, and compliance artifacts are part of the output schema, not an afterthought.

---

## Traditional Prompting vs. Mechatronic Prompting

| Aspect            | Traditional Prompting | Mechatronic Prompting |
| ----------------- | --------------------- | --------------------- |
| Reliability Model | Implicit / hope-based | Engineered            |
| Failure Handling  | Reactive              | Pre-analyzed (FMEA)   |
| Constraints       | Implicit prose        | Explicit, structured  |
| Testing           | Trial & error         | Adversarial injection |
| Structure         | Free-form             | State-machine driven  |
| Validation        | Manual review         | Built-in self-audit   |
| Documentation     | Optional              | Mandatory             |

---

## Foundational Components

The following systems and frameworks are concrete instantiations of the paradigm and are published separately:

* **SoftPrompt-IR** – symbolic intent and constraint representation → https://github.com/tobs-code/SoftPrompt-IR
* **ASEV** – Adversarial State Export Validation → /REFERENCE_PROMPTS/Adversarial_State_Export_Validation-Reference.md
* **AWDF** – Agent Workflow Diagnosis Framework
* **HMCF** – Hyper-Modal Cognitive Framework

Each component can be used independently but follows the same underlying design philosophy.

---

## What This Is NOT

* Not a jailbreak or prompt exploitation technique
* Not a collection of “clever wording tricks”
* Not beginner-friendly prompt advice
* Not a guarantee of correctness or truth
* Not optimized for persuasive or confident-sounding output
* Not aligned with “make the model sound smart”

Mechatronic Prompting prioritizes **controlled failure** over fluent nonsense.

---

## Design Philosophy

> In industrial automation, you learn early:
> the machine does not lie.
>
> It executes exactly what you specify —
> not what you intended.
>
> Large Language Models are no different.
> They do not need better wording.
> They need better control loops.
>
> **Mechatronic Prompting is the application of that lesson to AI systems.**

---

## License & Use

This paradigm is open for use, study, critique, and extension.

Attribution is required as per Apache 2.0.
Forks, adversarial testing, and refutations are explicitly welcome.
