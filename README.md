# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

### Program:
## Name: MUKESH P
## Register number: 212222240068

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('VJK.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions

# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)

# Display results using Matplotlib
plt.figure(figsize=(12, 12))

# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

# Sobel Edge Detection
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

# Laplacian Edge Detection
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

# Canny Edge Detection
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

# Show all results
plt.tight_layout()
plt.show()
```

## Output:
### Original Image

![WhatsApp Image 2024-10-16 at 16 11 25_eff86cf1](https://github.com/user-attachments/assets/03bff3cc-871f-4409-a314-394a0e10a36b)

### SOBEL EDGE DETECTOR

![WhatsApp Image 2024-10-16 at 16 11 30_1246442b](https://github.com/user-attachments/assets/6c1a2428-ec9c-42c5-b3cf-8f43341e7214)




### LAPLACIAN EDGE DETECTOR

![WhatsApp Image 2024-10-16 at 16 11 36_7f2414e9](https://github.com/user-attachments/assets/43466e19-3b29-422b-a4af-eca29d31fe54)




### CANNY EDGE DETECTOR

![WhatsApp Image 2024-10-16 at 16 11 42_6380711d](https://github.com/user-attachments/assets/35d64be8-c101-48d6-9f24-8261187f4f7f)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
