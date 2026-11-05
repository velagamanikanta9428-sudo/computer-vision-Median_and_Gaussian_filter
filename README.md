# Image Smoothing Using Median and Gaussian Filters

## Aim
To perform image smoothing using **Median Filtering** and **Gaussian Filtering**, and compare their outputs with the original grayscale image.

## Overview
This Jupyter Notebook uses OpenCV and Matplotlib to apply two filtering techniques to an input image:

1. Reads the input image in grayscale.
2. Creates a copy of the original image.
3. Applies a 3 × 3 Median Filter.
4. Applies a 3 × 3 Gaussian Filter.
5. Displays the original image, median-filtered image, and Gaussian-filtered image side by side.

## Technologies Used
- Python
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Jupyter Notebook / Google Colab

## Project Structure
```text
CV-Lab-08/
├── CVLAB08.ipynb
├── Salt & pepper Image.jpg  
└── README.md
```

## Requirements
Install the required packages:

```bash
pip install opencv-python numpy matplotlib
```

## How to Run

### Option 1: Jupyter Notebook

1. Clone or download this repository.
2. Open a terminal in the project folder.
3. Install the dependencies:
   ```bash
   pip install opencv-python numpy matplotlib
   ```
4. Place `Salt & pepper Image.jpg` in the project folder.
5. Open the notebook:
   ```bash
   jupyter notebook CVLAB08.ipynb
   ```
6. Update the image path in the notebook, if necessary.
7. Run the notebook cell.

### Option 2: Google Colab

1. Upload `CVLAB08.ipynb` to Google Colab.
2. Upload `Salt & pepper Image.jpg` to your Google Drive at the path expected by the notebook, or change the path in the code.
3. Run the notebook cell.

## Important Code

The notebook currently reads the image from this Google Drive path:

```python
A = cv2.imread('/content/drive/MyDrive/COMPUTER VISION/Salt & pepper Image.jpg', 0)
```
The `0` argument loads the image in grayscale.

### Median Filter

```python
median_filter = cv2.medianBlur(noisy_img, 3)
```

Median filtering replaces each pixel with the median value of its neighborhood. It is commonly used to reduce impulse (salt-and-pepper) noise.

### Gaussian Filter

```python
gaussian_filter = cv2.GaussianBlur(noisy_img, (3, 3), 0)
```

Gaussian filtering smooths an image using a Gaussian-weighted neighborhood. It can reduce high-frequency noise and fine detail.

## Expected Output
The notebook displays three grayscale images side by side:

- **Original Input** – the input image.
- **Median Filter** – the result after median filtering.
- **Gaussian Filter** – the result after Gaussian smoothing.

## Notes
- The notebook expects an input image named `Salt & pepper Image.jpg` at the configured path.
- Add the input image to the GitHub repository so others can reproduce the output.
- If the notebook prints `Error: Image not found.`, check the image filename and path.
- The notebook uses a 3 × 3 kernel for both filters.

## Author
Velaga Manikanta Sai.

241FA23016.

Data Science-A.


