---
title: "diff-tour: guided review of agent code changes"
source: "Telegram"
captured_at: "2026-10-24"
status: pending_review
---

# diff-tour: guided review of agent code changes

## Source

- https://github.com/init-co-jp/diff-tour
- Telegram attachment: `1792795399-TWMate.com-090e76d40d094e23c38daced601d038f.mp4` (local intake attachment; not copied into this public repository)

## User-provided description

`diff-tour` gives a read-only, developer-style walkthrough of agent-generated changes before merge. It explains intent, proposes a reading order including related unchanged files, checks compatibility, failure/retry behavior and rollback safety, separates required fixes from optional improvements, and pauses for prediction questions before explanations. The installer reportedly verifies downloads by checksum and installs in the user directory. The suggested workflow is to run `tour` before merge, then pass mandatory findings to an implementation agent for an approval-gated fix and test cycle.

## Review status

Repository implementation, installer safety, permissions, checksum verification, and Claude Code/Codex integration have not yet been independently inspected.
