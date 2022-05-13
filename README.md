# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required modules.
</br> 

### Step2
</br>
Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By   : Challa Sandeep
### Register Number: 212221240011
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bike.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")



```
ii) Using Weighted Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bike.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")



```
iii) Using Gaussian Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bike.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")



```

iv) Using Median Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bike.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bike.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")





```
ii) Using Laplacian Operator
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bike.png")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
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
</br>

i) Using Averaging Filter
</br>
<img width="600" alt="1" src="https://user-images.githubusercontent.com/93427522/168239991-ef28595a-17e4-4d3b-9404-e58a4904d36f.png">
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>
<img width="600" alt="2" src="https://user-images.githubusercontent.com/93427522/168240014-3c2baeed-d914-4fc6-bb79-2156e38819bf.png">
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>
</br>
<img width="600" alt="3" src="https://user-images.githubusercontent.com/93427522/168240071-0ba64847-1232-4ec7-829a-932b9d89bea3.png">

</br>
</br>
</br>

iv) Using Median Filter
</br>
<img width="600" alt="4" src="https://user-images.githubusercontent.com/93427522/168240091-d87eae1c-d69a-4944-8f43-38953bf95fb6.png">
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
<img width="600" alt="5" src="https://user-images.githubusercontent.com/93427522/168240157-c2ba0127-97b6-4f19-8f8c-b864dd3ebb4b.png">
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
<img width="600" alt="6" src="https://user-images.githubusercontent.com/93427522/168240177-9d84e52b-415e-45de-b3cb-9ecdd10e45c7.png">
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
