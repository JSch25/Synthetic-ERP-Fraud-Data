# Synthetic-ERP-Fraud-Data

<div align="justify">

This repository provides synthetic ERP fraud data accompanying the unpublished paper *"An Agent-Based Approach for Generating Customizable Synthetic ERP Data for Fraud Detection"*, submitted to ICAART 2027 – 19th International Conference on Agents and Artificial Intelligence.

The data addresses the scarcity of publicly available ERP fraud data, which limits research on fraud detection in enterprise systems. To overcome this challenge, an AI agent simulates both legitimate business processes and fraud scenarios while adhering to configurable organizational, temporal, and behavioral constraints. The resulting process plans are subsequently executed in an SAP S/4HANA system to generate realistic ERP transaction data. The data contains regular Procure-to-Pay (P2P) processes, multiple fraud cases, and legitimate process variants generated within the Global Bike Inc. model company. 


## Data

The repository contains the extracted and processed records from the following SAP S/4HANA tables:

- **BKPF (Accounting Document Header):** Header data of accounting documents.
- **BSEG (Accounting Document Segment):** Line items belonging to accounting documents in BKPF.
- **CDHDR (Change Document Header):** Header data for changes performed in SAP business objects.
- **CDPOS (Change Document Items):** Field-level changes belonging to change documents in CDHDR.
- **EBAN (Purchase Requisitions):** Purchase requisition documents.
- **EKKO (Purchase Order Header):** Header data of purchase orders.
- **EKPO (Purchase Order Items):** Material line items belonging to purchase orders in EKKO.
- **MKPF (Material Document Header):** Header data of material documents and goods movements.
- **MSEG (Material Document Items):** Material movement line items belonging to documents in MKPF.
- **RBKP (Invoice Document Header):** Header data of supplier invoice documents.
- **RSEG (Invoice Document Items):** Invoice line items belonging to documents in RBKP.

Together, these tables capture the complete execution trace of the generated P2P processes and fraud cases, including procurement activities, inventory movements, invoices, accounting postings, and master data changes. This enables the reconstruction and analysis of both legitimate business processes and fraud cases.

In addition to the SAP data tables, the repository includes the file **post-processing-manifest.yaml**, which provides the ground-truth information required to interpret the generated data. For each executed scenario, the document specifies whether it represents a regular P2P process, a legitimate P2P variant, or a fraud case. In addition, the manifest contains the complete sequence of process steps executed within each scenario. Furthermore, the repository also contains the file **object_registry.jsonl**. This document links the generated scenarios and process steps to the corresponding SAP document numbers created during execution. For each process step, the registry records the generated SAP document identifiers, allowing the extracted SAP table records to be connected to the ground-truth labels defined in the post-processing manifest. Furthermore, the registry enables the reconstruction of relationships between individual process steps within a scenario by tracing the business objects passed from one step to another.



## Licence
Shield: [![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

This work is licensed under a
[Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc].

[![CC BY-NC 4.0][cc-by-nc-image]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg

