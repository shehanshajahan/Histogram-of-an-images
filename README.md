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
# Developed By: Shehan Shajahan
# Register Number: 212223240154
```
### Input Grayscale Image and Color Image
```import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grayretriever.jpg")
color_image = cv2.imread("colorretriever.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("grayretriever.jpg")
Color_image = cv2.imread("colorretriever.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
### Histogram Equalization of Grayscale Image.
```
import cv2
gray_image = cv2.imread("grayretriever.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/bfc872da-5bfa-4f72-8270-58c2342a96a5)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/a8d0ad01-a09a-413d-9f8f-4bd765b68db8)
![image](https://github.com/user-attachments/assets/2e38ab44-ca5f-48a9-a861-822933e44c4a)
![image](https://github.com/user-attachments/assets/f22126f6-db44-4d71-bcbe-4345614482b5)
![image](https://github.com/user-attachments/assets/76c1dc3e-6843-4a02-9f7f-463a38e7735d)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/89261761-a53f-4bcf-8a8c-0efa016d07ea)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
