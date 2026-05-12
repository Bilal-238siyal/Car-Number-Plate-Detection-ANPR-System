readme_content = """# Automated Number Plate Detection and Recognition System

## AI Powered License Plate Detection and OCR Pipeline

---

An end-to-end ANPR system that detects vehicle license plates using YOLOv8 and extracts registration numbers using EasyOCR. The system first locates license plates in images, then applies OCR to read the plate text with preprocessing for improved accuracy.

---

## Overview

This project is an AI based number plate recognition system built using two models working together. The first model is a YOLOv8-nano fine-tuned on a license plate dataset to detect plates in images. The second component is EasyOCR that extracts the registration number from the detected plate region. The complete pipeline provides an end to end solution for automatic vehicle identification.

---

## Dataset

| Dataset | Purpose | Samples |
|---------|---------|---------|
| Car Number Plate Dataset (YOLO Format) | Plate Detection | 437 images (350 train, 87 val) |
| Source: Kaggle - Sujay Mann | Single class: license_plate | YOLO annotation format |

---

## Model Architecture

| Component | Model | Parameters | Task |
|-----------|-------|------------|------|
| Plate Detection | YOLOv8-nano | 3.0M | Detects license plates in images |
| Text Recognition | EasyOCR | Pre-trained | Extracts text from plate regions |

---

## Results

| Metric | Score |
|--------|-------|
| mAP50 | 0.903 |
| mAP50-95 | 0.554 |
| Precision | 0.895 |
| Recall | 0.828 |
| Inference Speed | 2.5ms per image (T4 GPU) |
| Training Epochs | 37 (early stopped) |

---

## Features

- Real-time license plate detection using YOLOv8
- OCR-based text extraction from detected plates
- Image preprocessing pipeline (grayscale, bilateral filtering, sharpening)
- Handles multiple plates in a single image
- Automatic filtering of state headers (IND, PUNJAB, etc.)
- Works with various Indian license plate formats
- Trained with automatic mixed precision for efficiency
- Early stopping to prevent overfitting

---

## Project Structure
