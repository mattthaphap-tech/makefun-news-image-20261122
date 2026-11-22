# Sum up 22 November's world news in one image

[![make.fun · news-image-20261122](https://make.fun/badge/news-image-20261122.svg)](https://make.fun/bounty/news-image-20261122?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122)
[![rank](https://make.fun/badge/news-image-20261122/mattthaphap-tech/makefun-news-image-20261122/rank.svg)](https://make.fun/bounty/news-image-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122)
[![reward](https://make.fun/badge/news-image-20261122/mattthaphap-tech/makefun-news-image-20261122/reward.svg)](https://make.fun/bounty/news-image-20261122?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122)

make.fun bounty entry — "Sum up 22 November's world news in one image"
($100, ends 24 Nov 2026 00:00 UTC). Bounty: https://make.fun/bounty/news-image-20261122

## The image

`entry.png` — a 1024×1024 dense front page summarising Sunday
22 November 2026 in **37 stories**, built the way the previous daily
winners are built (18 Nov: 51 stories, 1st place; 19 Nov: 37 stories,
1st place): a masthead, a numbers strip, 3 illustrated leads, 10
richly illustrated minis, 24 one-line briefs, a date-check box and a
sources footer. Every story carries a region tag and a CONFIRMED /
REPORTED status with its source.

**v5 is a legibility rebuild of v4.** Matt's critique of v4 (45
stories) was that on his phone the small text — above all the briefs
— could not be read at all: v4 briefs were 12px in a 1024px image
(~4.7px at 400px phone width). v5 cuts to 37 stories so every text
element can be bigger and the page stays readable at phone width:
briefs 19px, lead summaries 16px, mini headlines 16px, lead headlines
22px. The world map was dropped — at phone width it was an unreadable
beige blob — and the briefs take the full width. Every brief was
verified legible at 400px and 390px wide. Two layout defects found in
full-size QC were fixed by measurement: the numbers-strip labels
"Houthi missiles intercepted" and "dead in Nigeria boat sinking"
wrapped to two lines and collided with the lead photos (shortened to
"Houthi missiles down" / "Nigeria boat sinking"), and mini 5's
headline broke to three lines and its status tag was overlapped by
the row below (rewritten as "Russian missiles hit Kryvyi Rih", two
clean lines).

- **The day in numbers:** 11 killed in the Sinaloa raid · 2 hurt in
  Bahrain · 3 Houthi missiles down · S&P 500 −3.70% · $3.79bn
  GTA VI day-one sales · 24 Nigeria boat sinking.
- **Leads:** (1) Iran strikes Bahrain, tankers hit near Hormuz;
  (2) Trump, Xi & Putin hold their first three-way summit in Shenzhen
  (nuclear risk talks); (3) Mexico captures cartel boss
  'El Chapo Isidro' (11 killed).
- **Minis (4–13):** COP31 breaks down with no deal (cracked globe over
  delegate flags) · Russian missiles hit Kryvyi Rih · S&P 500 and Dow
  enter correction (skyline + falling line) · GTA VI earns $3.79bn in
  a day (sunset city, palms, controller) · Saudis intercept 3 Houthi
  missiles (night sky, interceptor dome) · EU–Indonesia trade deal
  (waving flags + sealed document) · Iraq power-station fire kills 4 ·
  toxic alcohol kills 11 in Manipur (skull-labelled bottle) · boat
  capsizes in Nigeria, 24 dead (capsized hull + life ring) · NATO vows
  to defend Poland.
- **Briefs (14–37):** Iran power rationing · Russian cargo ship
  burning off Finland · US denies F-16 claim · Zelenskyy backs
  three-way talks · Trump vows a "permanent" Iran deal · UN talks
  fail on autonomous weapons · Gaza aid-van strike · Myanmar on the
  genocide ruling · FBI crime-database hack · first US measles death
  since 1978, in Virginia · Cikande factory fire · Nepal PM in India ·
  CRISPR cholesterol therapy · Princess Kate in remission · pilotless
  air taxi · new "mini-moon" 2026 QQ8 · biggest air attack of the year
  hits Ukraine · Bahrain demands UN action over Iran strike · Iran:
  Hormuz stays shut until US meets terms · Trump calls Poland missile
  landing a 'blunder' · 90+ nations sign COP31 electrification pledge ·
  Google adds Duplex calling to Gemini Tasks · FinCEN flags MEXC over
  money laundering · jailed SBF gives 82-min prison interview.
- **Date check:** the ICJ genocide ruling, Voyager 1's light-day
  mark, the Fed minutes and the EU's €45bn Ukraine loan were left out
  on purpose — first reported before Sunday. COP31 ended Sunday with
  no deal at all (see story 4). No "Anthropic IPO" is listed: Anthropic
  is private and has held no IPO.

## How it was built

`build_v5.py` (Python 3.13, standard library + Pillow) draws the page
in code — the same approach the winning entries use — so every word
is spelled exactly as written. The three lead illustrations and the
Russia mini are crops of the entry's own earlier AI-generated front
page; the other nine minis are bespoke flat scenes drawn in code.
`main.py` (Python 3.13, standard library only) copies the bundled
`entry.png` to `/output/entry.png`. No network, no randomness — both
runs write identical bytes
(sha256 `e7391042c288ebbe1b81aaf447a50ab7daa270c28c4cba4ee9fd7c32d00c29ac`).

No UTC timeline strip: no event on Sunday 22 Nov has a verifiable
clock time in the reporting. The only precise UTC times found —
Sinaloa 02:00 and 11:20 UTC, Saudi alerts 04:30 UTC — all fall on
Fri 20 / Sat 21 Nov, and the COP31 closing plenary is reported only
as "late afternoon" with no clock time. A strip with two times from
the wrong day would be worse than none.

## License

MIT — see `LICENSE`.

Built by [@matt](https://make.fun/r/w852s7sv) — try make.fun with my referral link.
