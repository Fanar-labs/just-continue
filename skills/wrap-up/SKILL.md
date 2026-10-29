---
name: wrap-up
description: Close a working session so the next one starts cheaply. Rewrites STATE.md as a snapshot of now with the next step, adds the non-obvious reasons for decisions to DECISIONS.md, updates CLAUDE.md if the essence or the rules changed, and leaves a first message for the next session. Use when the user says "that's it for today", "let's wrap up", "let's stop here", or when a meaningful piece of work is finished and checked.
---

You are closing the session: stop, look at what was done, and move what matters from this
conversation into the files, so that the next session goes on without losses.

It fits when a meaningful piece is finished and works, before a break or the end of the day, or when
the session has grown long. Not in the middle of unfinished work: finish it first, or mark it
"in progress" in STATE.md.

## 0. Name the project

Say in one line which project you are wrapping up, and let the user correct you before you write
anything. If the session touched several projects, list them all and wrap up each in turn.
No STATE.md in the project → it hasn't been started with these files: offer `new-project` instead
of inventing them.

## 1. Rewrite STATE.md

Where we are now, and the next steps. STATE.md is a snapshot of the present, not a diary: remove what
is no longer true. End it with **Next step:** — concrete enough to start from tomorrow without this
conversation.

## 2. Add to DECISIONS.md — if decisions were made

Only the non-obvious *why*: what can't be read from the result itself. Take the reasons from the
conversation — the user's words, or what you worked out together — and don't add new ones of your
own. Add new entries at the bottom as `## YYYY-MM-DD · <the decision>` and a few lines. Never rewrite
old entries.

## 3. Update CLAUDE.md — only if it changed

The essence, the rules or the map of files changed → reflect it. Otherwise leave the file alone.

## 4. Look at the extra files

Suggest a new one if some knowledge keeps repeating and doesn't fit; suggest merging duplicates and
removing files nobody uses. Act on the user's yes.

## 5. Summarize

Briefly, in plain words: what was done in this session.

## 6. Hand over

Give a ready "first message for the next session": what to read and what the next step is. Its
source is the **Next step** in STATE.md — the chat is temporary, the file stays, and `catch-up` will
find it on its own. Suggest starting the next session fresh: the context comes back from the files,
not from the chat history.

## 7. Don't commit

Saving to version control is a separate step. If the project is a git repository, say in one line
that the files changed and can be committed — and commit only if the user asks.
