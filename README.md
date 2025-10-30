# Processed SEC EDGAR Filings for Senior Housing REITs

This repository contains processed SEC EDGAR filings for senior housing REITs, making them easier to access and analyze for natural language processing and financial analysis tasks.

## Tickers Included

- **AHR**: American Healthcare REIT, Inc.
- **DHC**: Diversified Healthcare Trust
- **VTR**: Ventas, Inc.
- **WELL**: Welltower Inc.

## Data Coverage

The filings in this repository cover the period from **2024 to 2025**.

## Repository Structure

To navigate the repository, follow this structure:

```
/<TICKER>/<FORM_TYPE>/<ACCESSION_NUMBER>/
```

For example, to find the 10-K for VTR with accession number `0000740260-25-000052`, you would navigate to:

```
/VTR/10-K/0000740260-25-000052/
```

### Processed Files

Within each accession number directory, you will find the following files:

-   `clean-text-for-llm.txt`: This file contains the clean, narrative text of the filing, with HTML, XBRL, and other markup removed. It is suitable for natural language processing and analysis.
-   `xbrl-data-markdown.md`: This file contains structured financial data extracted from the filing's inline XBRL tags, presented in markdown tables for easy readability.

## Limitations

The processing scripts (`extract_text.py` and `batch_process_filings.py`) have the following limitations, which affect the content of the processed files:

-   **Images are not included**: Any images or graphical content within the filings are skipped and not converted to text (i.e., no OCR is performed).
-   **Complex table structures may be lost**: While the XBRL data is extracted into markdown tables, complex HTML tables in the narrative text are converted to plain text, which may result in a loss of their original structure.
-   **Exhibits and other documents**: The processing focuses on the main filing documents (8-K, 10-K, 10-Q) and key exhibits (EX-99.1, EX-99.2). Other documents, such as XBRL schema files, are excluded.
-   **XBRL data is simplified**: The XBRL extraction is basic and captures inline XBRL tags. It does not parse the full XBRL taxonomy to establish complex relationships between financial concepts.
