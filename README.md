# PRD Interviewer

An [agent skill](https://agentskills.io/home) that builds a detailed Product Requirements Document through a focused, one-question-at-a-time interview.

## What it does

Instead of dumping a template to fill out, this skill interviews you iteratively — one question at a time, each building on your previous answers. It:

- Asks focused questions that dig into the most important gaps
- Covers problem, users, scope, requirements, success criteria, and edge cases
- Adapts depth to the complexity of your idea
- Generates a structured PRD.md when enough detail is gathered

## Installation

### As a skill

```bash
npx skills add https://github.com/diegopetrucci/prd-interviewer --skill prd-interviewer
```

### As a Claude Code plugin

```shell
/plugin marketplace add diegopetrucci/ai-agents-skills
/plugin install prd-interviewer@diegopetrucci-claude-plugins
```

## Usage

Trigger the skill when you have a product idea to flesh out:

- **Claude Code:** `/prd-interviewer` or say "help me write a PRD" or "I have an idea I want to spec out"

Then answer the questions one at a time. The skill will generate a PRD.md when it has enough detail.

## More Skills Like This

Found this skill useful? Browse all my hand-crafted ones in the [AI Agents skills](https://github.com/diegopetrucci/ai-agents-skills) repo.

## License

MIT
