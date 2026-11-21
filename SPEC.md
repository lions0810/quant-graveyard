# Build Spec — Public Quant Graveyard Repo

## Mission
Turn the raw research reports in `raw_reports/` into a polished, public GitHub repository:
the public graveyard of a nightly quantitative research desk. Every entry is a hypothesis
that was tested under pre-registered kill rules and died. The graveyard is the product:
proof of a disciplined research process, published with the numbers attached.

## Source material
- `raw_reports/` contains 25 original reports (Traditional Chinese) covering 24 research
  items: crypto series Q2, Q4–Q13 and tokenized-US-stock series T1–T13 (T8 has two files:
  the main report and a live feasibility follow-up).
- Two further items, Q1 and Q3, are WITHHELD: they are health checks of a live, commercial
  trading system. List them in the index as "WITHHELD — live-system health check, details
  not published". Do not invent any content for them.

## Deliverables (in this repo, on a pull request — do not merge)
1. `README.md` — what this desk is, the kill rules (below), how to read an entry, and the
   headline count: 24 hypotheses tested, 0 survivors. English.
2. `GRAVEYARD.md` — index table: ID, date tested, market (Crypto / US-stock tokens),
   one-line hypothesis, verdict, single most decisive statistic. One row per item,
   including the two WITHHELD rows.
3. `entries/<id>.md` — one English page per research item (25 source files → 24 entries;
   merge T8's two files into one entry). Each entry must contain:
   - the pre-registered question and kill criteria, as stated in the source report
   - data scope (instruments, timeframe, sample size, period)
   - method in brief
   - the decisive results — every number copied exactly from the source report
   - the verdict and what was NOT built because of it (no strategy / no survivor tag /
     line closed), exactly as the source concludes
4. Keep `raw_reports/` untouched as the provenance layer; link each entry to its raw file.

## The kill rules (for README.md — state them verbatim in substance)
A hypothesis is registered before it is tested, with its kill criteria committed first.
It survives only if ALL of the following hold:
- full available history, no cherry-picked windows
- trading costs deducted (fees, and spread/slippage where applicable)
- execution at the next bar's open — never the signal bar's close
- the effect holds out-of-sample and across sub-periods (weekday/weekend, per-year,
  per-instrument splits where the report uses them)
- for strategies: it must materially beat buy-and-hold, not merely be positive
- multiple-comparison discipline where the report applies it (e.g. Bonferroni thresholds)
Even a survivor is not traded: it must then pass a 90-day paper-forward trial with at
least 30 closed trades, profit factor ≥ 1.30, and max drawdown no worse than −20%
before any live discussion. Promotion decisions belong to the human owner alone.

## Hard constraints
- NEVER publish parameters, rules, or performance details of any live trading system.
  If a raw report references one, generalise it to "the desk's live system" with no numbers.
- Do not invent, round, or "improve" any statistic. Every number in an entry must appear
  in its raw report. If a number is ambiguous, quote the report's own wording.
- Strip local filesystem paths and machine-specific references (e.g. `~/workspace/...`,
  internal hostnames) from all published pages; replace with the repo-relative raw link.
- No credentials, tokens, account identifiers, or personal data anywhere.
- English for all new pages. Do not translate or edit the files inside `raw_reports/`.
- Tone: factual, dry, no marketing. The numbers carry it.

## Completion report
When the PR is open, summarise: files created, entries completed (count), any source
ambiguities found, and confirmation that the hard constraints were checked.
