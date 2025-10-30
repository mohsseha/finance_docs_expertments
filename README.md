# Processed SEC EDGAR Filings for Senior Housing REITs

This repository contains processed SEC EDGAR filings for senior housing REITs, making them easier to access and analyze for natural language processing and financial analysis tasks.

## FAQ

**What is this repository?**

This repository provides cleaned and structured data from SEC EDGAR filings for a curated list of senior housing REITs. The goal is to provide LLM-ready text and machine-readable financial data.

**What companies are included?**

- **AHR**: American Healthcare REIT, Inc.
- **DHC**: Diversified Healthcare Trust
- **VTR**: Ventas, Inc.
- **WELL**: Welltower Inc.

**What is the date range of the filings?**

The filings in this repository cover the period from **2024 to 2025**.

**How is the repository structured?**

Filings are organized by ticker, form type, and accession number:

```
/<TICKER>/<FORM_TYPE>/<ACCESSION_NUMBER>/
```

For example, to find the 10-K for VTR with accession number `0000740260-25-000052`, you would navigate to:

```
/VTR/10-K/0000740260-25-000052/
```

**What files are in each filing directory?**

-   `clean-text-for-llm.txt`: The clean, narrative text of the filing, with HTML, XBRL, and other markup removed.
-   `xbrl-data-markdown.md`: Structured financial data extracted from the filing's inline XBRL tags, presented in markdown tables.

**What are the limitations of the data?**

-   **Images are not included**: Images and graphical content are not processed.
-   **Complex table structures may be lost**: HTML tables in the narrative text are converted to plain text, potentially losing their original structure.
-   **Limited scope of documents**: Processing focuses on main filing documents (8-K, 10-K, 10-Q) and key exhibits (EX-99.1, EX-99.2).
-   **Simplified XBRL data**: The XBRL extraction is basic and does not parse the full XBRL taxonomy for complex financial relationships.