---
name: new-project
description: Start a project with a living context. Asks what the project is about, then creates CLAUDE.md (what it is and how we work), STATE.md (where things stand) and DECISIONS.md (why) in the project folder. Use when the user starts a new project ("let's start a new project", "set up this project"), or opens a folder that has no STATE.md and wants Claude to keep track of the work across sessions.
---

You are starting a project so that every later session can pick it up cheaply from three small files.

## 1. Ask what the project is — like a person, not a form

Ask one or two questions at a time. Gather the charter: what it is (one sentence) · why, the goal ·
done when · constraints · non-goals. If the user has already said all of it, don't ask again.

The charter is a living hypothesis, not a contract. "Don't know yet" is a valid answer, and an empty
field is a signal too. For creative or research projects, "done when" and "non-goals" can wait.

**Write down only what the user said.** Don't add constraints, rules, reasons or sections of your own,
and don't turn their words into slogans. If something seems missing, ask; if they don't know, write
"don't know yet".

## 2. Notice what will grow — but don't create it

Ask yourself what knowledge will pile up here that won't fit in three files: sources, a glossary,
test notes, a list of contacts. Name one or two such files to the user as a guess. Don't create them:
extra files are born later, and only when the need keeps coming back.

## 3. Lay out the files

Use the current folder unless the user wants a new one. Use the three templates below as they are,
filling in only the parts in angle brackets.

- **No CLAUDE.md yet:** create it from the CLAUDE.md template.
- **CLAUDE.md already exists** (for example, one written by `/init`): don't overwrite it. Show the user
  the Charter and "How this project breathes" sections and, on their yes, add them at the top of the
  existing file. Everything that was there stays.
- Create STATE.md with the phase and the first next step.
- Create DECISIONS.md. Add an entry only for a decision the user actually made in this conversation,
  with the reason they gave; otherwise leave the header alone.

Don't create INBOX.md now: `park` creates it the first time a thought is parked.

### CLAUDE.md template

```markdown
# <Project> — living context

> Claude reads this file at the start of every session. Keep it small and honest.
> Where things stand lives in STATE.md; why things were decided lives in DECISIONS.md.

## 1. Charter — a living hypothesis, not a contract
("Don't know yet" is a valid answer. Revisit it at wrap-up.)
- What it is: <…>
- Why / goal: <…>
- Done when: <…>
- Constraints: <…>
- Non-goals: <…>

## 2. Files
The spine: this file (what and how) · STATE.md (where we are) · DECISIONS.md (why) ·
INBOX.md (parked thoughts, created when the first one arrives).
Extra files (born when a need keeps coming back): —
How to run · how to ship: — (one line, a command rather than a story, as soon as there is
something to run or ship)

## 3. How this project breathes
- **Session start:** read this file → STATE.md → DECISIONS.md → any extra file the task needs.
- **While working:** give every settled thing its home and say where you put it — a decision and its
  reason → DECISIONS.md · a finished milestone → STATE.md · knowledge that keeps piling up → its own
  file (propose it, create it on "yes") · a stray thought → INBOX.md.
- **Wrap-up:** when a meaningful piece is done, or the session has grown long, offer to wrap up.
  Nobody has to remember commands.

## 4. Keeping the files useful
Two rules hold the rest: keep the signal, not the log · write for the one who wasn't here — the next
session, or the next person.
From them: one fact, one home · what is stable apart from what changes · structure only as heavy as
the project · a new rule replaces an old one instead of piling up · every file stays short enough to
read in one sitting.
```

### STATE.md template

```markdown
# STATE — where we are

**Phase:** start.

**Next step:** <…>
```

### DECISIONS.md template

```markdown
# DECISIONS — why

Only the reasons that can't be read from the result itself. New entries go at the bottom;
old ones are never rewritten.
```

An entry, when there is one: `## YYYY-MM-DD · <the decision>` and the reason in a few lines.

## 4. Hand over

Name the files you created and give the first next step. Then say in one line how the project goes on:
work as usual; say "that's it for today" when you stop and "let's continue <the project>" when you come
back —
the `wrap-up` and `catch-up` skills take it from there.
