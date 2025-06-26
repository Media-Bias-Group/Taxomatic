# TaxoMatic: Leveraging Large Language Models for Automated Definition Extraction

This repository contains the code, data, and evaluation files used in the paper **"Leveraging Large Language Models for Automated Definition Extraction with TaxoMatic - a Case Study on Media Bias"**. The project explores using Large Language Models (LLMs) to extract, classify, and evaluate definitions related to media bias from academic literature. 

Since no suitable datasets for testing definition extraction were available, we created one specifically for the media bias domain, where definitions are diverse and often unclear.
---

## Project Structure

### 1. Code

The codebase includes scripts and notebooks for automating the research process:

- **SES Scraper**: Searches the Semantic Scholar database for literature on media bias.
- **PDF Scraping**: Extracts full-text content from PDFs and converts them to machine-readable formats using GROBID.
- **GROBID to df**: Formats and transforms extracted content for further processing.
- **Relevance Classification**: Utilizes five LLMs (e.g., GPT, Claude) and eight prompting strategies to classify article relevance to media bias definitions.
- **Definition Extraction**: Prompts Claude 3 with five strategies to extract media bias definitions from relevant articles.
- **Performance Evaluation**: Evaluates classification and definition extraction processes, including manual and automated methods.

---

### 2. Data

The `Data` folder includes:

- **Manually Evaluated Articles**: Ground truth data of articles assessed for relevance.
- **LLM-based Relevance Classifications**: Outputs from classification by different LLMs.
- **Extracted Definitions**: Manually and automatically extracted media bias definitions.
- **Keywords**: A comprehensive list of keywords for scholarly searches.

---

### 3. Performance Evaluation Files

The `Evaluation` folder contains:

- **Relevance Evaluation**: Performance metrics (e.g., accuracy, F1 score) for article classification.
- **Definition Evaluation**: Cosine similarity analysis, error analysis, and comparisons between manual and LLM-based extractions.

---

## Data Composition

The dataset includes:

- 2,398 articles annotated for relevance.
- 123 definitions manually extracted from 113 relevant articles.
- A filtered sample of 75,151 open-access academic papers based on relevance and citation count.

### Key Features:

- Articles filtered by citation count (≥100).
- Minimal noise due to extraction errors during PDF processing.
- No offensive content; all articles are publicly available.

---

## Collection Process

1. **Data Sources**: Keyword-based searches on Semantic Scholar.
2. **Extraction**: Automated scraping scripts and GROBID for PDF-to-XML conversion.
3. **Annotation**: Manual relevance checks by six researchers with expertise in media bias.

---

## Preprocessing and Labeling

- PDFs converted to XML using GROBID.
- Manual annotation for relevance and definition extraction.
- Raw PDFs and processed XML files are stored for reproducibility.
- All preprocessing scripts are included in this repository.

---

## Uses

This dataset and code were used to evaluate the TaxoMatic framework for:

1. Classifying relevant articles.
2. Extracting definitions.

In the future, TaxoMatic could support research on concept extraction, semantic analysis, and taxonomy building in various domains.

---

## Distribution

- On acceptance, this repository will be made publicly available under an open-source license.
- Contains only open-access and open-source materials.
- No further regulatory restrictions.

---

## Maintenance

The TaxoMatic research team will maintain this repository. Updates and contact details will be shared upon paper acceptance. Contributions are welcome!

---

We hope this repository serves as a valuable resource for researchers exploring automated definition extraction and media bias!
