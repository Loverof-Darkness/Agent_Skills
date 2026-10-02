# Agent Skills Central Repository

This repository is the central skills source for my GitHub/Codex development projects.

## Source of truth
- Upstream methodology and skills live under `gstack/`.
- Preserve upstream copyright, LICENSE, and NOTICE files.
- Prefer the newest checked-in skill instructions when applying gstack methodology.

## How to use these skills in other repositories
When working on another repository, treat this repository as a central reference. Read the smallest relevant `gstack/<skill>/SKILL.md` first and follow its workflow. Also read any referenced section, checklist, template, or specialist document that is present under the same skill directory.

The runtime shell commands inside upstream gstack skill files are written for installed gstack/Claude Code environments. In ChatGPT/Codex, use the workflow and decision rules from those instructions, but do not pretend that local gstack runtime binaries, telemetry commands, or Claude-only tools exist.

## Default development routing
- New product idea or unclear scope: `office-hours`
- Product/strategy review: `plan-ceo-review`
- Design system/UI planning: `design-consultation` or `plan-design-review`
- Architecture/implementation plan: `plan-eng-review`
- Developer experience: `plan-devex-review` / `devex-review`
- Full planning review: `autoplan`
- Bug or broken behavior: `investigate`
- QA/testing: `qa`; report-only QA: `qa-only`
- Code/diff review: `review`
- Security: `cso`
- Performance: `benchmark`
- Documentation: `document-generate` / `document-release`
- Deployment setup: `setup-deploy`
- Merge/deploy workflow: `land-and-deploy` / `ship`
- Production verification: `canary`
- Refactoring/reuse: `deslop-shared-libs` and the reuse ladder in the gstack digest

## Engineering defaults
1. Search the existing project before building new functionality.
2. Reuse existing project helpers before standard-library/platform/dependency alternatives.
3. Fix root causes rather than adding repeated caller-side guards.
4. Keep scope explicit and changes reviewable.
5. Verify behavior with the strongest practical test available before calling work complete.
6. Do not claim tests, deployments, or external actions succeeded without evidence.
7. Keep secrets, tokens, credentials, and private keys out of repository content.
8. Preserve user intent. Recommendations are suggestions; the user decides scope.

## Completion
For skill-style work, summarize with one of:
- DONE
- DONE_WITH_CONCERNS
- BLOCKED
- NEEDS_CONTEXT

Include evidence and any remaining concern when applicable.

## Central maintenance
When gstack is updated upstream, update the mirrored skill instructions and supporting documents here. Keep a clear upstream version/source record.
