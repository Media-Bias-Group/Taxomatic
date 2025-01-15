# Leveraging Large Language Models for Automated Definition Extraction with TaxoMatic - a Case Study on Media Bias

## Overview

This repository contains the code, data, and evaluation files used in the paper **"Leveraging Large Language Models for Automated Definition Extraction with TaxoMatic - a Case Study on Media Bias"**. The project explores the feasibility of using Large Language Models (LLMs) to extract, classify, and evaluate definitions related to media bias from academic literature. More information will be added in case of paper acceptance.

## Project Structure

The repository is organized into two main sections: **Code** and **Data**.

### 1. Code

The codebase consists of several scripts and notebooks designed to automate the following steps of the research process:

- **SES Scraper**: Scripts for searching Semantic Scholar database and retrieving information about relevant literature on media bias.
- **PDF Scraping**: Python scripts for extracting full-text content from PDF documents. Later files are converted them into a machine-readable format using tools like GROBID.
- **Grobid to df**: Formatting XLSX files after the previous step and transforms extracted content from GROBID into body text that is suitable for further processing.
- **Relevance Classification**: Classification of articles using 5 different LLMs (GPT, Claude, etc.) and 8 distinct prompting strategies to determine the relevance of articles to media bias definitions.
- **Definition Extraction**: Scripts utilizing **Claude** for the extraction of media bias definitions from relevant articles.
- **Performance Evaluation**: Code for evaluating the performance of both classification and definition extraction processes, including manual and automated evaluations.

### 2. Data

This folder includes the data generated and used during the project, broken down into the following categories:

- **Manually Evaluated Articles**: A subset of academic articles that were manually assessed for relevance to media bias definitions, serving as ground truth data for evaluation.
- **LLM-based Relevance Classifications**: Outputs from the relevance classification step (5 files, names {model}_relevance), where articles were classified using different LLM models and prompting techniques.
- **Extracted Definitions**: Definitions of media bias extracted both manually and via LLMs, used for comparison and evaluation.
- **Keywords**: Extensive list of keywords used for scholarly database search.

### 3. Performance Evaluation Files

This folder contains the evaluation scripts and results for both stages of the project:

1. **Relevance Evaluation**: Performance metrics (e.g., accuracy, F1 score) for the LLM-based relevance classification of scholarly articles.
2. **Definition Evaluation**: Evaluation of the extracted definitions using cosine similarity, including error analysis and performance comparisons between LLM-based and manual definitions.

