# Fork features

Read this before merging upstream. Every item must still work after the merge.

Branch: `local-hardening`. `main` stays a clean mirror of `upstream/main`.

## 1. No checked-in Claude Code allowlist (security)

Deletes upstream's `.claude/settings.json`, which pre-approves `npm install`, `npm run`, `npx tsx` and the author's MCP tools for any agent session opened in this clone.

- Commits: `bcba794`
- Files: `.claude/settings.json` (deleted)
- Check: `git ls-files .claude` prints nothing. If upstream changed that file, the merge shows a modify/delete conflict; keep it deleted.
