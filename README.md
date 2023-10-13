# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required packages for further process.
<br>

### Step2:
<br>
Read the image and convert the bgr image to gray scale image.
<br>

### Step3:
<br>
Use any filters for smoothing the image to reduse the noise.
<br>

### Step4:
<br>
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>

### Step5:
<br>
Display the filtered image using plot and imshow.
<br>

## Program:
```
DEVELOPED BY : ROSHINI RK
REG NO : 212222230123
```


### Import the packages
```
import cv2
import matplotlib.pyplot as plt
```

### Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("rose.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```


### SOBEL EDGE DETECTOR
### SOBEL X AXIS :
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
### SOBEL Y AXIS :
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
### SOBEL XY AXIS :
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


### CANNY EDGE DETECTOR
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
### SOBEL X AXIS :
<br>

![image](https://github.com/roshiniRK/EDGEDETECTION/assets/118956165/0b6a7a7d-71c1-4172-a23b-24f3a1c143e1)

<br>

### SOBEL Y AXIS :
<br>

![image](https://github.com/roshiniRK/EDGEDETECTION/assets/118956165/569b3288-c43a-42dd-a53a-9b09078b66d7)



<br>

### SOBEL XY AXIS :
<br>

![image](https://github.com/roshiniRK/EDGEDETECTION/assets/118956165/59342455-169c-412a-bea8-6f919cd85609)


<br>

### LAPLACIAN EDGE DETECTOR
<br>

![image](https://github.com/roshiniRK/EDGEDETECTION/assets/118956165/b361ebb6-764c-42ed-9a60-ce9da359348a)


<br>



### CANNY EDGE DETECTOR
<br>

![image](https://github.com/roshiniRK/EDGEDETECTION/assets/118956165/e0ca191e-50ef-4027-9e9a-e3c6a07db5ad)


<br>


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
