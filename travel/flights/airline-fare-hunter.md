# Airline Fare Hunter

Find the cheapest round-trip airfare matching the criteria specified by the user.

User Inputs

- Departure City or Airport: [USER INPUT]
- Destination City or Airport: [USER INPUT]
- Departure Date: [USER INPUT]
- Return Date: [USER INPUT]
- Number of Adult Passengers: [USER INPUT]
- Number of Child Passengers: [USER INPUT]
- Number of Infant Passengers: [USER INPUT]
- Preferred Cabin Class: [USER INPUT]
- Nonstop Required: [YES / NO]
- Maximum Stops: [USER INPUT]
- Flexible Dates Allowed: [YES / NO]
- Flexible Date Range: [USER INPUT]
- Nearby Departure Airports Allowed: [YES / NO]
- Nearby Destination Airports Allowed: [YES / NO]
- Maximum Nearby Airport Distance: [USER INPUT]
- Checked Bags Needed: [USER INPUT]
- Carry-On Bags Needed: [USER INPUT]
- Seat Selection Required: [YES / NO]
- Preferred Departure Time: [USER INPUT]
- Preferred Arrival Time: [USER INPUT]
- Maximum Total Travel Time: [USER INPUT]
- Maximum Layover Time: [USER INPUT]
- Preferred Airlines: [USER INPUT]
- Airlines to Avoid: [USER INPUT]
- Maximum Total Budget: [USER INPUT]

Search Sources

Search public fare information from:

- Major airlines
- Public airfare search engines
- Public fare aggregators
- Airport route information when useful
- Any publicly accessible airfare sources

Search Control

- Search major airlines and one major public fare source first.
- Include nearby airports only if allowed by the user.
- Do not expand to every nearby airport by default.
- Stop once 5-10 strong options are found.
- Prefer completing the report over exhaustive searching.
- Prefer nonstop flights when available unless connections are allowed and offer substantial savings.
- Only apply a filter when the user provides a value.

Blocked Source Fallback Rule

If a fare source:

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
- Do not repeatedly retry a blocked or unusable source during the same run.

Nearby Airport Rule

If nearby airports are allowed:

- Check the primary departure and destination airports first.
- Check nearby airports only after primary-airport options are collected.
- Clearly label alternate-airport results.
- Explain whether alternate airports reduce total cost enough to justify using them.

If nearby airports are not allowed:

- Do not include alternate airports.
- Do not rank alternate-airport options.

Flexible Date Rule

If flexible dates are allowed:

- Check the requested dates first.
- Check nearby dates only within the requested flexible date range.
- Clearly label alternate-date results.
- Explain whether alternate dates reduce total cost enough to justify changing dates.

If flexible dates are not allowed:

- Do not include alternate-date options.
- Do not rank alternate-date options.

Required Flight Information

For each flight option provide:

- Airline
- Departure airport
- Arrival airport
- Total trip price
- Price per passenger
- Travel dates
- Flight times
- Number of stops
- Total travel time
- Layover cities when available
- Layover duration when available
- Cabin class
- Lowest available fare for each relevant cabin class
- Baggage restrictions or major fare limitations if known
- Fare source
- Fare link

Ranking Rules

- Rank results from lowest total price to highest total price.
- Do not rank options that violate hard user requirements.
- If no exact matches exist, rank the closest alternatives.
- Explain why each alternative may still be worth considering.

Result Summary Line Rule

Airfare is volatile and can change between when it is observed and when the user reads the report.

The one-line Summary field at the top of the result file (used as the email subject/preview line) must not state a price as current fact.

The Summary field must include:

- the word "lead" or "as of" framing, not a bare price claim
- the time the fare was observed (from the run time already recorded)
- the top fare source, so the user can verify in one tap

Example of a correct Summary line:

Summary: Best lead as of 2026-08-05 15:59 - United SEA-IAH $343/pax (Google Flights) - verify before booking.

Example of an incorrect Summary line:

Summary: Cheapest fare is $343 per passenger on United.

Apply this same observed-at-time and source-in-summary treatment to the Final Fare Summary section below, not only the result header.

Final Fare Summary

Identify:

- Cheapest Overall Option
- Cheapest Nonstop Option
- Best Value Option
- Best Premium Cabin Option
- Best Schedule Option
- Best Alternate Airport Option if applicable
- Booking Recommendation

Market Summary

Summarize:

- significant price differences
- route availability
- nonstop availability
- alternate airport savings if applicable
- alternate date savings if applicable
- whether booking now or waiting appears better

No Results Rule

If no qualifying fare options are found:

- Report that no qualifying fare options were found.
- Provide evidence of the search performed.
- Explain the limiting factors.
- Do not invent prices.
- Do not invent flights.
- Do not substitute different airports or dates unless the user allowed it.



Final Verification Step

Immediately before finalizing the result, re-check the top fare option's fare link one more time.

Confirm whether the price and availability still matches what was found earlier in the run.

- If it matches, note "confirmed at [time]" next to the top result.
- If it has changed or the fare is no longer available, note "changed since first seen - verify before acting" and update the figure if a new one is visible.
- Only re-check the single top-ranked result this way. Do not re-check every option - that defeats the purpose of a lightweight verification step.
- If the re-check source is blocked, rate-limited, or fails to load, note that the re-check could not be completed rather than assuming the original figure still holds.

Output Formatting Rule

- Do not use a standalone line of three or more dashes (---) anywhere in the report, including between individual entries.
- Separate multiple entries using a blank line followed by a heading (e.g. "### 2)") instead of a dash divider.
- This applies to the entire report.
