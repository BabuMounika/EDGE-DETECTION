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
## Program:
### ORIGINAL IMAGE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('pigeon.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE:
<img width="707" height="564" alt="Screenshot 2025-10-04 104440" src="https://github.com/user-attachments/assets/16e9bc9e-d5d5-4336-a08c-b7e4a11165fd" />

### SOBEL EDGE DETECTOR:
<img width="739" height="551" alt="Screenshot 2025-10-04 104453" src="https://github.com/user-attachments/assets/a56f6184-6009-409f-8a39-f93030473533" />



### LAPLACIAN EDGE DETECTOR:
<img width="699" height="547" alt="Screenshot 2025-10-04 104501" src="https://github.com/user-attachments/assets/19a8f626-86a3-43c3-b06b-022ebd3aa92e" />



### CANNY EDGE DETECTOR:
<img width="698" height="555" alt="Screenshot 2025-10-04 104509" src="https://github.com/user-attachments/assets/d483d442-8a6b-430e-aafc-ebfdfc629512" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
