# Seam Carving for Image Resizing

## Description

This project implements **seam carving**, an image resizing technique that removes **horizontal and vertical seams** while preserving important visual content. The implementation follows a **dynamic programming approach** to find and remove the lowest-energy seams in an image.

## Features

- **Energy Calculation:** Computes an energy image using **Kornia’s SpatialGradient**.
- **Dynamic Programming:** Constructs a scoring matrix to find optimal seams.
- **Seam Removal:** Removes vertical and horizontal seams iteratively to resize the image.
- **Helper Function (`CarvingHelper`)**: Handles seam removal for either direction.
- **Seam Transposition Technique:** Transposes the image to reuse the function for both horizontal and vertical seam removal.

## Technologies Used

- **Python**
- **NumPy**
- **Matplotlib**
- **Torch**
- **Kornia**

## Installation

```bash
pip install numpy matplotlib torch kornia
```

## Project Tasks

### **Task 1: Compute the Energy Image**
- Use **Kornia’s SpatialGradient** to compute the gradient magnitude image.

### **Task 2: Construct the Scoring Matrix**
- Initialize a matrix **M** with dimensions matching the input image.
- Populate **M** using dynamic programming to find the optimal seams.

### **Task 3: Seam Removal**
- Trace and remove the seam with the lowest accumulated energy.
- Repeat until the target image size is reached.

### **Task 4: Implement Seam Removal with `CarvingHelper`**
- Remove vertical seams first.
- Transpose the image and remove horizontal seams using the same function.

## Visualizations

- **Original vs. Resized Image:** Compare images before and after seam carving.
- **Energy Map Visualization:** Display the computed energy map.
- **Seam Removal Steps:** Show step-by-step seam removal process.

