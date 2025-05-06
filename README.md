# GHG Emissions Dataset - Brazil

This repository contains a small sample of greenhouse gas (GHG) emissions data from companies that voluntarily reported their emissions to the [GHG Protocol Brazil Registry](https://registropublicodeemissoes.fgv.br/). The data is organized by company, sector, scope, and year.

## Dataset Overview

| Column         | Description                                                  |
|----------------|--------------------------------------------------------------|
| ID             | Internal sequential ID assigned during extraction            |
| Empresa        | Reporting company name                                       |
| Setor          | Economic sector (e.g., Industry, Energy, Services)           |
| Subsetor       | Subsector classification                                     |
| Escopo         | Emissions scope (e.g., Scope 1, Scope 2 - localização, etc.) |
| 2008 - 2023    | Emissions in metric tons CO₂e reported for each year         |

> ⚠️ This dataset is a **simplified sample**, for educational and illustrative use only. Do not use it for official or decision-making purposes.

---

##  How the data was collected

The full dataset was built using a custom Python web scraping pipeline that combines:

- `Selenium`: to interact with the GHG Protocol site and render JavaScript-based content.
- `BeautifulSoup`: to parse HTML tables with emission values.
- `PyAutoGUI`: to extract elements that were not directly accessible through HTML, such as company names or sector labels embedded in the UI.

The scraper loops through a range of numeric IDs corresponding to companies in the registry, extracts available data, and saves it in a structured tabular format.

---

## Files

- `ghg_emissions_sample.csv`: Sample emissions data (anonymized or public companies only)
- `README.md`: This file with context and documentation

---

## Example Use Cases

This sample dataset can be used for:
- Testing emissions dashboards (e.g., in Power BI, Python, or R)
- Prototyping emission analysis pipelines
- Benchmarking emission factors by sector/scope/year

---

## License

This repository is intended for educational and illustrative purposes. The original data source is the [GHG Protocol Brazil Registry](https://registropublicodeemissoes.fgv.br/), which hosts all complete and official emissions records submitted by companies voluntarily.

