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
### Developed by: PULI NAGA NEERAJ
### Register Number: 212223240130
### Importing packages,load and convert to gray image
```
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('flower.jpg',0)
gray=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.imshow(gray)
```
### SOBEL EDGE DETECTOR
### SOBEL X
```
sobel_x = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobel_x,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### Sobel Y
```
sobel_y = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobel_y,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### Sobel XY
```
sobel_xy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobel_xy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### Laplacian Edge Detector
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### Canny Edge Detector
```
canny=cv2.Canny(gray_image,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:

### Gray Scale: 

![flower1](https://github.com/PuliNagaNeeraj/EDGE-DETECTION/assets/138849173/9b311a6d-c21f-4746-b757-d74adb5e9b76)

### SOBEL EDGE DETECTOR
#### Sobel X

![flower2](https://github.com/PuliNagaNeeraj/EDGE-DETECTION/assets/138849173/4cddc104-318b-444d-a152-fd215582960b)

#### Sobel Y

![flower3](https://github.com/PuliNagaNeeraj/EDGE-DETECTION/assets/138849173/4bd81a39-2722-4d60-b6c9-baa3231c597e)

#### Sobel XY

![flower4](https://github.com/PuliNagaNeeraj/EDGE-DETECTION/assets/138849173/26d1cee4-2ec1-42ef-a063-e33c1d5102d1)

### LAPLACIAN EDGE DETECTOR

![flower5](https://github.com/PuliNagaNeeraj/EDGE-DETECTION/assets/138849173/0e2cfe22-3a44-427e-bb25-d79a6e5eefc1)

### CANNY EDGE DETECTOR

![flower6](https://github.com/PuliNagaNeeraj/EDGE-DETECTION/assets/138849173/49ea9a04-034f-4b02-89dd-83752f44061a)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
