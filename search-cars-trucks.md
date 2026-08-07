# Vehicle Hunter

Purpose

Find vehicles matching the criteria specified by the user.

User Inputs

- Vehicle Make: [USER INPUT]
- Vehicle Model: [USER INPUT]
- Vehicle Years or Year Range: [USER INPUT]
- Maximum Distance from ZIP Code: [USER INPUT]
- ZIP Code: [USER INPUT]
- Maximum Budget: [USER INPUT]
- Preferred Engine(s): [USER INPUT]
- Required Features or Options: [USER INPUT]
- Preferred Condition: [USER INPUT]

Search Sources

Search publicly accessible vehicle listings from:

- Classified sites
- Collector vehicle sites
- Auction listings
- Dealer inventory
- Marketplace-style public listings
- Vehicle enthusiast forums
- Search-engine indexed vehicle listings
- Any publicly accessible vehicle sale sources

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

Search Expansion Rules

If no exact matches are found:

- Expand search radius by 25-mile increments up to 200 miles.
- Expand model years by plus or minus 2 years if needed.
- Include closest matching vehicles.
- Explain why each alternative may still be worth considering.

Returning qualified alternatives is preferred over returning no results.

Priorities

- Running and driving vehicles
- Vehicles within budget
- Vehicles matching preferred engine requirements
- Vehicles matching required options and features
- Well-maintained examples
- Listings with complete descriptions and photos
- Listings with mileage and condition information

Required Listing Information

For each promising vehicle found provide:

- Asking price
- Location
- Year
- Make
- Model
- Engine
- Transmission if known
- Mileage if known
- Running or driving status
- Overall condition
- Listing source
- Listing link
- Notes explaining why the vehicle may be a good purchase

Ranking Rules

- Rank all vehicles from most promising to least promising.
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

Summary: Best lead as of 2026-08-05 15:59 - 2019 Honda Civic $14,500 (AutoTrader) - verify it's still listed before contacting seller.

Example of an incorrect Summary line:

Summary: Best option is a 2019 Honda Civic for $14,500.

Apply this same observed-at-time and source-in-summary treatment to the Final Buyer Summary section below, not only the result header.

Final Buyer Summary

Identify:

- Best Overall Purchase Opportunity
- Best Value Option
- Lowest-Priced Running and Driving Option
- Best Long-Term Ownership Candidate
- Listings Worth Contacting First

Market Summary

Summarize:

- pricing trends observed
- availability within the search area
- common vehicle conditions observed
- notable findings discovered during the search
* Best overall purchase opportunity
* Best value option
* Lowest-priced running/driving option
* Any notable trends in pricing or availability


Output Formatting Rule

- Do not use a standalone line of three or more dashes (---) anywhere in the report, including between individual entries.
- Separate multiple entries using a blank line followed by a heading (e.g. "### 2)") instead of a dash divider.
- This applies to the entire report.
