# Contributing

Default guide for `cronai-labs` repositories. A repository with its own `CONTRIBUTING.md`
overrides this one.

## The flow

1. **An issue first.** Describe the problem and the evidence for it, not just the desired
   change. Large efforts become a tracking issue with sub-issues.
2. **Branch from the issue** so it is linked and named `<issue-number>-<short-kebab-summary>`.
   Docs-only changes without an issue use `docs/<short-kebab-summary>`.
3. **Pull request to `main`**, referencing `Closes #<n>`. Never commit to `main` directly.
4. **Squash merge.** One PR becomes one commit: one changelog entry, one revert unit.

Sequential work should be a [stack](https://docs.github.com/en/pull-requests) rather than one
large PR — `gh extension install github/gh-stack`, then `gh stack init` / `add` / `submit`.

## Commit and PR titles

Conventional Commits, enforced on the **PR title** because that becomes the squash subject:

```text
<type>(<optional scope>): <subject>
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`,
`revert`. Add `BREAKING CHANGE:` in the body when it applies.

Branch commits are not linted — write them for whoever reads the PR.

## Before you open a PR

Run the repository's own checks and put the real results in the template. If a check cannot run
in your environment — no container runtime, no API key — say so explicitly rather than leaving
the row blank.

## Reviews

Required approvals are currently **0**: there is one maintainer, and a repository cannot deadlock
waiting for someone to approve their own work. CI, linear history and revertability are the real
controls. That changes when a second maintainer joins.

## Security

Do not open a public issue for a vulnerability — see [SECURITY.md](SECURITY.md).
