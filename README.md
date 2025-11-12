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

## Output:
### DEVELOPED BY : LOGU R
### REG NO : 212224230141
### ORIGINAL IMAGE
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('/content/LOGU PASSPORT IMAGE.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/7ebf253c-b224-46e9-ae01-f66046c04b54" />

### SOBEL EDGE DETECTOR
```Python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/bae2dd01-2822-461d-aeef-61e3437a3070" />

### LAPLACIAN EDGE DETECTOR
```Python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/559ace52-867f-487d-b775-169aab348326" />

### CANNY EDGE DETECTOR
```Python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  

```
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/6ffd9fe8-f5bf-44e7-8340-adab7d9e4b9b" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
