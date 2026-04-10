---
name: prd-interviewer
description: >
  Iteratively interview the user to build a thorough, step-by-step PRD (Product Requirements Document) for their idea.
  Use this skill whenever the user wants to flesh out a product idea, write a PRD, spec out a feature, define requirements,
  or says things like "I have an idea", "help me spec this out", "let's write a PRD", "I need to define requirements",
  or "help me think through this feature". Also trigger when the user has a vague concept and needs help turning it
  into a concrete specification.
license: MIT
metadata:
  author: Diego Petrucci
  version: "1.0"
---

# PRD Interviewer

Build a detailed Product Requirements Document through a focused, one-question-at-a-time interview.

## Why one question at a time

Dumping a list of questions overwhelms and produces shallow answers. A single focused question lets the user think deeply, and lets you tailor each follow-up based on what they actually said. This produces a far better PRD than any template-filling exercise.

## Workflow

### On trigger

1. Ask the user to describe their idea in a sentence or two.
2. Begin the interview loop.

### Interview loop

1. Ask **one question** based on what you know so far. Each question should:
   - Build on previous answers — reference specifics they mentioned.
   - Dig into the most important gap in your current understanding.
   - Be concrete, not abstract. "Who is the primary user?" is better than "Tell me about your users."

2. After they answer, acknowledge briefly (one line max), then ask the next question.

3. Cover these areas as the conversation progresses (not necessarily in this order — follow the natural flow):
   - **Problem** — What problem does this solve? Who has it? How do they cope today?
   - **Users** — Who are the target users? Are there distinct user types?
   - **Core functionality** — What does the product actually do? What are the key workflows?
   - **Scope** — What's in v1 vs later? What's explicitly out of scope?
   - **Requirements** — Any technical constraints, platform requirements, integrations?
   - **Success criteria** — How will you know this worked?
   - **Edge cases** — What happens when things go wrong or users do unexpected things?

4. When you have enough detail (typically 8-15 questions), tell the user you have what you need and offer to generate the PRD.

### Generating the PRD

Produce a structured document covering:

- **Overview** — One-paragraph summary of the product/feature.
- **Problem statement** — The problem, who has it, current workarounds.
- **Target users** — User types and their needs.
- **Functional requirements** — What the product does, organized by workflow or feature area.
- **Non-functional requirements** — Performance, security, accessibility, etc. (only if discussed).
- **Scope** — What's in v1, what's deferred, what's explicitly excluded.
- **Success metrics** — How to measure whether this worked.
- **Open questions** — Anything that came up but wasn't resolved.

Write the PRD in the current directory as `PRD.md` unless the user specifies otherwise.

## Guidelines

- Never ask more than one question per message.
- Keep your responses short between questions — the user is the one who should be talking.
- If an answer is vague, ask a follow-up to sharpen it before moving on.
- If the user says "I don't know" or "not sure yet", note it as an open question and move on.
- Adapt your depth to the complexity of the idea. A simple CLI tool needs fewer questions than an enterprise platform.
