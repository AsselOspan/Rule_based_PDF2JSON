# PDF2JSON: Rule-Based Metadata Extraction from Newspaper PDFs

## Overview

**PDF2JSON** is a hybrid rule-based pipeline designed to automatically extract structured metadata from PDF documents (e.g., title, author, date, abstract, text, journal, category). It leverages Python tools such as `PyMuPDF`, `pdfminer.six`, and `pdfplumber` to parse and process newspaper archives and output clean, machine-readable JSON files suitable for downstream applications like training large language models.

This project was developed to support structured data collection from printed publications in low-resource languages.

## Features

- Integration of multiple rule-based parsers for optimal text and layout extraction  
- Cleansing and normalization of raw OCR text  
- Automatic metadata tagging (e.g., title, date, abstract, journal)  
- Output generation in standardized JSON format  
- Designed for scalability on large collections of PDF documents

## Technologies Used

- Python 3.x  
- [pdfminer.six](https://github.com/pdfminer/pdfminer.six)  
- [PyMuPDF](https://pymupdf.readthedocs.io/)  
- [pdfplumber](https://github.com/jsvine/pdfplumber)  
- `re`, `unicodedata`, and standard Python I/O modules

## Installation

```bash
pip install pdfminer.six PyMuPDF pdfplumber
```

## Usage

```python
from pdf2json import process_pdf

pdf_path = "path/to/file.pdf"
json_data = process_pdf(pdf_path)

# Save JSON
with open("output.json", "w", encoding="utf-8") as f:
    json.dump(json_data, f, ensure_ascii=False, indent=2)
```

## Folder Structure

```
PDF2JSON/
│
├── PDF2JSON.ipynb       # Main Jupyter notebook with pipeline steps
├── sample_data/         # Example PDFs
├── outputs/             # Extracted JSON files
└── README.md            # Project documentation
```

## Applications

- Data preparation for training/fine-tuning LLMs  
- Digital archiving and information retrieval  
- Media monitoring and journalism analytics  

## Contributors

- Assel Ospan  
- Madina Mansurova  
- Talshyn Sarsembayeva  
- Kanat Auyesbay  
- Aman Mussa
