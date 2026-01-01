# 🏥 Physician Notetaker AI

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Stable-red)
![Transformers](https://img.shields.io/badge/Hugging%20Face-Transformers-yellow)
![spaCy](https://img.shields.io/badge/spaCy-NLP-green)

## 📖 Overview
**Physician Notetaker** is an AI-powered NLP pipeline designed to automate the documentation process for healthcare professionals. It processes raw physician-patient dialogue transcripts to:
1.  **Extract Medical Entities**: Identifies symptoms, diagnoses, treatments, and prognoses.
2.  **Analyze Patient Sentiment**: Uses Deep Learning (Transformers) to detect patient anxiety or reassurance.
3.  **Generate SOAP Notes**: Automatically structures extracted data into a clinical **S**ubjective, **O**bjective, **A**ssessment, and **P**lan format.

---

## 🚀 Features
* **Medical Named Entity Recognition (NER)**: 
    * Utilizes `spaCy` (with support for `en_core_med7_lg`) and regex heuristics to extract clinical terms.
* **Transformer-Based Sentiment Analysis**: 
    * Implements a native **PyTorch** pipeline using `DistilBERT` fine-tuned on SST-2.
    * Maps general sentiment (Positive/Negative) to clinical context (Reassured/Anxious).
* **Automated SOAP Generation**: 
    * Converts unstructured dialogue into a structured JSON report ready for Electronic Health Records (EHR).

---

## 📂 Project Structure

```bash
physician-notetaker/
│
├── physician_notetaker.py   # Main pipeline script (NER + Sentiment + SOAP)
├── requirements.txt         # List of dependencies
└── README.md                # Project documentation
---

### 🔬 System Execution & Pipeline Output

<p align="center">
  <img src="assets/physician_pipeline_output.png" alt="Physician Notetaker Pipeline Output" width="900"/>
</p>

---
---

### 📄 Generated SOAP Note & JSON Output

<p align="center">
  <img src="assets/soap_note_output.png" alt="Generated SOAP Note and Medical JSON Output" width="900"/>
</p>

---
