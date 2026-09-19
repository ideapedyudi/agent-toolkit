---
description: Run npm run build, stage all changes, commit with an
  auto-generated Conventional Commits message in English, and push to the remote.
agent: build
---

Build, then commit and push the current git changes immediately. Do not create a todo list or ask for confirmation unless there is a build failure, merge conflict, authentication issue, or another blocking error.

Run these commands directly:

```bash
npm run build
git status
git diff --staged
git diff
git add .
git commit -m "<generated message>"
git push
```

If `npm run build` fails, fix the errors and re-run it until it succeeds before committing.

Generate the commit message in English using Conventional Commits:
- `<type>(<scope>): <short description>`
- Imperative mood, max 72 chars for subject
- No trailing period

Report only the build result, commit hash, and push result after completion.

$ARGUMENTS