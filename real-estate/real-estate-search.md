# Real Estate Hunter

Find real estate matching the criteria specified by the user.

User Inputs

- Property Type: [USER INPUT]
- Location: [USER INPUT]
- Maximum Distance: [USER INPUT]
- Maximum Budget: [USER INPUT]
- Minimum Bedrooms: [USER INPUT]
- Minimum Bathrooms: [USER INPUT]
- Minimum Square Footage: [USER INPUT]
- Minimum Lot Size: [USER INPUT]
- Minimum Acres: [USER INPUT]
- Maximum HOA Fee: [USER INPUT]
- Year Built Range: [USER INPUT]
- Waterfront Required: [YES / NO]
- Water View Required: [YES / NO]
- Pool Required: [YES / NO]
- Garage Spaces Required: [USER INPUT]
- RV Parking Required: [YES / NO]
- Property Condition: [USER INPUT]
- Required Features: [USER INPUT]
- Preferred Features: [USER INPUT]

Search Sources

Search active listings from:

- Realtor websites
- Brokerage websites
- MLS-backed listing pages
- Real estate listing aggregators
- Search-engine indexed property listings
- County property resources when applicable
- Any publicly accessible real estate listing sources

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

- Brokerage inventory
- MLS-backed listing pages
- Realtor inventory
- County property resources
- Search-engine indexed listing pages

Geographic Scope Rule

The requested location is mandatory.

For real estate searches:

- Search only inside the requested location.
- Do not substitute different cities.
- Do not substitute different counties.
- Do not substitute different lakes.
- Do not substitute different regions.
- Do not expand to other states.
- Do not expand nationwide.

If a city is specified:

- Remain inside the city when possible.
- Expansion is limited to the requested Maximum Distance.
- Do not expand beyond the requested Maximum Distance.

If a county is specified:

- Remain inside the county.

Properties outside the permitted search area must not be:

- Ranked.
- Recommended.
- Selected as purchase candidates.

Property Type Rule

The requested property type is mandatory.

Do not substitute different property types unless explicitly requested.

If searching for:

- Single-family homes
- Multi-family homes
- Condominiums
- Townhomes
- Manufactured homes
- Land
- Acreage
- Waterfront lots
- RV lots
- Commercial property

remain within the requested property type.

If no qualifying properties are found:

- Report that no qualifying properties were found.
- Do not substitute a different property type.

Listing Source Priority

Prefer:

- Original listing source
- Brokerage listing
- MLS-backed listing
- Verified property source

Avoid duplicate listings when possible.

Required Listing Information

For each qualifying property provide:

- Property address
- Asking price
- Property type
- Bedrooms
- Bathrooms
- Building size
- Lot size
- Acreage when available
- Year built
- HOA fee when available
- Listing source
- Listing link
- Key features
- Notes explaining why the property may be a good purchase

Ranking Rules

- Rank all qualifying properties from most promising to least promising.
- If no strong matches exist, rank the closest alternatives.
- Explain why each alternative may still be worth considering.

Final Buyer Summary

Identify:

- Best Overall Value
- Best Budget Option
- Best Premium Option
- Best Investment Opportunity
- Best Long-Term Ownership Candidate
- Properties Worth Contacting First

Market Summary

Summarize:

- Pricing trends observed
- Inventory availability
- Common property characteristics
- Notable findings discovered during the search

No Results Rule

If no qualifying in-scope properties exist:

- Report that no qualifying properties were found.
- Provide evidence of the search performed.
- Explain the limiting factors.
- Do not substitute different locations.
- Do not substitute different property types.
- Do not fill the report with out-of-scope properties.
