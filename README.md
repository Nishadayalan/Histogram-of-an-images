# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: NISHA D
# Register Number:212223230143
```
### Bright Image
```
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
```
# Load the color image
image = cv2.imread('bright.jpg')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
# Plotting the original grayscale image, equalized image, and histograms
plt.figure(figsize=(10, 7))
```
```
# Show original grayscale image
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Show equalized grayscale image
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
```
# Plot histogram of the original grayscale image
plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
```
# Plot histogram of the equalized image
plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
```
plt.tight_layout()
plt.show()
```
### Dark Image
```
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
```
# Load the color image
image = cv2.imread('dark.jpg')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
# Plotting the original grayscale image, equalized image, and histograms
plt.figure(figsize=(10, 7))
```
```
# Show original grayscale image
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Show equalized grayscale image
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
```
# Plot histogram of the original grayscale image
plt.subplot(2, 2, 3)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
```
# Plot histogram of the equalized image
plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
```
plt.tight_layout()
plt.show()


```
## Output:
```python
# Developed By: NISHA D
# Register Number:212223230143
```
### Output of Bright Image:
![image](https://github.com/user-attachments/assets/8bc05ede-fe5b-4a9d-86e5-a3a077e3bedf)
![image](https://github.com/user-attachments/assets/5e631897-be1d-4bc8-a589-05ecb4ac7710)

![image](https://github.com/user-attachments/assets/b171bca1-5a43-4741-99ef-a30f756fc5e4)
![image](https://github.com/user-attachments/assets/9c32cfc6-912f-4cd4-a4e6-4214727ab413)


### Output of Dark Image:
![image](https://github.com/user-attachments/assets/d1bc84f1-868b-42f8-9ab9-0f9107ab19c8)
![image](https://github.com/user-attachments/assets/5a040ba0-b0aa-4aae-84e5-3ba7ece55bd4)
![image](https://github.com/user-attachments/assets/c56b6484-dd72-4243-9f8e-afe796f5bc99)

![image](https://github.com/user-attachments/assets/137c5bce-4f0c-4379-ad2b-117c523ddce7)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
