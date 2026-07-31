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
