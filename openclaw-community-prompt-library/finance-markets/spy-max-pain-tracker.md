# SPY Max Pain Tracker

Find today's max pain price level for SPY options matching the criteria specified by the user.

User Inputs

- Ticker: SPY
- Expiration Date: Nearest Available
- As-Of Time: Most Recent Available

Data Accuracy Rule

Max pain is a calculated value, not a published fact, and different sources can produce different figures depending on methodology and timing. This rule overrides convenience.

- Every max pain figure must include its source and calculation timestamp.
- If a source states its methodology (which expirations or strikes were included), report it.
- Do not calculate a max pain figure independently from raw options-chain data.
- Do not average max pain figures from disagreeing sources.
- If sources disagree, report each figure with its source rather than picking one.

Search Sources

Search public options data from:

- Dedicated max pain calculation sites
- CBOE public options data
- Financial news options-market pages
- X
- Any publicly accessible options data sources

Search Control

- Check dedicated max pain calculation sites first.
- Use CBOE data to verify or cross-check when available.
- Use X for corroboration, not as the primary figure.
- Stop once a sourced, timestamped max pain figure is found for the requested expiration.

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

Required Max Pain Information

For each expiration checked provide:

- Ticker
- Expiration date
- Max pain price
- Current price at time of check
- Distance between current price and max pain price
- Calculation methodology, if stated by the source
- Calculation or as-of timestamp
- Source
- Source link

Comparison Rules

- If more than one source provides a max pain figure for the same expiration, report each one with its source.
- Note the range between the highest and lowest reported figures rather than resolving it to a single number.
- Do not present one source's figure as more correct than another's without a stated reason.


Result Summary Line Rule

Max pain and options pricing shift throughout the trading day, and can move sharply near expiration.

The one-line Summary field at the top of the result file (used as the email subject/preview line) must not state a price or figure as current fact.

The Summary field must include:

- "lead" or "as of" framing, not a bare price/figure claim
- the time the item was observed (from the run time already recorded)
- the top source, so the user can verify in one tap

Example of a correct Summary line:

Summary: Best lead as of 2026-08-05 15:59 - SPY max pain $560 for 08/08 expiry (CBOE) - verify before acting.

Example of an incorrect Summary line:

Summary: SPY max pain is $560.

Apply this same observed-at-time and source-in-summary treatment to the Final Summary section below, not only the result header.

Final Summary

Identify:

- Reported Max Pain Level(s)
- Current Price vs Max Pain
- Range Across Sources, if applicable
- Notable Open Interest Concentration, if reported by a source

Market Summary

Summarize:

- what max pain theory generally suggests about price behavior into expiration
- any notable difference between current price and the reported max pain level
- relevant context from the sources checked

This summary is informational only, reflects one options-market theory among several, and is not financial or investment advice.

No Results Rule

If no qualifying max pain data is found:

- Report that no qualifying data was found.
- Provide evidence of the search performed.
- Explain the limiting factors.
- Do not invent a max pain figure.
- Do not calculate one independently unless the user explicitly requests a manual calculation from raw data.



Final Verification Step

Immediately before finalizing the result, re-check the top max pain figure's source link one more time.

Confirm whether the figure still matches what was found earlier in the run.

- If it matches, note "confirmed at [time]" next to the top result.
- If it has changed or the figure is no longer available, note "changed since first seen - verify before acting" and update the figure if a new one is visible.
- Only re-check the single top-ranked result this way. Do not re-check every option - that defeats the purpose of a lightweight verification step.
- If the re-check source is blocked, rate-limited, or fails to load, note that the re-check could not be completed rather than assuming the original figure still holds.

Output Formatting Rule

- Do not use a standalone line of three or more dashes (---) anywhere in the report, including between individual entries.
- Separate multiple entries using a blank line followed by a heading (e.g. "### 2)") instead of a dash divider.
- This applies to the entire report.
