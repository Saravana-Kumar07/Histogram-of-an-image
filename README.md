# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot packages.

### Step2:
Read the images using imread()function.

### Step3:
Using cv2.calcHist find Histogram of the images.

### Step4:
Using cv2.equalizeHist find Equalization of Histogram.

### Step5:
Run the program and execute the output.

## Program:
```python
# Developed By: Saravana Kumar.S
# Register Number:21005866

# Write and display your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
gray_image=cv2.imread('gray.jpg')
color_image=cv2.imread('color.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1=cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.title('Histogram of color image - Green channel')
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image. 
import cv2
g=cv2.imread('eq.png',0)
cv2.imshow('gray',g)
equ = cv2.equalizeHist(g)
cv2.imshow('Equalized image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![output](./out1.png)

### Histogram of Grayscale Image and any channel of Color Image
![output](./out2.png)

### Histogram Equalization of Grayscale Image
![output](./out3.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
