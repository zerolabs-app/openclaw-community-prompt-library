# Wholesale Product Hunter

Research wholesale, bulk, and resale product options for a small boutique store.

## User Inputs

- Product Category: Beauty / Makeup
- Product Type: Lip gloss / lip oil / small makeup items
- Store Type: Small boutique
- Target Customer: Women, teens, gift buyers
- Maximum Unit Cost: $5
- Target Retail Price: $12–$20
- Minimum Order Quantity Preference: Low MOQ preferred
- Maximum Initial Order Budget: $300
- Preferred Brands: Any
- Brands To Avoid: NA
- Required Features: Wholesale pricing, resale-friendly, available online, low MOQ
- Preferred Features: Trendy packaging, giftable, private-label option, cruelty-free when available
- Intended Use: Buy inventory for resale
- Shipping Region: United States

## Research Goals

- Find wholesale products suitable for boutique resale.
- Compare unit cost, MOQ, retail potential, and supplier quality.
- Identify best starter inventory options.
- Avoid products with poor resale margin or unclear supplier terms.

## Search Sources

Search publicly accessible wholesale and supplier information from:

- Wholesale marketplaces
- Brand wholesale pages
- Faire
- Alibaba / AliExpress wholesale
- Tundra
- FashionGo
- Abound
- Faire alternatives
- Manufacturer websites
- Private-label suppliers
- Boutique supplier directories
- Public reviews and seller feedback

## Search Rules

- Search first.
- Gather evidence before analysis.
- Prefer suppliers with clear wholesale pricing.
- Prefer low MOQ suppliers.
- Prefer products with strong resale margin.
- Verify prices, MOQ, shipping region, and resale terms when practical.
- Do not invent products.
- Do not invent wholesale prices.
- Do not invent MOQ.
- Do not invent supplier claims.

## Required Supplier Information

For each option provide:

- Supplier name
- Product name
- Product category
- Wholesale unit cost
- MOQ
- Estimated initial order cost
- Suggested retail price
- Estimated gross margin
- Shipping region
- Resale / wholesale terms
- Product link
- Notes explaining why it may work for a boutique

## Ranking Rules

Rank products by:

1. Low initial order risk
2. Good resale margin
3. Low MOQ
4. Attractive packaging
5. Trend fit
6. Supplier credibility
7. Shipping practicality

## Output

Generate:

- Top wholesale product options
- Best low-risk starter buy
- Best margin product
- Best giftable product
- Best private-label option
- Products to avoid
- Supplier comparison
- Final buying recommendation

## Result Summary Line Rule

Wholesale pricing, MOQ terms, and supplier stock change frequently.

The one-line Summary field at the top of the result file (used as the email subject/preview line) must not state a price as current fact.

The Summary field must include:

- "lead" or "as of" framing, not a bare price claim
- the time the item was observed (from the run time already recorded)
- the top supplier source, so the user can verify in one tap

Example of a correct Summary line:

Summary: Best lead as of 2026-08-05 15:59 - ceramic mug set $2.10/unit MOQ 500 (Alibaba supplier) - verify current price and MOQ before ordering.

Example of an incorrect Summary line:

Summary: Best product is a ceramic mug set at $2.10/unit.

Apply this same observed-at-time and source-in-summary treatment to the Market Summary section below, not only the result header.

## Market Summary

Summarize:

- pricing trends
- typical MOQ ranges
- common supplier terms
- resale margin expectations
- packaging trends
- risk factors for boutique buyers

## No Results Rule

If no qualifying wholesale products are found:

- Report the limitation.
- Provide evidence of the search performed.
- Explain the limiting factors.
- Provide closest alternatives.
- Do not invent products, prices, MOQ, reviews, or supplier terms.


Output Formatting Rule

- Do not use a standalone line of three or more dashes (---) anywhere in the report, including between individual entries.
- Separate multiple entries using a blank line followed by a heading (e.g. "### 2)") instead of a dash divider.
- This applies to the entire report.
