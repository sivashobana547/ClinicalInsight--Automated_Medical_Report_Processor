# ClinicalInsight

**ClinicalInsight** is an AI-powered pipeline that digitizes medical PDFs via OCR, anonymizes PHI, and uses LLMs to extract clinical events, synthesize medical history, and analyze lab results. It provides structured, privacy-conscious insights for healthcare professionals to assist in longitudinal patient monitoring and clinical decision-making.

## Key Features

* **Document Digitization:** Seamlessly converts PDF medical reports into machine-readable text using `Tesseract OCR` and `pdf2image`.
* **Privacy-First Design:** Implements automatic PII/PHI detection and anonymization with an optional re-identification module for authorized use.
* **LLM-Powered Analysis:** * Extracts structured JSON data (dates, events, categories).
    * Synthesizes historical medical information across multiple reports.
    * Analyzes lab values, assesses severity, and provides non-prescriptive recommendations.

## Technology Stack

* **Language:** Python
* **OCR:** Tesseract, Poppler
* **LLM Integration:** Groq API (Llama 3.1)
* **Data Processing:** Regex, JSON, Pandas

## Setup and Installation

### Prerequisites
* Tesseract OCR and Poppler installed on your system.
* A valid [Groq API Key](https://console.groq.com/).

### Installation
1. Clone this repository.
2. Install the required dependencies:
   ```bash
   pip install pytesseract pdf2image pillow groq
Set your API key:

Bash
export GROQ_API_KEY='your_api_key_here'
Usage
Upload your patient medical PDFs.

The pipeline extracts, anonymizes, and processes the text using Llama 3.1.

The output is a structured JSON containing a medical history summary, identified diseases, medications, and an analysis of the latest laboratory results.

Privacy & Compliance
This tool is intended for research and clinical decision-support. Users must ensure compliance with local healthcare data protection regulations (e.g., HIPAA, GDPR) when processing sensitive patient information.
