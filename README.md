# IMPLEMENTATION-OF-FILTERSS
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
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program. 

## Program:
### Developed By   : Thirukaalathessvarar S
### Register Number: 212222230161
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('unspash.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel = np.ones ((11,11), np.float32)/121
image3=cv2.filter2D(image2,-1, kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('unspash.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16 
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('unspash.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```

iv) Using Median Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('unspash.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
median=cv2.medianBlur(src=image2, ksize=11)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("4.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (10,10))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Laplacian kernel Filtered Image")
plt.axis("on")
```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('spiderman.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")
```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter
![dip1_exp6](https://github.com/Thirukaalathessvarar-S/IMPLEMENTATION-OF-FILTERSS/assets/121166390/883b22e8-6fb8-41f0-803b-187ad4464b72)

ii) Using Weighted Averaging Filter
![dip2_exp6](https://github.com/Thirukaalathessvarar-S/IMPLEMENTATION-OF-FILTERSS/assets/121166390/43809522-2033-4047-90c9-cde9b19339c9)


iii) Using Gaussian Filter
![dip3_exp6](https://github.com/Thirukaalathessvarar-S/IMPLEMENTATION-OF-FILTERSS/assets/121166390/57405af1-8a74-4a49-a751-4f5705ec3b1a)


iv) Using Median Filter
![dip4_exp6](https://github.com/Thirukaalathessvarar-S/IMPLEMENTATION-OF-FILTERSS/assets/121166390/52dadf7e-3de4-4e41-96d2-4d5f22a0762f)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![dip5_exp6](https://github.com/Thirukaalathessvarar-S/IMPLEMENTATION-OF-FILTERSS/assets/121166390/2dc9b409-3dd5-49f2-ac28-ba3f8c71588d)


ii) Using Laplacian Operator
![dip6_exp6](https://github.com/Thirukaalathessvarar-S/IMPLEMENTATION-OF-FILTERSS/assets/121166390/c955a006-93a9-47aa-9f28-b3710e5b7766)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
