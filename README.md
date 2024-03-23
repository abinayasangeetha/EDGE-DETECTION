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
## PROGRAM:
```
 DEVELOPED BY:ABINAYA S
 REGISTER NUMBER: 212222230002
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dandelions.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
## SOBEL X:
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
## SOBEL Y:
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBEL XY:
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![dandelions](https://github.com/abinayasangeetha/EDGE-DETECTION/assets/119393675/512eea3b-9569-4113-ad2b-5824e32c3fb1)

### SOBEL EDGE DETECTOR:

![Screenshot 2024-03-23 135419](https://github.com/abinayasangeetha/EDGE-DETECTION/assets/119393675/6dab248a-d189-494b-967c-8b5ac04eff5d)

![Screenshot 2024-03-23 135442](https://github.com/abinayasangeetha/EDGE-DETECTION/assets/119393675/9f8e9fcf-e093-487a-99d2-f405c976285f)


![Screenshot 2024-03-23 135532](https://github.com/abinayasangeetha/EDGE-DETECTION/assets/119393675/5ae6640b-f168-44c1-81e2-650efa2b7271)

### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-03-23 135606](https://github.com/abinayasangeetha/EDGE-DETECTION/assets/119393675/5586402b-dc0b-4ad9-bc99-603a82b235ed)

### CANNY EDGE DETECTOR
![Screenshot 2024-03-23 135650](https://github.com/abinayasangeetha/EDGE-DETECTION/assets/119393675/ded49785-2b66-414d-96bb-07a2c13b337c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
