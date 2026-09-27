---
name: desktop-summary
description: Write an executive summary as a markdown file on the Desktop, in the house 3-bullet style, ready to copy-paste into Microsoft Teams. Use whenever the user asks for a summary/brief/message to send to a colleague, client, or stakeholder — "summarise this for Teams", "write up where we got to on #NNN", "make a brief on the <redacted>", "desktop summary of this spike" — and for follow-up revisions to one already written ("make it five bullets", "now write it in Italian").
---

The point is to boil a lot of information down into something a person can take in at a glance, which is why the default is three bullets. It is a strong first draft, not the finished message: the user touches it up personally before sending.

## The format — non-negotiable

**Always write 3 bullets.** Do not decide on your own to write more or fewer; the user asks for a different count when they want one (see Revisions), and 6 is the hard ceiling even then. If the material overflows 3, cut scope or split into two summaries — do not extend the list.

Every bullet opens with its claim as a plain first sentence, ending in a full stop, then one or two sentences that back it. The first sentence must carry the message on its own: a reader who scans only the opening sentences should get the whole picture. The rest supplies the detail that makes it actionable.

**Never open a bullet with a bold phrase.** Bold lead-ins read as patronising to the recipient, they are an instant tell that the message was written with AI, and the user strips them by hand every time. They are ornament, and ornament distracts from the information. The structure (claim first, detail after) stays; only the bold lead-in goes.

**Bold is scarce, so use it strategically or not at all.** The more of it there is, the less any of it means. Reserve it for the one thing the reader must not miss, such as a deadline, a hard blocker, or a decision needed from them, and expect most summaries to need none. A handful of words in the whole message is the ceiling, never one per bullet.

```
- Manca solo il deploy: il servizio non gira da nessuna parte. Nessuna istanza accesa, nessun owner.
- Ci serve AWS: su quale account gira, con Bedrock e Textract abilitati nella region giusta (sono dati personali, quindi la region va confermata). È l'unica dipendenza pesante: il container in sé è leggero, solo CPU, niente GPU.
```

Bullets are ordered by what the reader needs first — usually state of play, then the blocker, then the ask. Not chronologically.

## Register

Executive, but technical, and deliberately dry. A summary is a factual transfer of information, not a narrative: no storytelling, no persuasion, no emphasis for effect. Dispassionate is the target; if a sentence is there to make the reader feel something rather than know something, cut it. The reader is a senior colleague or a client-side decision maker: they know the domain, they do not know this week's detail, and they will not read a second screen. Name the real things — services, tickets, accounts, regions, people — but never walk through implementation. Concrete over hedged: "the service runs nowhere" beats "deployment status is currently unclear".

**No em dashes.** They read as machine-written, and in a message going out under the user's own name that costs far more than the punctuation gains. Use a comma, a colon, parentheses, or start a second sentence. Applies to the Italian versions too, and to any revision.

Keep the whole body under roughly 200 words.

## Shape of the file

1. **Title line** — short, topic-first (`# <redacted> — richiesta di deploy`). Optional for very short notes; a plain first line works too (`<redacted>`).
2. **Metadata line** — only when it's a message with named recipients: `**A:** <redacted>, <redacted> · **Da:** Thomas · 21 luglio 2026`, then a `Rif:` line with markdown links to the milestone / ticket / Jira issue. Skip both lines for a general write-up.
3. **One-line opener** — greeting plus what this is about, when addressed to people.
4. **The bullets.**
5. **The ask.** Close on a direct question that names what the user wants next: *"Chi di voi può prenderlo in carico?"*, *"Possiamo discutere domani?"* A summary with no ask has no reason to have been sent — if there genuinely isn't one, say so and confirm before omitting it.
6. **Optional `*Nota (non inviare)*` footer** — the user's own reference material (linked tickets, context not for the recipient), clearly marked as not part of the paste.

## Teams paste

The safe subset that survives pasting into the Teams compose box: `-` bullets, `[text](url)` links, `` `inline code` `` (bold survives too, but see the format rule on keeping it scarce). Avoid tables, nested bullets, and `---` rules — they flatten or paste literally. Headings and long link URLs are a judgment call; if the summary is short, a bold first line is the safer title.

## Language

**Always write in English first.** Never ask which language, and never pre-empt with an Italian version — even when the recipients are <redacted> or other Italian client-side readers. Italian happens only as a revision the user explicitly asks for.

## Revisions

Writing the file is the first step of a loop, not the end of it. The user reads the draft and comes back with adjustments; expect them and keep the same source material rather than re-deriving it.

The two standing ones:

- **"Make it five bullets"** (or two, four, six) — rewrite at that count. This is a re-cut, not an append or a deletion: pick the bullets that carry the message at the new length and re-balance them, rather than bolting new ones on the end or dropping the last one and leaving the rest untouched. Same file, overwritten.
- **"Now write it in Italian"** — translate the current version, at whatever bullet count it now stands. Write it as a **new file with an `-IT` suffix** (`<redacted>-deploy-messaggio-IT.md`), leaving the English file in place, and report both paths.

Translate into the register a native writer would use for the same message to that reader — not word-for-word from the English. Keep the claim-first bullets (no bold lead-ins), the ordering, and the closing ask intact. Ticket numbers, links, service names, and technical terms of art stay as they are.

Any later revision applies to whichever version is in play; if both an English and an Italian file exist and the instruction is ambiguous, ask which one before overwriting.

## Writing the file

Save to `C:\Users\utente\Desktop\<slug>.md` — short kebab-case topic slug (`<redacted>-brief.md`, `SDLC-summary.md`). Report the path back. Do not print the full body into the conversation — the file is the deliverable.

For a **new** summary, check whether the path already exists first; if it does and it isn't this session's own draft, confirm overwrite or pick a different slug. Revisions to a summary written in this session overwrite their file directly — no confirmation needed.

## Grounding

These get sent to real colleagues and to the client, so every factual claim must come from something checked in this session — the ticket, the diff, the memory file, the conversation — not from inference. Verify ticket numbers, milestone links, and merge status before asserting them. If a bullet needs a fact you don't have, ask rather than hedge it into vagueness.

Never send, post, or share the summary anywhere. This skill writes a local file; the user does the pasting.
