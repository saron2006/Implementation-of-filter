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
### Developed By   : SARON XAVIER A
### Register Number: 212223230197
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("tree.png")
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


median=cv2.medianBlur(image2,13)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
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
### Original Image
![Screenshot 2025-04-25 121957](https://github.com/user-attachments/assets/f92ad45c-c2f3-4275-aca9-1454302c72ef)


### 1. Smoothing Filters

# i) Using Averaging Filter
![Screenshot 2025-04-25 122006](https://github.com/user-attachments/assets/409280d9-7199-4583-99a4-9315324c7a56)


# ii)Using Weighted Averaging Filter
![Screenshot 2025-04-25 122019](https://github.com/user-attachments/assets/25aeff8f-d433-4c44-b0cf-ae66b15eef7f)


# iii)Using Gaussian Filter
![Screenshot 2025-04-25 122033](https://github.com/user-attachments/assets/dc23a915-0bea-41d1-bf9f-602634cd71f3)


# iv) Using Median Filter
![Screenshot 2025-04-25 122044](https://github.com/user-attachments/assets/7e18c9c5-bd24-4825-9294-cfbd604f3d3e)


### 2. Sharpening Filters
</br>

# i) Using Laplacian Kernal
![Screenshot 2025-04-25 122053](https://github.com/user-attachments/assets/0f63edf7-151d-4f00-9955-823f54de771f)


# ii) Using Laplacian Operator
![Screenshot 2025-04-25 122104](https://github.com/user-attachments/assets/c82d4cad-f139-4cf5-8498-7c3b718f0198)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
