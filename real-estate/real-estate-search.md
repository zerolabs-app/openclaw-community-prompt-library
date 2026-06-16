# OpenClaw Real Estate Search

Purpose:

Find real estate matching the requested criteria.

Search first.

Gather evidence before analysis.

---

SEARCH RULES

- Search before analysis.
- Follow Search-First rules.
- Use the configured search provider.
- Prefer active listings.
- Prefer original listing sources.
- Prefer verified property information.

Do not invent:

- listings
- prices
- addresses
- acreage
- property details

---

GEOGRAPHIC SCOPE RULE

The requested Location is mandatory.

The requested search area is a hard boundary.

For land searches:

- search only inside the requested location
- do not expand to other states
- do not expand nationwide
- do not substitute different lakes
- do not substitute different counties
- do not substitute different cities
- do not substitute different regions

If a city is specified:

- remain inside the city when possible
- expansion is limited to a maximum 25-mile radius

If a county is specified:

- remain inside the county

If a lake is specified:

- remain within the requested lake area

Properties outside the permitted search area must not be:

- ranked
- recommended
- selected as purchase candidates

If no qualifying properties are found:

- report that no qualifying in-scope properties were found
- explain which requirements limited results

Do not fill the report with out-of-scope properties.

---

SOURCE PRIORITY RULE

Prioritize:

- Realtor.com
- Land.com
- LandWatch
- Lands of America
- Zillow when accessible
- Redfin when accessible
- local broker websites
- county property databases
- search-engine indexed listing pages

Delay:

- Facebook Marketplace
- login-required websites
- anti-bot protected websites
- JavaScript-only listing pages
- sources that already failed during the current run

If a source is blocked:

- record the source
- record the reason
- continue immediately

Do not repeatedly retry blocked sources.

Candidate listings are higher priority than source coverage.

---

TIMEBOX RULE

Within the first five minutes:

- identify working sources
- identify blocked sources
- collect candidate listings

If timeout risk exists:

- save findings immediately
- create canonical artifacts immediately
- preserve collected evidence
- create a partial buyer guide

A partial result is preferred over a timeout without artifacts.

---

SEARCH REQUEST

Property Type:

[PROPERTY TYPE]

Location:

[LOCATION]

Budget:

[BUDGET]

Requirements:

[REQUIREMENTS]

---

LISTING DATA

For each qualifying property provide:

- Property address
- Asking price
- Property type
- Lot size
- Building size when applicable
- Bedrooms and bathrooms when applicable
- Listing source
- Listing link
- Key features
- Potential concerns

---

ANALYSIS

Identify:

- Best overall value
- Best budget option
- Best premium option
- Best investment opportunity
- Potential concerns
- Market observations
- Properties that appear overpriced

---

OUTPUT RULES

Rank qualifying properties from most promising to least promising.

Generate:

- Top recommendations
- Strengths and weaknesses
- Potential risks
- Recommended next actions
- Best overall purchase candidate

If no qualifying in-scope properties exist:

- report no qualifying properties found
- provide evidence of the search performed
- explain the limiting factors
