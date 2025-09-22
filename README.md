# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:

Import the required libraries.

### Step2:

Convert the image from BGR to RGB.

### Step3:

Apply the required filters for the image separately.

### Step4:

Plot the original and filtered image by using matplotlib.pyplot.

### Step5:

End the program.

## Program:
### Developed By   : Amruthavarshini Gopal
### Register Number: 212223230013
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("photo1.jpeg")
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
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```Python
median = cv2.medianBlur(image2, 13)
plt.imshow(cv2.cvtColor(median, cv2.COLOR_BGR2RGB))
plt.title("Median Blur")
plt.axis('off')
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

<img width="915" height="476" alt="Screenshot 2025-09-22 094657" src="https://github.com/user-attachments/assets/e53bff94-d262-4c94-b75b-7231343d1ca4" />


ii)Using Weighted Averaging Filter

<img width="500" height="536" alt="Screenshot 2025-09-22 095851" src="https://github.com/user-attachments/assets/f79b68f5-8c1d-41b6-9313-8bf4951e152c" />


iii)Using Gaussian Filter

<img width="504" height="530" alt="Screenshot 2025-09-22 095949" src="https://github.com/user-attachments/assets/3ed97c0a-be1a-4e3a-96a5-a4960d53782d" />

iv) Using Median Filter

<img width="510" height="511" alt="Screenshot 2025-09-22 100048" src="https://github.com/user-attachments/assets/e396a5ee-bc28-4434-93ff-f7e3fc19343b" />


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

<img width="520" height="537" alt="Screenshot 2025-09-22 100126" src="https://github.com/user-attachments/assets/ee397c14-eb49-49dc-8d39-2f88b7d21c93" />


ii) Using Laplacian Operator

<img width="520" height="532" alt="Screenshot 2025-09-22 100158" src="https://github.com/user-attachments/assets/13aaf147-5a09-44f6-b625-32e7e8c83502" />

## Result:

Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
