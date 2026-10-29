---
name: park
description: Park a stray thought in INBOX.md without derailing the current work. Appends it as one dated line and confirms. Use when the user says "park this", "note for later", "inbox: …", "remind me later about …", or throws in an idea unrelated to the task at hand. Only captures — sorting happens in catch-up.
---

You catch a thought and drop it into the inbox without sorting it. Capturing and sorting are
different jobs; yours is capturing.

1. Take the thought: everything after "park", "note for later", "inbox" and the like. If there is
   nothing, ask once: "What should I park?"
2. Find INBOX.md in the project folder, next to STATE.md. If there is none, create it with exactly
   this text:

   ```markdown
   # INBOX — parked thoughts

   One thought per line, newest at the bottom. Nothing here is sorted yet: `catch-up` sorts it and
   moves each line to INBOX-archive.md.

   <!-- write below this line -->
   ```
3. Add one line at the very bottom, below `<!-- write below this line -->`:
   `- [YYYY-MM-DD] <the thought>`, with today's date. Several thoughts → several lines.
   Never edit or remove other lines.
4. Confirm in one line — "Parked:" and the thought echoed back — and return to the task at hand.

Rules: append only · one thought, one line · don't judge, classify or discuss it: the inbox holds,
it doesn't think. If the user asks to sort the inbox, that is `catch-up`.
