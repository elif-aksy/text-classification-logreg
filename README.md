# Image Fusion & Resolution Enhancement (Pansharpening Pipeline)

## Overview
This project implements and compares multiple **pansharpening / image fusion** strategies to enhance spatial detail in color images by combining:
- a **low-resolution RGB** image (MS),
- a **high-resolution grayscale (PAN)** image.

The notebook focuses on an **end-to-end fusion workflow**: preprocessing, fusion, visualization, and quantitative evaluation.

---

## What’s Implemented
The notebook includes the following fusion approaches:

### 1) IHS-Based Fusion (Intensity Substitution)
- Convert the upsampled RGB image to an IHS/HSV-like representation
- Match intensity statistics (and/or histogram) between intensity and PAN
- Substitute or fuse the **Intensity** component using PAN
- Convert back to RGB

**Goal:** preserve color structure while improving spatial sharpness.

---

### 2) IHS-Like Fusion (Detail Injection Baseline)
- Compute a base intensity from the upsampled RGB
- Normalize/match PAN to the intensity distribution
- Inject PAN detail into RGB channels

**Goal:** a strong baseline to compare against IHS substitution.

---

### 3) Brovey Transform
- Compute intensity from RGB channels
- Use ratio-based modulation with PAN:
  - gain = PAN / (Intensity + eps)
  - fused = RGB * gain

**Goal:** aggressive sharpening and contrast enhancement (may introduce spectral distortion).

---

### 4) Gram–Schmidt / Detail Injection Baseline
- Build an intensity proxy from RGB
- Match PAN to intensity statistics
- Inject the detail component (PAN - Intensity) into RGB

**Goal:** another commonly-used baseline for spatial detail injection.

---

### 5) Hybrid Fusion (Weighted Blend)
- Combine IHS and Brovey outputs with a weight `w`:
  - hybrid = w * IHS + (1-w) * Brovey

**Goal:** balance color preservation (IHS) with sharpness (Brovey).

---

## Evaluation
Fusion quality is evaluated with both **visual comparison** and quantitative metrics:
- **MSE**
- **PSNR (dB)**
- **SAM (deg)**
- **SCC** (spatial correlation / correlation-based measure)

These metrics help compare trade-offs between spatial enhancement and spectral distortion.

---

## Tech Stack
- Python
- NumPy
- OpenCV
- scikit-image
- SciPy
- Matplotlib

---

## How to Run
1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
