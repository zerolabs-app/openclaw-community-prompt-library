# Real Treasury Yield Tracker

Find the current real (inflation-adjusted) Treasury yields matching the criteria specified by the user.

User Inputs

- Maturities to Check: 2-Year, 10-Year, 30-Year
- As-Of Date: Most Recent Available
- Compare to Prior Period: YES
- Comparison Period: 1 Week

Data Accuracy Rule

Real yield figures inform real financial decisions. This rule overrides convenience.

- Every yield figure must include its source and as-of date.
- Do not calculate or estimate a real yield by subtracting an assumed inflation rate from a nominal yield.
- Only report a real yield figure that a source directly publishes.
- If a source publishes real yields with a reporting lag, state the lag clearly.
- If real yield data is unavailable for a requested maturity, report that plainly.
- Do not average figures from disagreeing sources.
- If sources disagree, report each figure with its source rather than picking one.

Search Sources

Search public yield data from:

- U.S. Treasury / TreasuryDirect real yield curve data
- FRED (Federal Reserve Economic Data) inflation-indexed Treasury series
- Financial news bond-market pages
- X
- Any publicly accessible Treasury yield data sources

Search Control

- Check Treasury.gov and FRED first; these are primary, official sources.
- Use financial news pages and X for corroboration, not as the primary figure.
- Stop once each requested maturity has a sourced, dated figure.

Blocked Source Fallback Rule

If a source:

- blocks automated access
- requires sign-in
- is captcha-gated
- is rate-limited
- fails to render
- returns unusable pages

then:

- Record the blocked source.
- Record the reason.
- Move to the next source.
- If all named sources are blocked, expand to search-engine indexed pages before reporting no data.
- Do not repeatedly retry a blocked or unusable source during the same run.

Required Yield Information

For each maturity checked provide:

- Maturity
- Real yield
- Nominal yield for the same maturity, when available
- Implied breakeven inflation rate, when both figures are available and directly stated by a source
- As-of date
- Source
- Source link

Comparison Rules

- Compare the requested maturities to describe the shape of the real yield curve (normal, flat, or inverted).
- If a comparison period was requested, report the change since that period for each maturity.
- Do not describe a trend without a sourced prior-period figure to compare against.


Result Summary Line Rule

Yields move throughout the trading day.

The one-line Summary field at the top of the result file (used as the email subject/preview line) must not state a price or figure as current fact.

The Summary field must include:

- "lead" or "as of" framing, not a bare price/figure claim
- the time the item was observed (from the run time already recorded)
- the top source, so the user can verify in one tap

Example of a correct Summary line:

Summary: Best lead as of 2026-08-05 15:59 - 10Y yield 4.28% (Treasury.gov) - verify before acting.

Example of an incorrect Summary line:

Summary: 10-year yield is 4.28%.

Apply this same observed-at-time and source-in-summary treatment to the Final Yield Summary section below, not only the result header.

Final Yield Summary

Identify:

- Current Real Yield Snapshot for each requested maturity
- Real Yield Curve Shape
- Largest Change Since Comparison Period
- Notable Divergence Between Real and Nominal Yields

Market Summary

Summarize:

- what the current real yield levels may suggest about inflation expectations
- any notable recent shift in the real yield curve
- relevant, recently published context from official sources, if available

This summary is informational only and is not financial or investment advice.

No Results Rule

If no qualifying real yield data is found for a requested maturity:

- Report that no qualifying data was found.
- Provide evidence of the search performed.
- Explain the limiting factors.
- Do not invent a yield figure.
- Do not estimate a yield figure from unrelated data.



Final Verification Step

Immediately before finalizing the result, re-check the top yield figure's source link one more time.

Confirm whether the yield value still matches what was found earlier in the run.

- If it matches, note "confirmed at [time]" next to the top result.
- If it has changed or the figure is no longer available, note "changed since first seen - verify before acting" and update the figure if a new one is visible.
- Only re-check the single top-ranked result this way. Do not re-check every option - that defeats the purpose of a lightweight verification step.
- If the re-check source is blocked, rate-limited, or fails to load, note that the re-check could not be completed rather than assuming the original figure still holds.

Output Formatting Rule

- Do not use a standalone line of three or more dashes (---) anywhere in the report, including between individual entries.
- Separate multiple entries using a blank line followed by a heading (e.g. "### 2)") instead of a dash divider.
- This applies to the entire report.
