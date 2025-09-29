# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.


### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.
## Program:
```
 Developed By   :Pavithra S
 Register Number:212223230147
```

### 1. Smoothing Filters

## i) Using Averaging Filter
```

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("/content/dog.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()




```
## ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
## iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```
## iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
## i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()





```
## ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters


## i) Using Averaging Filter
<img width="596" height="222" alt="Screenshot 2025-09-29 123436" src="https://github.com/user-attachments/assets/0f021c7f-9ab3-4f71-9280-b74b1c264490" />



## ii)Using Weighted Averaging Filter


<img width="456" height="175" alt="Screenshot 2025-09-29 123442" src="https://github.com/user-attachments/assets/58920b4f-668c-4f04-8d48-b19c0e962c85" />

## iii)Using Gaussian Filter
<img width="465" height="167" alt="Screenshot 2025-09-29 123448" src="https://github.com/user-attachments/assets/4be40b40-22ed-4967-9bba-824fa3999009" />



## iv) Using Median Filter

<img width="596" height="229" alt="Screenshot 2025-09-29 123453" src="https://github.com/user-attachments/assets/e4fda9d2-cc12-4191-9243-93dfb9458d11" />


### 2. Sharpening Filters


## i) Using Laplacian Kernal

<img width="448" height="172" alt="Screenshot 2025-09-29 123458" src="https://github.com/user-attachments/assets/41245957-63a0-4bce-a092-8f5e60f4e715" />


## ii) Using Laplacian Operator
<img width="446" height="169" alt="Screenshot 2025-09-29 123503" src="https://github.com/user-attachments/assets/42e72fac-8af8-45fb-86b8-1a1cbe6ea4e6" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
