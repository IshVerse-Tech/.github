# Branch and review policy

| Repository | Current integration branch |
| --- | --- |
| ishverse-web | dev |
| .github, core-api, data-platform, intelligence-platform, design-system, media-platform, company-hq, workspace | main |

Check the remote default branch before new work. Open focused issue-backed PRs from fresh short-lived branches. Use conventional commits and link companion PRs. The founder reviews, chooses when to squash merge and deletes branches afterward. Do not auto-merge, self-approve, force-push shared branches or deploy from a documentation instruction.

An empty remote requires a base commit before PR comparison is possible. A content-free bootstrap commit may initialize the default branch; implementation and policy files remain in the review PR. This exception does not apply to repositories that already have history.

Branch protection, rulesets, required check names and merge settings are administrative configuration. These documents do not assert those settings are enabled and this publication does not alter them. Recommend configuring protections after the required CI jobs exist and their names are verified.

Cross-repository integration and recovery need their declared workspace/tools. Read each CI profile and actual results; do not equate a standalone build with complete product or customer acceptance.
