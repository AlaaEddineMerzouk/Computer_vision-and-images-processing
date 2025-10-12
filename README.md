# 🔬 Lab 2 — Image Convolution

## 🎯 Objective

The purpose of this lab is to understand the fundamentals of **image convolution** and how different filters (kernels) can modify, enhance, or extract information from digital images.

---

## ⚙️ Tools Used

- **Python 3**
- **OpenCV (cv2)**
- **NumPy**
- **Matplotlib**
- **Google Colab** (for experimentation and visualization)

---

## 🧩 Lab Tasks Overview

1. **Select and load an image**
   - Load an image from local storage using `cv2.imread()` or `matplotlib`.

2. **Apply Mean Filter (G1)**
   - Use a 3×3 mean kernel to blur the image and reduce noise.
   - Understand how averaging neighboring pixels smooths sharp transitions.

3. **Create and Apply Intensity Filter (G2)**
   - A filter that multiplies image intensities by 2 to increase brightness.

4. **Apply Sharpening Filter (G3)**
   - Enhance image details using a kernel that emphasizes edges and textures.

5. **Apply Custom Filter (G4)**
   - Experiment with a directional filter to highlight edges in specific orientations.

6. **Double Blur (G1 applied twice)**
   - Observe how repeated convolution increases smoothing.

7. **Apply Sobel Filters**
   - Use horizontal and vertical Sobel kernels to detect image edges and gradients.

---

## 🧮 Kernels Used

| Filter | Kernel Matrix | Purpose |
|:--------|:--------------|:---------|
| **Mean (G1)** | (1/9) × \[\[1,1,1\],\[1,1,1\],\[1,1,1\]\] | Blur and noise reduction |
| **Intensity (G2)** | \[\[0,0,0\],\[0,2,0\],\[0,0,0\]\] | Brightness amplification |
| **Sharpening (G3)** | \[\[0,-1,0\],\[-1,5,-1\],\[0,-1,0\]\] | Highlight edges and details |
| **Custom (G4)** | \[\[-1,-1,0\],\[-1,3,0\],\[0,0,0\]\] | Directional edge emphasis |
| **Sobel X** | \[\[-1,0,1\],\[-2,0,2\],\[-1,0,1\]\] | Detect vertical edges |
| **Sobel Y** | \[\[-1,-2,-1\],\[0,0,0\],\[1,2,1\]\] | Detect horizontal edges |

---

## 🧠 Key Learnings

- Convolution is a mathematical operation that combines neighboring pixels to produce new image values.
- Filters (kernels) control how the image changes — from **blurring** to **sharpening** to **edge detection**.
- Applying filters sequentially (like double blurring) compounds their effects.
- Sobel filters are foundational for **edge detection**, used in many vision applications like object recognition and segmentation.

---

## 📊 Example Output

| Original | Mean Filter | Sharpened | Sobel Edges |
|-----------|--------------|------------|--------------|
| ![Original](sample_original.png) | ![Blurred](sample_blur.png) | ![Sharpened](sample_sharp.png) | ![Edges](sample_sobel.png) |

*(Images above are examples – results vary by input image.)*

---

## 🧾 Author & Course Info

**Author:** Alaa Eddine Merzouk  
**Institution:** École Supérieure d’Informatique Sidi Bel Abbès  
**Course:** Computer Vision  
**Date:** October 12, 2025

---

## 🧰 How to Run

1. Open [Google Colab](https://colab.research.google.com/).  
2. Upload the notebook `Image_Convolution_Lab.ipynb`.  
3. Upload any image (e.g., `cat.jpg`, `flower.png`).  
4. Run all cells to see the effects of each convolution filter.

---

## 🔗 Repository Structure

