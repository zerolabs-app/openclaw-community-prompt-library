# Motorcycle Hunter

Purpose

Find motorcycles matching the criteria specified by the user.

User Inputs

- Motorcycle Make: [USER INPUT]
- Motorcycle Model: [USER INPUT]
- Motorcycle Years or Year Range: [USER INPUT]
- Maximum Distance from ZIP Code: [USER INPUT]
- ZIP Code: [USER INPUT]
- Maximum Budget: [USER INPUT]
- Preferred Engine Size or Engine Type: [USER INPUT]
- Required Features, Trim, or Options: [USER INPUT]
- Preferred Condition: [USER INPUT]

Search Sources

- Classified sites
- Motorcycle dealer inventory
- Powersports dealer inventory
- Auction listings
- Marketplace-style public listings
- Motorcycle enthusiast forums
- Any publicly accessible motorcycle sale sources

Blocked Source Fallback Rule

If a source:

- blocks automated access
- requires sign-in
- fails to render
- returns unusable pages

then:

- Record the blocked source.
- Record the reason.
- Continue searching.
- Do not stop searching because a source is unavailable.

Required fallback sources include:

- Direct motorcycle dealer inventory
- Direct powersports dealer inventory
- Regional dealer inventory
- Motorcycle forums and owner groups
- Classified aggregators
- Auction sites
- Search-engine indexed listing pages

Search Expansion Rules

If no exact matches are found:

- Expand search radius by 25-mile increments up to 200 miles.
- Expand model years by plus or minus 2 years if needed.
- Include closest matching listings.
- Explain why each alternative may still be worth considering.

Returning qualified alternatives is preferred over returning no listings.

Priorities

- Running and riding motorcycles
- Clean title motorcycles when title status is available
- Motorcycles within budget
- Motorcycles matching preferred engine size, trim, options, and condition requirements
- Well-maintained examples
- Listings with clear descriptions and photos
- Listings with mileage, title status, maintenance history, and recent service information

Required Listing Information

For each promising motorcycle found provide:

- Asking price
- Location
- Year
- Make
- Model
- Engine size or engine type
- Mileage
- Title status if known
- Running or riding status
- Overall condition
- Listing link
- Purchase notes

Ranking Rules

- Rank all motorcycles from most promising to least promising.
- If no strong matches exist, rank the closest alternatives.
- Explain why each alternative may still be worth considering.


Result Summary Line Rule

Listings can sell, get pending offers, or change price at any time.

The one-line Summary field at the top of the result file (used as the email subject/preview line) must not state a price or figure as current fact.

The Summary field must include:

- "lead" or "as of" framing, not a bare price/figure claim
- the time the item was observed (from the run time already recorded)
- the top source, so the user can verify in one tap

Example of a correct Summary line:

Summary: Best lead as of 2026-08-05 15:59 - 2015 Kawasaki KLR650 $4,200 (Craigslist) - verify it's still listed before contacting seller.

Example of an incorrect Summary line:

Summary: Best option is a 2015 Kawasaki KLR650 for $4,200.

Apply this same observed-at-time and source-in-summary treatment to the Final Buyer Summary section below, not only the result header.

Final Buyer Summary

Identify:

- Best Overall Value
- Best Condition
- Best Budget Option
- Best Long-Term Ownership Candidate
- Listings Worth Contacting First

* Best overall purchase opportunity
* Best value option
* Lowest-priced running/riding option
* Best low-mileage option
* Any notable trends in pricing or availability



Final Verification Step

Immediately before finalizing the result, re-check the top listing's source link one more time.

Confirm whether the listing is still active and the price still matches what was found earlier in the run.

- If it matches, note "confirmed at [time]" next to the top result.
- If it has changed or the listing is no longer available, note "changed since first seen - verify before acting" and update the figure if a new one is visible.
- Only re-check the single top-ranked result this way. Do not re-check every option - that defeats the purpose of a lightweight verification step.
- If the re-check source is blocked, rate-limited, or fails to load, note that the re-check could not be completed rather than assuming the original figure still holds.

Output Formatting Rule

- Do not use a standalone line of three or more dashes (---) anywhere in the report, including between individual entries.
- Separate multiple entries using a blank line followed by a heading (e.g. "### 2)") instead of a dash divider.
- This applies to the entire report.
