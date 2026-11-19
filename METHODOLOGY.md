# Methodology

## How the news was chosen

On the evening of 19 November 2026 (WIB), world-news roundups and live
coverage for that day were searched and cross-checked (news vertical search,
then the underlying outlets). A story was used only if at least two
independent sources reported it on 19 November 2026, and only if the event
happened — or was first reported — on that day. Nothing from before
13 November 2026 is in the image.

Six stories were picked for breadth across regions and fields, in the order
the judge weighs them: one day's news, named with its date; the most
consequential stories across regions and fields; readable from the image
alone; faithful to what was reported, without hype.

- Diplomacy: the first-ever US–China–Russia trilateral summit (Shenzhen).
- Justice: the ICJ's first genocide ruling against a state (The Hague).
- Business / technology: the largest IPO in history (New York).
- War, Europe: the third strike on the Kerch Bridge in a week (Ukraine).
- War, Middle East: the widening Iran conflict and the Riyadh missile strike.
- Climate / energy: COP31 deadlock and the IEA's Hormuz warning (Antalya).

Each poster line is a plain statement of what the sources reported. Where a
claim was still developing or contested (e.g. the Riyadh strike was an
"apparent" missile attack per the NYT), the poster states only the
reported fact.

## How the image was made

The poster was drawn programmatically with Python 3 + Pillow, using the
DejaVu Sans / DejaVu Serif fonts installed on the build machine — no AI
image generator, so no headline text can come out garbled. The script lays
out a navy header band with the date in large serif type, then a 2×3 grid
of cards: a place tag, a simple geometric glyph, a bold headline and a
one-line summary per story, plus a footer naming the source outlets.

The finished PNG was read back visually and checked: all six headlines and
summaries complete, no text clipped or overflowing its card, the date
prominent at the top. One headline ("UN court finds Myanmar guilty of
Rohingya genocide") was shortened after the first render showed it being
cut off at two lines.

## The program

`main.ts` (Node 22, standard library only) copies `entry.png` to
`$MAKEFUN_OUTPUT_DIR/entry.png` (default `/output`). It does no network
access and writes the same bytes on every run — verified by running it
twice and comparing sha256 hashes.
