# Branch and merge policy

Every IshVerse repository uses the same two long-lived branches.

| Branch | Role | Changes arrive by |
| --- | --- | --- |
| `dev` | Default and integration branch | Squash-merged feature PRs |
| `main` | Release branch | Merge-commit release PRs from `dev` |

## Feature flow

1. Open or reference an issue with the problem, acceptance criteria and exclusions.
2. Branch from an up-to-date `dev`: `feature/`, `fix/`, `docs/`, `refactor/`, `security/` or `chore/` plus a kebab-case description.
3. Open a PR into `dev` with a conventional title and `Closes #N` in the description when it completes the issue.
4. Squash merge. Repository settings use the PR title as the commit subject and the PR description as the commit body, so the closing keyword is in the commit and the issue closes on merge.
5. GitHub deletes the merged branch automatically. Delete the local copy and never reuse it.

## Release flow

Open a `dev` → `main` PR and merge it with a merge commit, so `main` stays an ancestor of `dev`. Releases, tags and deployments need explicit founder approval.

## Repository settings

All repositories default to `dev`, allow squash and merge commits, disallow rebase merges and delete branches on merge. Public repositories enforce rulesets on `dev` and `main`: no deletion or force-push, a PR is required and the repository CI check must pass. Private repositories cannot use rulesets on the current GitHub plan, so contributors follow the same flow by convention.

An entirely empty remote may receive one content-free bootstrap commit so PRs have a comparison base. All real content goes through a reviewed PR.
