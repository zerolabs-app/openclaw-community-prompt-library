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
