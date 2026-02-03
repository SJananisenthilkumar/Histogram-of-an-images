# EXP - 03
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
# Developed By: JANANI S
# Register Number: 212223230086

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('rose.jpeg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])



plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()


```
## Output:

### Input Grayscale Image and Color Image

<img width="365" height="415" alt="image" src="https://github.com/user-attachments/assets/4018265c-3649-49f9-bb87-a3f84ca53409" />

<img width="350" height="413" alt="image" src="https://github.com/user-attachments/assets/e6d847ce-3e36-442b-aafd-556fa68b9cae" />

### Histogram of Grayscale Image and any channel of Color Image

<img width="634" height="447" alt="image" src="https://github.com/user-attachments/assets/cf1f6595-1f33-456e-92a5-1c0cc73bbe3a" />


### Histogram Equalization of Grayscale Image.

<img width="664" height="440" alt="image" src="https://github.com/user-attachments/assets/57a30f33-90fb-491c-b1b5-70d59afdb77c" />


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
