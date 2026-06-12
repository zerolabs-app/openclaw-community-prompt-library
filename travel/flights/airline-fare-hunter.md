# Airline Fare Hunter

Find the cheapest round-trip airfare for the number of passengers specified by the user.

User Inputs:

* Departure City or Airport: [USER INPUT]
* Destination City or Airport: [USER INPUT]
* Departure Date: [USER INPUT]
* Return Date: [USER INPUT]
* Number of Adult Passengers: [USER INPUT]
* Number of Child Passengers (if any): [USER INPUT]

Requirements:

* Round-trip tickets
* Search major airlines and one major public fare source first.
* Include nearby airports only if the primary-airport search completes successfully and time remains.
* Do not expand to every nearby airport by default.
* Stop once 5-10 strong options are found.
* Prefer completing the report over exhaustive searching.
* Prefer nonstop flights when available, but include the best connecting options if they offer substantial savings

For each flight option found, provide:

* Airline
* Departure airport
* Arrival airport
* Total trip price
* Price per passenger
* Travel dates
* Flight times
* Number of stops
* Total travel time
* Seat classes available (Basic Economy, Economy, Premium Economy, Business, First Class, etc.)
* Lowest available fare for each seat class
* Baggage restrictions or major fare limitations if known

Rank results from lowest total price to highest total price.

Search Control:

- If a fare source is blocked, login-gated, captcha-gated, rate-limited, or unusable, record the limitation once and move to the next source.
- Do not repeatedly retry a blocked or unusable source during the same run.
- Stop broad searching once 5-10 strong options are found or once major airlines plus one public fare source have been checked.
- Prefer a complete, well-supported report over exhaustive fare hunting.

At the end, provide:

* Cheapest overall option
* Cheapest nonstop option
* Best value option
* Best premium cabin option
* Any significant price trends
* Recommendations for booking immediately versus waiting
* Any alternate airports that may reduce overall cost
