# 📄 Information Retrieval from Business Receipts Using Deep Learning

Bachelor’s Thesis Project (BTP)  
Department of Computer Science and Engineering  
Harcourt Butler Technical University, Kanpur  

Authors:  
Parit Kansal | Shubh Gupta | Pankhuri Gupta  

---

## 🚀 Overview

This project presents an end-to-end deep learning pipeline for automated information extraction from business receipts.  

The system integrates:

- **Mask R-CNN** for receipt detection and segmentation  
- **Donut (OCR-Free Transformer)** for structured text extraction  

Unlike traditional OCR-based systems, this approach directly extracts structured information from document images without relying on intermediate OCR steps.

---

## 🧠 System Architecture

### Stage 1 — Receipt Segmentation
- Model: Mask R-CNN  
- Dataset: CORD  
- Synthetic dataset generation for robustness  
- Metrics: mAP, mAR (IoU-based evaluation)

### Stage 2 — Structured Text Extraction
- Model: Donut (Vision Transformer + Decoder)  
- Dataset: SROIE  
- Output Format: Structured JSON  
- Extraction Accuracy: **81%**

---

## 🏗 Synthetic Data Contribution

A custom synthetic dataset was generated to improve model generalization by:

- Overlaying receipts on diverse backgrounds  
- Applying random rotations (±5°)  
- Generating instance masks and bounding boxes  
- Assigning unique pixel values per receipt  

This improved robustness to real-world variations.

---

## 📊 Results

### Mask R-CNN Performance
- AP @ IoU 0.50:0.95 → 0.971  
- AP @ IoU 0.50 → 0.989  
- AR @ IoU 0.50:0.95 → 0.980  

### Donut Performance
- Structured Text Extraction Accuracy → **81%**

The system successfully extracts:
- Company Name  
- Address  
- Date  
- Total Amount  

---

## ⚙️ Tech Stack

- Python  
- PyTorch  
- Mask R-CNN  
- Donut (OCR-Free Transformer)  
- Vision Transformer (ViT)  
- CORD Dataset  
- SROIE Dataset  

---

## 💻 Implementation Repository

The full implementation code (developed collaboratively as part of BTP) is available here:

🔗 **[https://drive.google.com/drive/folders/1oLWKWWXEHUaJnVEU-zFkxtA0eNppcIPR]**

1. Donut Model
2. notebook for data creation and object detection
3. Object detection API(git folder)
4. Notebook to generate API for object detection
5. Donut Model Training
6. Inference Notebook
7. Project Report

---

## 👤 My Contribution (Shubh Gupta)

- Contributed to model integration and pipeline design  
- Assisted in synthetic dataset generation  
- Worked on model evaluation and performance analysis  
- Participated in experimentation and system validation  

---

## 🔮 Applications

- Financial automation  
- Expense management systems  
- Invoice processing  
- Intelligent document processing  
- Enterprise workflow automation  

---

## 📌 Note

This repository contains the research paper and project overview.  
The implementation was developed collaboratively during our BTP.
