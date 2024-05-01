# EDGE DETECTION

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

## Program
```
Developed by : JANANI.S
Reg. No. : 212222230049
```
### RGB to Gray conversion

```python
import cv2
import matplotlib.pyplot as plt
img=cv2.imread('peacock.jpg')
gray=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imwrite('peacock.jpg',gray)
plt.imshow(gray,cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.show()
```
### Import Packages and load the image

```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("flower.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
#### SOBEL X
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
#### SOBEL Y
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
#### SOBEL XY
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### ORIGINAL IMAGE

![Screenshot 2024-05-01 134222](https://github.com/JananiSoundararajan/EDGE-DETECTION/assets/119477549/3c7db012-d85d-483b-8981-3c2140d75ee8)


### SOBEL EDGE DETECTOR

![Screenshot 2024-05-01 134512](https://github.com/JananiSoundararajan/EDGE-DETECTION/assets/119477549/b0e4b022-0964-4453-80b5-0d85ab5bd6f8)

![Screenshot 2024-05-01 134606](https://github.com/JananiSoundararajan/EDGE-DETECTION/assets/119477549/9c005434-cf05-4208-b082-05b825a15cf5)

![xy](https://github.com/JananiSoundararajan/EDGE-DETECTION/assets/119477549/71376f99-58be-47fc-a90f-dfab161e99e5)


### LAPLACIAN EDGE DETECTOR

![lap](https://github.com/JananiSoundararajan/EDGE-DETECTION/assets/119477549/87adf774-6db5-4cc8-9240-643aa545543d)

### CANNY EDGE DETECTOR

![ced0](https://github.com/JananiSoundararajan/EDGE-DETECTION/assets/119477549/53869ea9-4e9e-4dda-8ec0-6b5c092466d7)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
