# Contributing to Interface AI

## First-time setup

Install Git and sign into your own GitHub account. Accept the repository invitation if one is pending. Use your own credentials; never share the owner's token or password.

```sh
git clone https://github.com/rahult0540/interfaceai.git
cd interfaceai
git config user.name "Your Name"
git config user.email "YOUR_GITHUB_VERIFIED_OR_NOREPLY_EMAIL"
```

Replace the quoted values with your details. These commands set identity for this clone only. Use the exact verified or private noreply email shown in your GitHub account settings. Commit identity does not authenticate you; use Git Credential Manager or your own SSH key for authentication.

## Work on a branch

Start each task from an updated main branch with a clean working directory:

```sh
git switch main
git pull --ff-only origin main
git switch -c feature/short-description
```

Use `fix/short-description` or `docs/short-description` when appropriate. Agree on task ownership before editing the same area.

## Preview and check

Open `index.html` in a browser. No package installation, backend, database or build is needed. Check desktop and mobile widths, section navigation, the contact link, and the browser console. Check documentation links when editing docs.

Before committing, inspect the changes:

```sh
git diff --check
git diff
git status --short
```

Keep credentials, customer records, production exports and hosting backups out of Git. The repository is public. Ignoring a file does not remove an already tracked file or erase history.

## Commit and request review

Stage only the files you intend to change; for example:

```sh
git add index.html
git commit -m "Fix mobile navigation spacing"
git push -u origin feature/short-description
```

Open a pull request into `main`, explain the change and checks performed, and request a teammate's review. Include screenshots for visual changes. Wait for approval before merging. This is the team workflow; enforcement requires the owner settings in [TEAM_SETUP.md](docs/TEAM_SETUP.md).

To bring main into an existing task branch, first commit your work, then:

```sh
git fetch origin
git merge origin/main
```

Resolve conflicts by reviewing both versions together. Stage resolved files and complete the merge commit, then preview again and push. Use `git merge --abort` if you need to stop the conflict resolution. Do not force-push shared branches.

After the pull request is merged:

```sh
git switch main
git pull --ff-only origin main
git branch -d feature/short-description
```

If local deletion is refused after a squash merge, verify the pull request is merged before deleting the branch through your Git client.

## Deployment

Follow [DEPLOYMENT.md](docs/DEPLOYMENT.md). Merging into GitHub does not deploy to Hostinger. Coordinate publishing with the repository owner and deploy the reviewed version from main.
