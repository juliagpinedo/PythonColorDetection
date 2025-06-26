# 🎨 Python Color Detection (Dominant Color Matcher)

This project detects the **dominant color** of a specific UI element (e.g., a button) in mobile app screenshots. It's particularly useful for automated UI verification, such as checking whether a button is disabled (gray) or enabled (green) based on visual appearance.

## 🧠 How It Works

The script uses computer vision and clustering to detect the **most frequent color** in a selected region of a screenshot.

- Loads the screenshot using OpenCV.
- Crops the image to focus on a specific UI element (e.g., a button).
- Filters out near-white pixels (e.g., white text or background).
- Applies K-Means clustering to identify the **dominant color**.
- Compares the dominant color to an expected hex value (like `#35c759` or `#8e8e93`) using Euclidean distance.

## 🧭 Workflow Overview

1. **Load the screenshot**  
   Read the image file and convert to RGB.

2. **Crop the desired region**  
   Focus only on the UI element you're checking (e.g., the "Continue" button).

3. **Extract dominant color**  
   - Filter out near-white pixels.
   - Apply K-Means clustering to identify the dominant color.

4. **Compare to expected hex value**  
   Match against a predefined color using RGB distance.

## 📦 Requirements

- Python 3.7+
- OpenCV (`opencv-python`)
- scikit-learn
- matplotlib
- numpy

```bash
pip install opencv-python scikit-learn matplotlib numpy
