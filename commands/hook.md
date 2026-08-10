# bazable hook

Installs a **pre‑push Git hook** that runs `bazable inspect` before every `git push`.  
If contract violations are found, the push is blocked and the developer must fix them before pushing.

## Usage
```bash
bazable hook

Options
None.

## What it does
Creates (or overwrites) the file .git/hooks/pre-push in your repository.

The hook script runs bazable inspect automatically.

If bazable inspect exits with a non‑zero code (violations found), the push is aborted with a clear message.

If the inspection passes, the push proceeds normally.

## Skipping the hook
To temporarily bypass the check, set the environment variable BAZABLE_SKIP=1 before pushing:
```bash
BAZABLE_SKIP=1 git push

This is useful in emergencies or when you need to push a known‑broken contract quickly.

## Prerequisites
Your project must be a Git repository (run git init if needed).

Your project must contain a valid bazable.config.json.

## Example
```bash
cd my-project
bazable hook
Bazable Git hook installed! 'bazable inspect' will now run automatically before every git push.
