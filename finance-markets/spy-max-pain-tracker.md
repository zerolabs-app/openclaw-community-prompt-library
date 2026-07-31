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
