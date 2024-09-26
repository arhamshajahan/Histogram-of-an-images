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
```
# Developed By: SANJAY S
# Register Number: 212222230132


!pip install opencv-python

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('gray_image.jpeg')
color_image = cv2.imread('color_image.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
gray_image=cv2.imread('gray_image.jpeg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('color_image.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
gray_image = cv2.imread("gray_image.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/9c93ba99-a35d-44b3-9114-7acb136c368e)

### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image

![image](https://github.com/user-attachments/assets/eb7e421b-ad69-4757-9037-cf1b0085f08b)

![image](https://github.com/user-attachments/assets/3de3c73f-6bf2-4b01-96ca-0583244668b5)

#### Color Image

![image](https://github.com/user-attachments/assets/335eb738-c9cd-465d-ab3c-d58dabce4b49)

![image](https://github.com/user-attachments/assets/a12235d1-28ec-4e0e-83e2-3d6285b49d0b)

### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/46994668-8072-42bb-9941-693aadc88e86)

![image](https://github.com/user-attachments/assets/78c6b286-b9dc-405d-9780-0580a6b06f8b)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
