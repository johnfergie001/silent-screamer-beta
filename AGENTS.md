# AGENTS.md — silent-screamer-beta

Shared rules for every agent in this repo (Claude Code, Codex, DeepSeek, any other). Single source of truth; `CLAUDE.md` points here.

## Read first (every session)
1. `VISION.md` — what this is, success criteria, out of scope.
2. `progress.json` — current phase and next agreed step; lead with it.

## Working rules
- GitHub is the source of truth for this project's code and docs; Google Drive is a mirror and asset bucket only.
- Terminal commands for John: PowerShell syntax, full file paths.
- Any action costing more than about $1-2 needs an explicit go-ahead.
- Never commit secrets; never read or print credential files.
- End meaningful sessions by updating the project docs listed above (`/update-docs`), including this file if a rule changed.
- Several agents may share a clone: work on your own branch or worktree, never switch the branch someone else has checked out.

---

# Session Scope Guardrail

This repository is one of John Fergie's real, live project repos. Read this before making any change here — especially if you are a freshly-started session, a cloud-hosted session, or otherwise have no direct memory of the conversation that led here.

## Hard rule

Do not commit, push, open a PR, or otherwise write to this repository unless:

1. The current conversation contains an explicit, current instruction from John naming this repo and the specific issue/task, **and**
2. You have stated back to John, in this same session, which repo and task you are about to act on, and received confirmation.

If you cannot satisfy both conditions — including because a prior session ended, context was lost, or you are inferring intent from a task description rather than a direct instruction in front of you right now — **stop and ask John to confirm before writing anything.**

## Why this file exists

On 2026-08-20/21, a Claude Code cloud session picked up an in-progress multi-repo trial after the original local session appeared to disconnect. Lacking any memory of the original plan, it substituted an unrelated mechanism, briefly targeted the wrong repository, and then continued running real autonomous work against real repos after explicitly stating out loud that it was not doing what had actually been agreed — because "keep going" was read as blanket permission rather than confirmation of the immediate step. Full incident record: `AIS-OS` `decisions/log.md`, 2026-08-21 entry.

## Always safe, no confirmation needed

- Reading, exploring, and explaining code in this repo.
- Answering questions about it.
- Proposing a plan or diff for John to review, without pushing anything.

## Always needs a fresh, explicit go-ahead in the *current* session

- Any `git push`, branch, commit, or PR against this repository.
- Resuming or continuing work described in an earlier session you have no direct transcript of.
- Treating a task list, issue body, or prior summary as itself sufficient authorization to act.
- Assuming two systems are the same because they use similar terminology (e.g. "worktree isolation" in Claude Code's own Agent tool vs. Paperclip's `git_worktree` workspace policy — these are unrelated).
