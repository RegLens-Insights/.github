# RegLens

**Regulatory intelligence, before it lands.**

RegLens tracks federal and 50-state legislation, Federal Register rulemaking,
federal court opinions and congressional hearings — then scores each item for
regulatory risk and industry impact and surfaces it as watchlists, alerts,
digests and organization-level exposure analysis.

It is live at **[reglens.info](https://www.reglens.info)** as free early access.

## What we track

| Corpus | Upstream source | Open to everyone |
| --- | --- | --- |
| Federal bills | Congress.gov (US government, public domain) | [Jurisdiction hubs](https://www.reglens.info/states), [Atom feed](https://msontjctxpthnmdhcmvu.supabase.co/functions/v1/feeds?feed=us), individual bill pages |
| State bills — 50 states + DC | LegiScan | [Per-state hubs](https://www.reglens.info/states), individual bill pages |
| Agency rulemaking | Federal Register | Account required |
| Federal court opinions | CourtListener | Account required |
| Congressional hearings | Congress.gov | Account required |

Per-state Atom feeds exist and are valid to subscribe to, but are not
publishing entries yet — we are confirming redistribution terms with our state
legislative data supplier first. The federal feed is public-domain data and is
live now.

A live **[coverage board](https://github.com/RegLens-Insights/.github/blob/main/COVERAGE.md)**
shows per-jurisdiction freshness and bill counts, regenerated every 6 hours,
with stale lanes named rather than hidden. An upstream access issue with our
state legislative data supplier kept many state lanes stale from mid-July;
access was restored on **2026-08-22** and those lanes are refreshing again —
the board records each one's recovery as its backlog drains.

## How scoring works

Every bill analysis produces five dimension scores on a 1–5 scale, combined
into a weighted composite that sets a risk tier, plus a passage likelihood that
can escalate that tier or cap it. Agency rules use a three-dimension variant.
The dimensions, weights and thresholds are all published at
**[reglens.info/methodology](https://www.reglens.info/methodology)**, and the
full specification — including the prompts the model actually receives — is in
**[reglens-method](https://github.com/RegLens-Insights/reglens-method)**.

Given a published assessment's five dimension scores you can reproduce its risk
tier by hand. That is the point of publishing it.

RegLens scores are analytical estimates — not legal, investment or compliance
advice.

## Look before you sign up

- **[reglens.info/states](https://www.reglens.info/states)** — every
  jurisdiction and what is moving in each
- Individual bill pages, including the per-dimension rationales behind a score
- **[The federal Atom feed](https://msontjctxpthnmdhcmvu.supabase.co/functions/v1/feeds?feed=us)**
- **[reglens.info/architecture](https://www.reglens.info/architecture)** — how the
  pipeline works: five sources, ingest, AI scoring, and what it powers
- [Methodology](https://www.reglens.info/methodology) ·
  [FAQ](https://www.reglens.info/faq) ·
  [System status](https://www.reglens.info/status)

## Repositories

| Repo | What it does |
| --- | --- |
| [reglens-method](https://github.com/RegLens-Insights/reglens-method) | The scoring rubric: dimensions, weights, tier thresholds, the prompts verbatim, and a changelog. |

The RegLens application itself is closed source.

## Links

- **[reglens.info](https://www.reglens.info)**
- [Methodology](https://www.reglens.info/methodology) ·
  [Architecture](https://www.reglens.info/architecture) ·
  [System status](https://www.reglens.info/status) ·
  [Terms](https://www.reglens.info/terms) ·
  [Privacy](https://www.reglens.info/privacy)
