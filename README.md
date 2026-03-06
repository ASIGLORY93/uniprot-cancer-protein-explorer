# uniprot-cancer-protein-explorer
A reproducible Python notebook for programmatic access to UniProt cancer protein data, starting with TP53. Demonstrates REST API queries, metadata handling and data export
# 🧬 UniProt Cancer Protein Explorer

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ASIGLORY93/uniprot-cancer-protein-explorer/blob/main/UniProt_Cancer_Protein_Explorer.ipynb)
[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![UniProt](https://img.shields.io/badge/Data-UniProt_REST_API-teal.svg)](https://www.uniprot.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

 A reproducible Python notebook for programmatic access to UniProt cancer protein data, starting with TP53. Demonstrates REST API queries, metadata handling and data export. A beginner-friendly Python notebook for querying human cancer protein data from the UniProt REST API (Application Programming Interface). Built as a hands-on project following the **UniProt Programmatic Data Access Webinar** hosted by EMBL-EBI (European Molecular Biology Laboratory, European Bioinformatics Institute).

## 📖 About This Project

This project was built to apply knowledge gained from an EMBL-EBI webinar on programmatic access to UniProt, delivered by **Aurélien Luciani** and **Emily Bowler-Barnett**.

The notebook demonstrates how to use the UniProt REST API to:
- Search for human cancer proteins using gene names
- Read and interpret response headers as metadata
- Handle HTTP (HyperText Transfer Protocol) status codes correctly
- Display results in a clean, readable table
- Export data to CSV (Comma-Separated Values) for use in Excel or Google Sheets

The starting example uses **TP53**  the most frequently mutated gene in human cancers, often called the *guardian of the genome*.

## 🚀 Quick Start

No installation needed. Click the badge below to open directly in Google Colab and run in your browser:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ASIGLORY93/uniprot-cancer-protein-explorer/blob/main/UniProt_Cancer_Protein_Explorer.ipynb)

Once open, click **Runtime > Run All** and the notebook will run from top to bottom automatically.

## 🔬 What the Notebook Does

| Step   |             Action                        |     What It Demonstrates 
|--------|-------------------------------------------|-----------------------------
| Step 1 |        Import Python libraries            | requests, pandas, IPython setup 
| Step 2 |        Connect to UniProt REST API        | Base URL configuration and helper function 
| Step 3 |        Search for cancer proteins         | SOLR (Simple Object Lookup and Retrieval) query format 
| Step 4 |        Read response headers              | Metadata: x-total-results, x-uniprot-release 
| Step 5 |        Display results as a table         | JSON (JavaScript Object Notation) parsing with pandas 
| Step 6 |        Generate UniProt links             | Direct links to each protein entry page 
| Step 7 |        Save to CSV file                   | Export for Excel or Google Sheets 


## 🧪 Sample Output

Searching for **TP53** in *Homo sapiens* (Human), reviewed entries only:

| Accession | Gene |      Protein Name          |    Organism  | Length | Score |
|-----------|------|----------------------------|--------------|--------|-------|
| P04637    | TP53 | Cellular tumor antigen p53 | Homo sapiens | 393 aa | 5 / 5 |

**Response headers confirmed:**
- `x-total-results`: 1 matching reviewed entry
- `x-uniprot-release`: 2026_01 (January 2026 database release)

## 🎯 How to Customise

Change the `SEARCH_GENE` variable in **Step 3** to explore any cancer gene:

python
# Change this to any cancer gene you want to explore
SEARCH_GENE = 'TP53'   # Try: BRCA1, KRAS, EGFR, MYC, BRCA2, PTEN


Re-run the notebook and it will automatically fetch and display the new results.


## 📡 Key Concepts Covered

**REST API** — Representational State Transfer Application Programming Interface. A web service that returns data in response to HTTP requests.

**SOLR Query Format** — The search syntax used by UniProt. The UniProt Advanced Search UI (User Interface) generates this automatically so you do not need to learn it from scratch.

**Response Headers** — Metadata returned alongside the data:
- `x-total-results` tells you the TRUE total number of matches, not just what is on the current page
- `link` provides the URL for the next page of results (pagination)

**HTTP Status Codes:**
- `2xx` — Success. Your request worked
- `4xx` — Client error. Check your query or URL (Uniform Resource Locator)
- `5xx` — Server error. Contact UniProt support if it persists


## 🛠️ Requirements

All dependencies are pre-installed in Google Colab. If running locally:

bash
pip install requests pandas


## 📚 Resources

| Resource | Link |
|----------|------|
| UniProt Website | https://www.uniprot.org |
| REST API Base URL | https://rest.uniprot.org |
| API Documentation | https://www.uniprot.org/help/api |
| UniProtKB API Docs | https://www.uniprot.org/api-documentation/uniprotkb |
| Google Colab | https://colab.research.google.com |


## 🎓 Based On

This project was inspired by the **UniProt Programmatic Data Access Webinar** hosted by:
- **Aurélien Luciani** — EMBL-EBI
- **Emily Bowler-Barnett** — EMBL-EBI

Organised by EMBL-EBI 


## 📄 License

This project is open source and available under the [MIT License](LICENSE).


## 🤝 Connect

If you found this useful, feel free to ⭐ star the repository and share it with fellow researchers!

*Built with curiosity and a love for open science. 🔬*

