# Quant graveyard

**24 hypotheses tested, 0 survivors**

This is the public research graveyard of a nightly quantitative research desk. Hypotheses are registered with kill criteria before testing. The archive records the lines that died, the evidence behind each decision, and what was not built.

Some reports reject a predictive hypothesis. Others document a descriptive relationship or a data-feasible market without establishing a strategy. A positive descriptive result is not a survivor. The index preserves those distinctions rather than relabeling every finding as statistically absent.

## Kill rules

A hypothesis is registered before it is tested, with its kill criteria committed first. It survives only if all of the following hold:

- Full available history, with no cherry-picked windows.
- Trading costs deducted: fees, and spread/slippage where applicable.
- Execution at the next bar's open, never the signal bar's close.
- The effect holds out-of-sample and across sub-periods, including weekday/weekend, per-year and per-instrument splits where the report uses them.
- For strategies, it must materially beat buy-and-hold, not merely be positive.
- Multiple-comparison discipline where the report applies it, such as Bonferroni thresholds.

Even a survivor is not traded. It must first pass a 90-day paper-forward trial with at least 30 closed trades, profit factor ≥ 1.30, and maximum drawdown no worse than −20% before any live discussion. Promotion decisions belong to the human owner alone.

These are promotion requirements, not a claim that every descriptive report conducted a strategy backtest. Entries identify missing numerical kill thresholds, incomplete execution tests and other limitations rather than inventing them.

## How to read an entry

Start with [GRAVEYARD.md](GRAVEYARD.md). Each entry has metadata and five sections:

- **Pre-registered question and kill criteria:** what was asked and the source's stated rejection or promotion conditions.
- **Data scope:** instruments, venue, bar size, sample size and period.
- **Method:** definitions, comparisons and checks, including timing and dependence limitations.
- **Decisive results:** the evidence that determines the verdict, not every source table.
- **Verdict and what was not built:** the source conclusion, whether the line closed, and the absence of a strategy or survivor promotion.

T8 additionally has a **Live feasibility follow-up** before its verdict. Its quote-feasibility result does not establish strategy profitability.

Numbers are copied verbatim from the linked sources, without new rounding, unit conversion or derived calculations. Source ambiguities are retained or explicitly qualified. `raw_reports/` is the untouched Traditional-Chinese provenance layer; each entry links its source report, or both reports for T8. Descriptive proportions are not strategy win rates, and gross forward returns are not cost-adjusted strategy performance.

Q1 and Q3 are withheld live-system health checks. Their details are not published; they are not part of the public tested-hypothesis count. References to the desk's live system contain no parameters or performance details.

## Repository layout

- `GRAVEYARD.md` — ordered research index, including withheld placeholders.
- `entries/` — English research summaries, one page per public research item.
- `raw_reports/` — original Traditional-Chinese reports, unchanged.
- `SPEC.md` — publication contract and research-promotion requirements.
