# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working in this workspace.

## Git & GitHub — always on, every session

Every project lives in its own git repository with a matching GitHub remote under **Didilan75**.

### Rules
- **Commit after every meaningful change** — don't batch unrelated work into one commit.
- **Push after every commit** — so GitHub always reflects the latest state and nothing is ever lost.
- **Never end a session without pushing** — even partial work should be committed with a `wip:` prefix if needed.

### Commit message format
```
<type>: <short imperative description>

<optional body — what changed and why>
```

Common types: `feat`, `fix`, `style`, `refactor`, `docs`, `chore`, `wip`

Examples:
```
feat: add restart button that resets scores
fix: prevent clicking a cell after game ends
style: increase board cell size on mobile
docs: update CLAUDE.md with git workflow
wip: halfway through adding AI opponent
```

### Workflow per change
```bash
git add <changed-files>
git commit -m "<type>: <description>"
git push
```

### Setting up a new project
```bash
cd D:/ClaudeCode/Workspaces/<project>
git init
git add .
git commit -m "feat: initial project setup"
gh repo create <project> --public --source=. --remote=origin --push --description "<short description>"
```

## Environment

- Platform: Windows 11, shell: bash
- GitHub account: Didilan75 (authenticated via `gh` CLI)
- Git identity: `Didilan75 <ilan.dahan@gmail.com>`
- Projects root: `D:/ClaudeCode/Workspaces/`
