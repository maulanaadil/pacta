<!-- BEGIN:turborepo-agent-rules -->

# This is NOT the Turborepo you know

Turborepo configuration, task behavior, and CLI commands can vary between installed versions and may differ from your training data. Resolve the `turbo` package from this file's directory or relevant workspace; in monorepos, it may not be visible from the repository root. For example, run `node -p "require.resolve('turbo/package.json')"` from a workspace that depends on `turbo`.

Read `docs/README.md` inside that installed package first, then read the relevant pages from its `docs/` directory before changing Turborepo configuration or commands. Heed deprecation notices. These bundled docs match the installed package version and are available without network access.

This block is written and re-added by `turbo` before repository-scoped commands when an AI agent is detected. In the Turborepo source repository, its template is defined in `crates/turborepo-cli/src/cli/agent_guidance.rs`. Removing the managed block while updates are enabled means a later qualifying invocation will add it again. Set `"agentGuidance": true` in the root `turbo.json` or `turbo.jsonc` to opt in; this does not remove an existing block. Keep the block committed with your work to avoid an uncommitted change on the next agent invocation.
<!-- END:turborepo-agent-rules -->

# Branching and pull requests

| Branch | Environment | Purpose |
|---|---|---|
| `dev` | Development (default branch) | All development work goes here. |
| `main` | Production | Release only. Updated by merging `dev` into `main`. |

- Branch off `dev`, never off `main`.
- Open every pull request against `dev`: `gh pr create --base dev --reviewer maulanaadil`.
- Request a review from Maulana Adil (`@maulanaadil`). If you are opening the PR as `maulanaadil`, GitHub won't let you request your own review, so use `--assignee maulanaadil` instead.
- Only release PRs (`dev` → `main`) target `main`.
