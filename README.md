# Synthetic-ERP-Fraud-Data

<div align="justify">
This repository provides synthetic ERP fraud data for the unpublished paper "An Agent-based Approach for Generating Customizable Synthetic ERP Data for Fraud Detection", submitted to ICAART 2027 – 19th International Conference on Agents and Artificial Intelligence.

The dataset was created to address the scarcity of publicly available ERP fraud data. An AI agent simulates both legitimate business processes and fraud cases within configurable organizational and behavioral constraints. The planned process executions are 
subsequently carried out in an SAP S/4HANA system to generate realistic ERP transaction data. The dataset accompanying the paper contains regular Procure-to-Pay (P2P) processes, multiple fraud cases, and legitimate process variants generated within the Global 
Bike Inc. (GBI) model company.


## Data

The repository contains the extracted and processed records from the following SAP S/4HANA tables:

- **BKPF (Accounting Document Header):** Stores header-level information for financial accounting documents, including document numbers, posting dates, company codes, and document types.
- **BSEG (Accounting Document Segment):** Contains the line items of accounting documents, including vendor postings, G/L accounts, and monetary amounts.
- **CDHDR (Change Document Header):** Records header information for changes performed in SAP business objects.
- **CDPOS (Change Document Items):** Stores the detailed field-level changes associated with change documents recorded in CDHDR.
- **EBAN (Purchase Requisitions):** Contains purchase requisition data generated during procurement processes.
- **EKKO (Purchase Order Header):** Stores header information for purchase orders, such as vendor references, purchasing organizations, and document dates.
- **EKPO (Purchase Order Items):** Contains the individual material positions associated with purchase orders.
- **MKPF (Material Document Header):** Stores header-level information for goods movements and inventory transactions.
- **MSEG (Material Document Items):** Contains detailed material movement records, including quantities, storage locations, and movement types.
- **RBKP (Invoice Document Header):** Stores header information for logistics invoice verification documents.
- **RSEG (Invoice Document Items):** Contains the individual invoice line items associated with supplier invoices.

Together, these tables capture the complete execution trace of the generated Procure-to-Pay (P2P) scenarios, including procurement activities, inventory movements, invoices, accounting postings, and master data changes. 
This enables the reconstruction and analysis of both legitimate business processes and fraud scenarios.



## Licence
Shield: [![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

This work is licensed under a
[Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc].

[![CC BY-NC 4.0][cc-by-nc-image]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg

