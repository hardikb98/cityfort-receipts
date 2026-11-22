# Cityfort Receipts

Where each $100 (US) or ₹100 (India) that came into a listed company went, from its latest annual filing, for 475 companies.
Maintained by Hardik Bhandare (Pune, India), creator of [Cityfort](https://cityfort.co). Licence: CC BY 4.0.

## Files
- `receipts-us.csv`: 300 US-listed companies, latest fiscal year (SEC Form 10-K or 20-F). Basis: per $100 of revenue and other income.
- `receipts-in.csv`: 175 Indian companies, latest financial year (annual reports filed on NSE/BSE). Basis: per ₹100 of total income (revenue + other income).
- `CHANGELOG.md`: what changed in each snapshot.

## Columns (one row per receipt line)
`market` (US/IN) · `slug` (page id) · `company` · `ticker` (US ticker or NSE symbol) · `sector` · `period` (FY2026, FY26, CY25) · `basis` (what the 100 is) · `line_order` · `line_label` · `line_kind` (cost, tax, profit, other) · `per_100` (1 decimal; a company's lines add to exactly 100.0) · `source` (filing title) · `source_url` (sec.gov, nseindia.com, bseindia.com or the company's filing) · `page_url` · `last_updated` (YYYY-MM-DD)

## Method
Each line = the amount in the filing ÷ (revenue + other income) × 100. Lines are rounded to 1 decimal so they add to exactly 100.0 (largest remainder). A negative profit line is a loss: the company spent more than came in. Figures are as filed (US GAAP, IFRS or Ind AS, as the company reports); per-100 values are a Cityfort calculation. Banks and insurers use receipt lines that fit their accounts (interest earned and paid, premiums and claims).

Each Cityfort page is drafted with AI tools from the company's own filings. A script checks structure and sources, a separate AI review traces every number to its filing, and Hardik Bhandare reads, corrects and approves the page before it is published. Corrections are logged at https://cityfort.co/corrections and https://cityfort.in/corrections.

## Updates
A new snapshot after each results season; see `CHANGELOG.md`.

## Licence and credit
CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). Credit: "Data: Cityfort" with a link to the company page on cityfort.co or cityfort.in.

For learning only. Cityfort is not a registered investment adviser or broker-dealer, is not a SEBI-registered adviser, and does not recommend buying or selling any security. No prices are included.

## Live data
Read-only MCP server for AI assistants: https://cityfort.co/mcp and https://cityfort.in/mcp. Details: https://cityfort.co/developers.
