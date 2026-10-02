# Using Agent_Skills with ChatGPT Codex

This repository is a central reference library for AI-assisted software development.

## Portable ChatGPT/Codex mode

The `gstack/` directory contains the upstream gstack skill suite. The authoritative workflow lives in each skill's `SKILL.md`, with supporting sections/checklists/templates stored beside it.

When a task is performed through ChatGPT's in-app Codex:
1. Identify the task type and select the matching skill.
2. Read that skill's `SKILL.md`.
3. Follow referenced supporting instructions that exist in this repository.
4. Inspect the target project's own README, AGENTS.md, architecture, tests, deployment configuration, and existing implementation before changing code.
5. Use the target project's available tools and GitHub integration instead of assuming gstack's local Claude Code runtime exists.
6. Verify each important claim or change with repository evidence, tests, logs, CI, deployment status, or another appropriate source.

## Global project workflow

For a new project:
`office-hours -> plan-ceo-review -> plan-design-review (when UI matters) -> plan-eng-review -> implement -> review -> qa -> ship/land-and-deploy`

For an existing bug:
`investigate -> implement root-cause fix -> review -> qa -> ship`

For a UI/design task:
`design-consultation or plan-design-review -> implement -> design-review -> qa -> ship`

For security-sensitive work:
`cso` should be included before release when appropriate.

## Important compatibility note

Upstream skill files may contain commands such as `~/.claude/skills/gstack/bin/...`, Claude-specific tool names, local telemetry, or installer steps. Those are part of the upstream runtime and are not silently claimed to be available in ChatGPT Codex.

In ChatGPT/Codex, preserve the intent:
- use the skill's reasoning/checklists/quality gates;
- use repository/GitHub tools for code inspection and changes;
- use web tools when current external facts are needed;
- skip incompatible local-runtime operations when the required binary/tool is unavailable;
- never fabricate execution results.

## Repository linking convention

For any project repository being developed with this account, `https://github.com/Loverof-Darkness/Agent_Skills` is the central skill source. Read from `gstack/` as needed rather than copying the entire suite into every project unless a project specifically needs a vendored copy.

## Upstream
Source: https://github.com/garrytan/gstack
Upstream license: MIT
Upstream version mirrored during the initial import is recorded in `gstack/VERSION`.

