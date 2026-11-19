# Back-end sorting routine

The owner only dumps raw thoughts into the Rebuild Notebook page. All sorting happens here. Keep his side dead simple.

- Page: https://claude.ai/artifact/DvufVb7XNUjkStZvAfNpNL (source `app/index.html`). Don't add features to it without being asked. One box, one mic, one button.
- Dumps live in the page's database, collection `dumps`: `{raw, createdAt, sorted}`.
- His story and voice live in `settings/profile` (`text`). Read it before writing anything.

## When he says "sort my dumps" (or similar)

1. `ArtifactData` query `dumps` where `sorted == false`.
2. For each dump, decide for yourself what it is. Split it into 1–4 pieces, one idea each, and pick a pillar (below).
3. Write each piece to `library/<pillar>/<YYYY-MM-DD>-<short-slug>.md` using the template below.
4. Update the dump to `sorted: true` (pin `if_version`).
5. Commit and push, then tell him in a few lines what's ready to film. Lead with the strongest one.

## Pillars

`owning-it`, `pit-and-back`, `dad-from-1900km`, `training-discipline`, `philosophy`, `people-can-change`, `building-the-empire`, `leading-people`

## Voice

Keep it raw, direct, first person and Australian. Keep his swearing if he swears. Reuse his own phrases. No guru-speak, no emojis, no invented facts.

## Safety (non-negotiable)

Anything touching suicide or self-harm: write about surviving and hope, never methods. End the caption with "If you're in a dark place right now, call Lifeline on 13 11 14. Seriously. Make the call." If a dump reads like he's in crisis *now*, stop sorting and check on him first.

## Piece template

```
# <Hook 1>
Pillar: <pillar> · Format: <Talking head reel | Running/training reel | Carousel | Quote post> · Status: idea
Source dump: <dump id>

## Hooks
- ...
## Reel script (30–60s)
...
## Caption
... #tags
## Carousel
1. ...
## Quote card
...
## Story prompt
...
```
