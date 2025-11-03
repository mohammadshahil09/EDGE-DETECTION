# EDGE-DETECTION
## Name: MOHAMMAD SHAHIL
## Reg : 212223240044
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

## Program :
```
DEVELOPED BY : MOHAMMAD SHAHIL
REG NO : 212223240044
```

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shail.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
![WhatsApp Image 2025-11-03 at 11 19 47_e2099d99](https://github.com/user-attachments/assets/ce339916-8f65-48a8-b82a-c227818f2bdd)


### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![WhatsApp Image 2025-11-03 at 11 20 02_250e696a](https://github.com/user-attachments/assets/0f73ca48-e2cf-4152-b044-440272a60474)


### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
![WhatsApp Image 2025-11-03 at 11 20 18_7f53481c](https://github.com/user-attachments/assets/c0974c14-7447-444b-8beb-771f8a9e1319)



### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

```
![WhatsApp Image 2025-11-03 at 11 20 34_cb0e264e](https://github.com/user-attachments/assets/03bb3ac3-b2e0-4f60-808d-a7b049aa018d)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
