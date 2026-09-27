---
name: eli5
description: >
  Explain something complicated one small chunk at a time, stopping after each one so the
  user can say "next", and building toward a conclusion rather than dumping a summary.
  Use when the user says "eli5", "explain it like I'm five", "break this down", "walk me
  through it", "I don't have context on this", "one at a time" - and especially when they
  say "too much", "that's too long" or "smaller chunks" about something you just wrote.
  Also reach for it unprompted when you are about to explain an unfamiliar domain to
  somebody who has told you they lack context in it.
---

# ELI5 - explain it in chunks that link

Somebody needs to understand something they did not build. The instinct is to write a
good, complete explanation. That instinct is the problem: a complete explanation arrives
as a wall, and a wall is read once, skimmed, and not retained.

This skill trades completeness-per-message for **retention**. One idea, then stop.

## The mechanic

1. Say roughly how many chunks it will take. Do not list them.
2. Write **one** chunk.
3. **Stop.** End your message. Do not write the next one.
4. Wait for the user to say `next` (or `ok`, or `k`, or anything).
5. Repeat until the conclusions land.

Step 3 is the whole skill. Everything else is detail.

## What one chunk looks like

**The scroll test: if the reader has to scroll, it is not a chunk.** That is the only
size rule that matters. Roughly 100-250 words, one idea, and it must fit on a screen.

Anatomy:

```
## 5. Case 1 - the magazine

[one idea, made concrete]

**Next up:** [one line, forward hook]
```

- **Numbered**, so the reader knows where they are in the arc.
- **A title that names the idea**, not "Part 5".
- **One forward hook at the end.** This is what makes them *chunks that link* rather
  than slides. It also earns the next `next`.

## Make it concrete, always

Abstraction is what made the thing hard in the first place. Do not re-abstract it.

| Don't | Do |
|---|---|
| "the row references a pricing entity" | `prezzo -> TESS_FULL (110,00)` |
| "there is a uniqueness concern" | show the four lines of the actual constraint |
| "the two fields are conflated" | show one real row and ask it two questions |

Real names, real numbers, real code - as long as it fits. A five-line snippet the reader
can actually look at beats a paragraph describing it.

## Build an argument, not a list

Chunks accumulate. Each one should be load-bearing for the next, and the reader should
be able to feel the thing assembling. A good arc:

1. **Ground it** - the concrete thing, as it exists today
2. **Find the tension** - what quietly stopped being true
3. **Name the idea** - usually one sentence, and it should feel small
4. **Work the cases** - the idea doing actual work, one case per chunk
5. **Land the conclusions** - in their own chunks, stated plainly

Do not tag conclusions inline as you go. Let them arrive at the end, where they land
harder because the reader built to them.

## When they push back, stop and fix it

If the user offers their own summary - *"so it was X, right?"* - that is the highest
value moment in the whole exchange. Answer it **immediately and honestly**, before
continuing:

- say plainly which half is right
- say plainly which half is off, and which way
- if the real answer runs opposite to their read, say so **now**, not in three chunks

A wrong model compounds. Every later chunk gets filed under it. Correcting it costs one
short message; leaving it costs the whole explanation.

Then return to the flow and offer `next`.

## When to abandon the format

Watch for impatience and honour it instantly. Tells: *"not interested in that bit"*,
*"I just want to ship"*, *"skip ahead"*, *"what do I actually do"*.

When you see one, **stop chunking mid-arc** and switch to compressed mode: the remaining
material in a few lines, then the practical answer they are actually reaching for. Do not
finish the arc for the sake of finishing it, and do not ask permission to stop.

The skill serves understanding. Once understanding is no longer the bottleneck, drop it.

## Explaining is not the same as simplifying

Never buy clarity with accuracy. If a claim can be checked - a file, a line, a constraint,
a ticket - **check it before you teach it.** A confidently wrong simple explanation is
worse than the wall it replaced, because it gets believed.

Where the honest answer is "this bit is genuinely uncertain" or "the document asserts
this and the code does not support it", that is a chunk of its own. Say it.

## Failure modes

These are the ways this goes wrong. All three feel like chunking and are not.

**Writing the whole thing with sub-headings.** Sections in one message are still one
message. The reader still scrolls.

**Writing "Step 1 ... Step 12" in one message.** Numbering is not pacing. This is the
most seductive failure: it looks like exactly what was asked for, and it is a wall with
numbers on it.

**Bundling "because they belong together".** Two ideas that depend on each other are two
chunks, and the dependency is what the forward hook is for. Material never justifies a
double chunk - if it seems to, the split is in the wrong place.

If you have already been told "too much" once, assume your next instinct is still too
big and halve it.
