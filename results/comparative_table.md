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