---
name: catch-up
description: Pick up a project where it was left, so the user can just continue without re-explaining it. Reads CLAUDE.md, STATE.md and DECISIONS.md, says in a sentence or two what the project is, where it stopped and what comes next, and offers to sort any parked thoughts in INBOX.md. Use at the start of a session or after a break — when the user names a project to go on with ("let's continue the recipe site", "back to the newsletter", "let's work on X"), or asks "where were we?", "catch me up", "what's next on this project?".
---

You are opening a session so that the user doesn't have to re-explain anything. Read only what this
needs.

## 1. Find the project

- The user named the project, and the current folder or a folder inside it matches — by the folder's
  name or by "What it is" in its CLAUDE.md → that is the project. Go there without asking.
- The current folder has STATE.md → that is the project.
- It doesn't, but folders inside it do, and none matches what the user said → list those projects by
  when their STATE.md last changed, newest first (at most five), and ask which one. Then work in that
  folder.
- No STATE.md anywhere → this project hasn't been started with these files yet. Offer `new-project`;
  don't invent the files.

## 2. Read

CLAUDE.md → STATE.md → DECISIONS.md. In DECISIONS.md the latest entries are enough, unless the next
step depends on an older one. If INBOX.md exists, count the thoughts below its line.

## 3. Report

Like a colleague after a break: straight to the point, no welcome.

- the project in one line, from "What it is" in the charter — so the user sees at once which project
  this is;
- where we stopped, in one or two sentences;
- the next step, as STATE.md states it;
- the parked thoughts, if there are any: up to five — list them, one short line each; more than five —
  give the count and the newest three. Then: "Sort them now?"

If the user already said what to do in this session, don't ask — start on it. Otherwise ask:
"Continue with <the next step>?"

## 4. Sort the parked thoughts — only on the user's yes

Take each line in turn and say where it goes:

- a settled fact or a decision → STATE.md or DECISIONS.md;
- knowledge that keeps coming back → an extra file (propose it, create it on yes);
- something to do later → the next steps in STATE.md;
- nothing worth keeping → nowhere, it is only archived.

Move every sorted line to `INBOX-archive.md` — append it with today's date and where it went.
Never delete a thought. Leave INBOX.md with its header and its line, empty below.
