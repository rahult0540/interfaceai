# Repository owner setup

The repository is public. Anyone can read it; invited collaborators can contribute according to their granted access. Existing teammate access does not need a new invitation.

## Protect main

These are owner actions to complete in GitHub Settings; adding this file does not apply them.

Under repository Settings, use Rules > Rulesets (or Branches > branch protection) to create an active rule targeting the default branch `main`:

- Require a pull request before merging.
- Require one approving review and dismiss stale approvals when new commits are pushed.
- Require code owner review. The default owner is @rahult0540 in `.github/CODEOWNERS`.
- Block force pushes and branch deletion.
- Keep bypass access limited to necessary repository administrators.

The author cannot approve their own pull request. With the current CODEOWNERS file, owner-authored changes need another eligible reviewer and may need an additional code owner before required code owner review can be satisfied. Add another maintainer only after confirming their exact GitHub username and write access.

There are currently no automated application checks. Do not require a status check that does not exist; use the manual checks in CONTRIBUTING.md. Add CI when the application tooling is introduced.

## Merge settings

Under Settings > General > Pull Requests, enable squash merging and automatic deletion of head branches. Prefer squash merge for a single reviewed commit per task. These settings have not been changed by this setup pull request.

## Team routine

1. Assign a task and create a short-lived branch.
2. Preview locally and open a pull request into main.
3. Request a teammate's review and address feedback.
4. Merge approved work and update local main.
5. Coordinate manual Hostinger deployment separately.

Use personal accounts and credentials. Periodically review Settings > Collaborators and remove access when no longer needed. Public visibility is independent of collaborator permissions.

## Scope

The repository contains a static website and documentation. The README describes a FastAPI prototype, but that backend is not in this repository. There is no backend setup or deployment pipeline to run here.
