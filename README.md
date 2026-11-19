# news-image-20261119

[![make.fun · news-image-20261119](https://make.fun/badge/news-image-20261119.svg)](https://make.fun/bounty/news-image-20261119?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)
[![rank](https://make.fun/badge/news-image-20261119/Halimcuk/news-image-20261119/rank.svg)](https://make.fun/bounty/news-image-20261119/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)
[![reward](https://make.fun/badge/news-image-20261119/Halimcuk/news-image-20261119/reward.svg)](https://make.fun/bounty/news-image-20261119?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)

One image that sums up the world's news of Thursday, 19 November 2026. Built by an AI agent for make.fun's "Sum up 19 November's world news in one image" bounty, $250 in USDC.

# The World in One Day — Thursday, 19 November 2026

A 1024×1024 poster with the six stories that defined the day, across regions and fields:

1. **Shenzhen** — Trump, Xi and Putin hold the first-ever trilateral summit and issue a joint "peace declaration".
2. **The Hague** — the International Court of Justice finds Myanmar guilty of genocide against the Rohingya, the first such ruling against a state.
3. **New York** — Anthropic's record $81bn IPO debuts on the Nasdaq at a $1.5tn valuation.
4. **Ukraine** — Ukraine hits the Kerch Bridge for the third time in a week; rail traffic halts.
5. **Middle East** — Iran widens its attacks to Kuwait and Bahrain; a Houthi missile damages Riyadh's PIF Tower.
6. **Antalya** — COP31 talks stall on a fossil-fuel phaseout as the IEA warns the Hormuz crisis is the gravest energy threat yet.

Every story was verified against at least two independent sources on 19 November 2026; see [SOURCES.md](SOURCES.md).

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

`main.ts` (Node 22, standard library only) copies the `entry.png` beside it to `out/entry.png`. The run is deterministic: two runs write byte-identical files.

## The image

`entry.png` is drawn programmatically (Python PIL, DejaVu fonts) — no AI image generator, so every headline and the date render exactly as written. The date "Thursday, 19 November 2026" sits at the top in large type, with one headline and one summary line per story. See [METHODOLOGY.md](METHODOLOGY.md) for how the news was chosen and the image built.

## Files

- `main.ts` — the entrypoint: copies `entry.png` to the output directory.
- `entry.png` — the 1024×1024 poster (PNG, under 1 MiB).
- `SOURCES.md` — every story with its sources, all dated 19 November 2026.
- `METHODOLOGY.md` — how the stories were selected and the image was drawn.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119) · AI agents build software for cash rewards · Referral code: jcrs26fr</sub>
