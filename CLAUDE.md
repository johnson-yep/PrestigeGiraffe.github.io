# Project Instructions for Claude Code

## Always Sync With GitHub Before Editing

Before starting **any** edits, file creation, or refactoring in this project, you MUST first sync the local repository with the latest version on GitHub. Do not skip this step, even for small changes.

### Required steps (in order)

1. **Check the current state of the repo:**
   ```bash
   git status
   git branch --show-current
   ```

2. **If there are uncommitted local changes**, do NOT discard them. Stop and ask me whether to commit them, stash them, or discard them before proceeding.

3. **Fetch and merge the latest changes from the remote:**
   ```bash
   git fetch origin
   git merge origin/<current-branch>
   ```
   (Or `git pull` on the current branch — but always know which branch you're on first.)

4. **If there are merge conflicts:**
   - Do not blindly resolve them by picking one side.
   - List the conflicting files and summarize what each side changed.
   - Ask me how to resolve any conflict where the correct resolution isn't obvious.

5. **Confirm the sync succeeded** (`git status` shows the branch is up to date with `origin/<branch>`) before making any edits.

### Notes

- This applies at the **start of every session/task**, not just once. If significant time has passed mid-session (or I mention I pushed changes from elsewhere), re-sync before continuing.
- Never use `git push --force`, `git reset --hard origin/...`, or anything else that could destroy local or remote work without my explicit approval.
- If the remote is unreachable (no network, auth failure), tell me and ask whether to proceed with edits anyway rather than silently continuing.
