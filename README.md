This repository contains processed SEC EDGAR filings for senior housing REITs, specifically for the following tickers: 

- AHR (American Healthcare REIT, Inc.)
- DHC (Diversified Healthcare Trust)
- VTR (Ventas, Inc.)
- WELL (Welltower Inc.)

The filings have been extracted and organized for easier access and analysis.

To navigate the repository, follow this structure: `/<TICKER>/<FORM_TYPE>/<ACCESSION_NUMBER>`. For example, to find the 10-K for VTR with accession number `0000740260-25-000052`, you would navigate to `/VTR/10-K/0000740260-25-000052/`. 

Within each accession number directory, you will find the following processed files:
- `clean-text-for-llm.txt`: This file contains the clean, narrative text of the filing, with HTML, XBRL, and other markup removed. It is suitable for natural language processing and analysis.
- `xbrl-data-markdown.md`: This file contains structured financial data extracted from the filing's inline XBRL tags, presented in markdown tables for easy readability.