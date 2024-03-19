# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Read the test image
</br> 

### Step2
Define the identity kernel, using a 3×3 NumPy array
</br> 

### Step3
Use the filter2D() function in OpenCV to perform the linear filtering operation
</br> 

### Step4
Display the original and filtered images, using imshow()
</br> 

### Step5
Save the filtered image to disk, using imwrite()
</br> 

## Program: 
### Developed By   : SRI SAI PRIYA.S
### Register Number: 212222240103
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\dog.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel = np.ones((11,11), np. float32)/121
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(9,9))
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
image1 = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\dog.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image4 = cv2.filter2D(image2, -1, kernel2)
plt.imshow(image4)
plt.title('Weighted Averaging Filtered')
```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\dog.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

gaussian_blur = cv2.GaussianBlur(src=image2, ksize=(11,11), sigmaX=0, sigmaY=0)
plt.imshow(gaussian_blur)
plt.title(' Gaussian Blurring Filtered')
```

iv) Using Median Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\dog.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

median=cv2.medianBlur (src=image2, ksize=11)
plt.imshow(median)
plt.title(' Median Blurring Filtered')
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\dog.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel3 = np.array([[0,1,0], [1, -4,1],[0,1,0]])
image5 =cv2.filter2D(image2, -1, kernel3)
plt.imshow(image5)
plt.title('Laplacian Kernel')
```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\dog.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

new_image = cv2.Laplacian (image2, cv2.CV_64F)
plt.imshow(new_image)
plt.title('Laplacian Operator')
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

![image](https://github.com/SriSaiPriyaSenthilvel/Implementation-of-filter/assets/119475702/b79d1e3c-7b93-4475-b6e7-aa8f2ffef1d0)

</br>
</br>

ii) Using Weighted Averaging Filter

![image](https://github.com/SriSaiPriyaSenthilvel/Implementation-of-filter/assets/119475702/46c7eaf0-6354-4385-921d-4dbfa4a3995b)

</br>
</br>

iii) Using Gaussian Filter

![image](https://github.com/SriSaiPriyaSenthilvel/Implementation-of-filter/assets/119475702/17d7dc98-35b9-4e56-99bb-d6baee1e6975)

</br>
</br>

iv) Using Median Filter

![image](https://github.com/SriSaiPriyaSenthilvel/Implementation-of-filter/assets/119475702/9f9d3aa9-26aa-4d76-a4e8-f8d5c59ac858)

</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![image](https://github.com/SriSaiPriyaSenthilvel/Implementation-of-filter/assets/119475702/46bd9318-758a-4e77-9d2a-403106090afc)

</br>
</br>

ii) Using Laplacian Operator

![image](https://github.com/SriSaiPriyaSenthilvel/Implementation-of-filter/assets/119475702/5ac5f67a-a207-4428-a718-371944615869)

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
