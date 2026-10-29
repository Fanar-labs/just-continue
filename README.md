# just-continue

**Explain your project once. After that, name it and just continue.**

Every new session with Claude starts blank. What the project is, what you decided and why, what
comes next — you tell it all over again, or Claude guesses from whatever it finds in the folder.

just-continue gives each project a memory: three small files in the project folder. When you come
back, you say which project, and Claude is already up to speed.

> Not a log of everything that happened. Only what the next session needs: what the project is,
> where it stands, and why it was decided that way.

## Start

Open your project's folder in Cowork or Claude Code and say:

> Let's continue <your project>.

- **A brand-new project:** say *Let's start a new project* and answer two or three questions.
- **Already halfway through:** the same first line works. Claude sees there are no notes yet,
  offers to set them up, and fills them in from what you tell it.
- **From then on:** say *that's it for today* when you stop, and *let's continue <your project>*
  when you come back.

It needs a project folder. In a plain chat on claude.ai, files don't survive from one conversation
to the next, so there the plugin has nowhere to keep its memory.

## What coming back looks like

A test project, four days later. The whole message is one line:

> **you:** Let's continue the recipe site.

> **Claude:** **Grandma's Recipes:** a small static site with grandmother's recipes, so the family
> can open them on a phone.
>
> **Where we stopped:** the first version is written but has never run. That includes `build.py`,
> the mobile-first CSS, the in-browser search and one recipe. Bash wasn't available last session.
> The one recipe, borscht, is my draft, not Grandma's wording, and the page says so.
>
> **Next step:** run `python3 build.py`, open `site/index.html` and fix whatever breaks. Then
> replace the borscht draft with Grandma's own text.
>
> **Parked thought (1):**
> - maybe a print-friendly version of each recipe. This may already be covered, since `style.css`
>   is supposed to print cleanly.
>
> Sort it now? Or continue with the first build run?

Without these files, Claude has only the code to guess from.

## How it works

Work on a project gets lost at four moments: when it starts without a clear idea of what it is,
when a new session has to be told everything again, when a session ends and its decisions stay in
the chat, and when a stray thought either disappears or derails the work. There is one skill for
each moment.

| skill | when | what it does |
|---|---|---|
| `new-project` | a project starts, or gets its notes halfway through | asks what the project is and where it stands, then creates `CLAUDE.md` (what it is and how we work), `STATE.md` (where things stand) and `DECISIONS.md` (why) |
| `catch-up` | you come back: "let's continue the recipe site" | finds the project, reads the three files, says where you stopped and what comes next — then you go on |
| `wrap-up` | a session ends: "that's it for today" | rewrites `STATE.md` as a snapshot of now, adds the reasons for decisions to `DECISIONS.md`, leaves the next step |
| `park` | any time: "park this: …" | adds a stray thought to `INBOX.md` as one line; it is sorted at the next catch-up |

You don't need to remember commands: say it in your own words, and Claude picks the matching
skill. In Claude Code they are also commands: `/just-continue:new-project`,
`/just-continue:catch-up`, `/just-continue:wrap-up`, `/just-continue:park`.

Several projects in one folder? Name the one you want. If you name none, Claude lists the most
recent ones and asks.

## Install

In Claude Code:

```
/plugin marketplace add Fanar-labs/just-continue
/plugin install just-continue@just-continue
```

## What it writes and sends

Plain Markdown files in your project folder: `CLAUDE.md`, `STATE.md`, `DECISIONS.md`, `INBOX.md`
and `INBOX-archive.md`. The plugin runs no scripts and sends nothing anywhere: Claude reads and
writes these files in your normal session. An existing `CLAUDE.md` is never overwritten — the
plugin asks before adding its sections to it.

The files are rewritten rather than piled up: `STATE.md` holds only what is true now, and
`DECISIONS.md` only the reasons you can't see in the result. They stay short enough to read in one
sitting — for you, for Claude, or for any other tool.

## Versions

- 0.2.1 · 2026-10-30 — "memory" in the description; a Start section; `new-project` records where a
  project already under way stands; in a plain chat the skills say there is no folder instead of
  writing files that vanish.
- 0.2.0 · 2026-10-30 — first public version.

## License

MIT © Fanarlabs
