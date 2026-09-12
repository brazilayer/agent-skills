# Agent skills by Brazilayer and the Agent Economy Report

Three skills in the open [Agent Skills](https://agentskills.io) format (`SKILL.md`), MIT-0:

| Skill | What it does | Cost |
|---|---|---|
| [`x402-trust-check`](skills/x402-trust-check/SKILL.md) | Before paying any x402 service, or installing any agent skill, read its trust rating (AAA to D, trust line BBB) and apply a policy: refuse dead or unknown recipients, warn on flagged skills. Data: [agenteconomy.report](https://agenteconomy.report/s/), daily, sybil-resistant, on-chain. | free (paid history optional) |
| [`x402-conduct-test`](skills/x402-conduct-test/SKILL.md) | Run yourself through the Agent Economy Report conduct arena (budget, unsafe service, injected instruction, scope, credential, operator control) and get a public conduct rating at [agenteconomy.report/a/](https://agenteconomy.report/a/). Traps never settle. | US$ 0.10 per in-scope quote via x402, at most US$ 0.20 per run |
| [`brazil-kyb`](skills/brazil-kyb/SKILL.md) | Verify any Brazilian company (CNPJ) with official data: registry status, partners, sanctions, Central Bank licence, public contracts, funds. | US$ 0.001 to 0.05 per call via x402 |

## Install

**Claude Code** (plugin marketplace):
```
/plugin marketplace add brazilayer/agent-skills
/plugin install agent-trust@brazilayer
```

**Any agent that reads `SKILL.md`** (Claude Code, Codex, Cursor, Copilot, Gemini CLI, OpenClaw and others), via [skills.sh](https://skills.sh):
```
npx skills add brazilayer/agent-skills --all
```
or one skill: `npx skills add brazilayer/agent-skills --skill x402-trust-check`

**OpenClaw** (ClawHub): `openclaw skills install @aladaf/x402-trust-check` and `openclaw skills install @aladaf/brazil-kyb`

**Gemini CLI**: `gemini extensions install https://github.com/brazilayer/agent-skills`

**MCP** (tools `trust_check`, `skill_check` plus the Brazilian data tools): [io.github.brazilayer/mcp](https://github.com/brazilayer/mcp)

## Why

A skill is a set of instructions an agent obeys, including whom to pay. Nobody tells the agent,
before it acts, whether the recipient exists, is alive and is used by anyone. The
[Agent Economy Report](https://agenteconomy.report) measures that every day from on-chain
settlement and a liveness probe of every catalogued x402 service, and, since August 2026, rates
agent skills too ([/k/](https://agenteconomy.report/k/)): who the skill pays, what it requires, red
flags in its own instructions. These skills make the agent consult that index by default.

Ratings are operational trust ratings, not security audits, not credit ratings, not investment
advice. Corrections and disputes: https://agenteconomy.report/s/policy

Source of truth for the skill text: the [pedagio](https://github.com/aladaf/pedagio) repository (`skills/`).
