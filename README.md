# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
<br>
### Step2:
Read the image and convert the bgr image to gray scale image.
<br>
### Step3:
Use any filters for smoothing the image to reduse the noise.
<br>
### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>
### Step5:
Display the filtered image using plot and imshow.
<br>

## Program:

```
DEVELOPED BY: SANJAY G
REG NO : 212222230131
```
# Import the packages
```
import cv2
import matplotlib.pyplot as pl
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("newo.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR
## SOBEL X
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
## SOBEL Y
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBEL XY
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
#### SOBEL X
![image](https://github.com/Jaiganesh235/EDGE-DETECTION/assets/118657189/aadd8bb3-9a87-4535-a843-8f4364feb642)


#### SOBEL Y
![image](https://github.com/Jaiganesh235/EDGE-DETECTION/assets/118657189/b8dab61e-4f18-4aca-a001-fb3e52059a85)


#### SOBEL XY
![image](https://github.com/Jaiganesh235/EDGE-DETECTION/assets/118657189/d5a94c9e-97a5-4bc7-9dc1-2ca87c1a03e7)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Jaiganesh235/EDGE-DETECTION/assets/118657189/b11e0ad7-16fc-43bf-a3fd-edc631ee572a)


### CANNY EDGE DETECTOR
![image](https://github.com/Jaiganesh235/EDGE-DETECTION/assets/118657189/590e7819-853f-41d3-8478-26f9a920ba37)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
