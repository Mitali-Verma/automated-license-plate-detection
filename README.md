#Comparative Analysis of Automated License Plate Recognition Systems 

This repository presents a comprehensive comparative analysis of six state-of-the-art Automated License Plate Recognition (ALPR) methods: YOLOv8 with EasyOCR, Faster R-CNN with CRNN, PaddleOCR, LPRNet, Vision Transformer (ViT)-based OCR, and Tesseract OCR. Each method is rigorously evaluated on a curated international dataset of 588-591 license plate images encompassing diverse geographic formats from multiple countries including India, United States, European Union, and Asian nations, captured under varied lighting conditions, weather scenarios, viewing angles, and challenging real-world scenarios including glare, occlusions, and motion blur. 

## Experimental Setup

All experiments were conducted using Google Colab
for GPU acceleration. The provided notebooks reflect
this environment and may require minor adjustments
for local execution.

## Installation

pip install -r requirements.txt

## System Dependencies

This project uses Tesseract OCR.

Install Tesseract before running the code:

### Ubuntu
sudo apt-get install tesseract-ocr

### Windows
Download installer from:
https://github.com/tesseract-ocr/tesseract

# Experimental Results
### Table I: Comparative Performance Analysis of Six ALPR Methods

| Method                     | Detection Rate (%) | Avg. Confidence | Inference Speed (ms) | Quality Score (/100) | High Conf. Rate (%) | Failed Rate (%) |
|----------------------------|-------------------:|----------------:|---------------------:|---------------------:|--------------------:|----------------:|
| YOLOv8 + EasyOCR           | 64.5               | 0.708           | 10.0                | 74.6                | 55.9               | 34.7            |
| Faster R-CNN + CRNN        | 73.0               | —               | —                   | —                   | —                  | 27.0            |
| PaddleOCR                  | 0.0                | —               | 20–30               | —                   | 0.0                | 100.0           |
| Tesseract OCR              | 1.87               | 0.302           | —                   | 82.14               | 0.0                | 98.13           |
| LPRNet                     | 87.0               | 0.80            | 3–5                 | 83.0                | 70.0               | 13.0            |
| ViT-based OCR (TrOCR)      | 98.98              | 0.777           | 15–25               | 88.16               | 38.6               | 1.02            |


**Note:** Due to the absence of character-level ground truth annotations,
performance is evaluated using plate-level detection rates, confidence
scores, and format validation metrics rather than character accuracy.
