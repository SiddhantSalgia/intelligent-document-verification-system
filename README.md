# FinVerify

## Computer Vision-Based Banking Document Verification and Tampering Detection System

FinVerify is a Computer Vision-based document verification system designed for banking and fintech use cases. The project focuses on analysing uploaded banking documents such as cheques, bank statements, identity documents, and proof-of-address records to determine whether the document is valid, clear, complete, or potentially suspicious.

Unlike a basic OCR system that only extracts text from an image, FinVerify focuses on visual document understanding. The system uses image preprocessing, document quality assessment, document classification, tampering detection, and optional OCR-based field validation to support banking document verification workflows.

---

## Problem Statement

Banks and fintech companies receive large volumes of uploaded financial documents for account opening, cheque processing, KYC verification, loan applications, and compliance checks. These documents may be blurry, cropped, low-quality, incomplete, digitally edited, or potentially fraudulent.

Manual review of every uploaded document is time-consuming and inconsistent. A document may contain readable text but still be visually suspicious due to editing, splicing, inconsistent regions, or poor image quality. Therefore, there is a need for an AI-assisted system that can analyse the document image itself and flag documents that require manual review.

FinVerify aims to solve this problem by using Computer Vision and Deep Learning techniques to assess the authenticity, quality, and visual integrity of banking documents.

---

## Project Summary

FinVerify is an AI-powered banking document verification system that analyses document images and generates a verification result. The system accepts uploaded banking documents and performs visual checks to detect issues such as blur, cropping, missing regions, poor lighting, suspicious edits, and possible tampering.

The core focus of the project is Computer Vision. OCR may be used as an additional supporting feature to extract fields such as name, date, amount, or account number, but the main objective is not simple text extraction. Instead, the system focuses on understanding the visual structure and integrity of the document.

The final output is a verification report containing document type, image quality status, tampering risk, suspicious regions, OCR confidence if applicable, and a final recommendation such as Accept, Reject, or Manual Review.

---

## Key Features

* Upload banking or financial document images
* Classify document type such as cheque, bank statement, ID card, or utility bill
* Detect blurry, low-resolution, or poor-quality uploads
* Detect cropped or incomplete documents
* Identify suspicious visual regions
* Detect possible tampering or digital manipulation
* Optionally extract text using OCR for field validation
* Generate document risk score
* Display verification result in a dashboard
* Recommend Accept, Reject, or Manual Review

---

## Core Computer Vision Tasks

### 1. Document Classification

The system classifies the uploaded image into categories such as:

* Cheque
* Bank statement
* Identity document
* Utility bill
* Unknown document

Possible models:

* CNN
* ResNet
* EfficientNet
* Vision Transformer

---

### 2. Document Quality Assessment

The system checks whether the uploaded document is suitable for verification.

Quality checks may include:

* Blur detection
* Brightness and contrast analysis
* Resolution check
* Cropping detection
* Skew detection
* Noise detection

---

### 3. Tampering Detection

The system analyses whether the document image appears visually manipulated.

Possible suspicious signs:

* Edited amount fields
* Different font or texture regions
* Copy-paste artefacts
* Inconsistent background patterns
* Spliced image regions
* Unnatural compression artefacts

Possible approaches:

* CNN-based binary classification
* Image forgery detection
* Error Level Analysis
* Patch-based anomaly detection
* Autoencoder-based anomaly detection

---

### 4. Optional OCR-Based Validation

OCR is used only as a supporting component.

OCR can extract:

* Name
* Date
* Amount
* Account number
* Address
* Document ID

The extracted fields can then be validated using rule-based checks.

Example:

* Amount in words matches amount in numbers
* Date is not expired
* Account number format is valid
* Required fields are present

---

## System Workflow

```text
User Uploads Document
        ↓
Image Preprocessing
        ↓
Document Classification
        ↓
Document Quality Assessment
        ↓
Tampering Detection
        ↓
Optional OCR Field Extraction
        ↓
Risk Scoring
        ↓
Verification Dashboard
```

---

## Example Output

```text
Document Type: Cheque

Image Quality: Good

Blur Detection: Passed

Cropping Detection: Passed

Tampering Risk: Medium

Suspicious Region:
- Amount field

OCR Confidence: 87%

Fraud Risk Score: 64/100

Recommendation: Manual Review
```

---

## Tech Stack

### Frontend

* React.js
* HTML
* CSS / Tailwind CSS

### Backend

* Python
* Flask / FastAPI

### Computer Vision / Deep Learning

* OpenCV
* PyTorch / TensorFlow
* CNN / ResNet / EfficientNet
* Autoencoder
* Image preprocessing techniques

### OCR

* EasyOCR / Tesseract OCR

### Database

* SQLite / PostgreSQL

---

## Machine Learning and Deep Learning Approach

The project can be developed in multiple stages.

### Phase 1: Rule-Based Computer Vision

* Blur detection using Laplacian variance
* Brightness and contrast analysis
* Skew detection
* Cropping and boundary checks
* Basic image quality score

### Phase 2: Document Classification

Train a CNN-based model to classify uploaded documents into categories such as cheque, bank statement, ID card, or utility bill.

### Phase 3: Tampering Detection

Train a deep learning model to classify documents as authentic or suspicious. This can be done using labelled datasets or synthetic tampering, where parts of document images are edited to create suspicious samples.

### Phase 4: OCR Field Validation

Use OCR to extract important fields and validate them using rule-based checks.

### Phase 5: Full-Stack Integration

Integrate the Computer Vision pipeline with a React frontend and Flask/FastAPI backend.

---

## Project Objectives

* Build a practical Computer Vision project for banking and fintech
* Detect poor-quality and suspicious document uploads
* Apply deep learning to document classification and tampering detection
* Use OCR only as a supporting feature for field validation
* Create a full-stack AI application with frontend, backend, and model integration
* Generate clear verification reports for banking document review

---

## Future Improvements

* Signature verification
* Handwritten text recognition
* Tampered region localisation
* Support for PDF documents
* Explainable AI visual heatmaps
* Cloud deployment on AWS or Azure
* User authentication
* Audit logs for compliance
* Integration with real banking workflows

---

## Disclaimer

This project is developed for educational and portfolio purposes. It is not intended to replace professional fraud investigation, banking compliance, or legal verification systems. The system is designed to assist document verification and risk screening, while final decisions should be made by authorised human reviewers.

---

## Author

Siddhant
Master of Artificial Intelligence
University of Technology Sydney                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        