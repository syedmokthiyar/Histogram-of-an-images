# EX 03 : Histogram-of-an-images
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
# Developed By: Syed Mokthiyar S.M
# Register Number: 212222230156

## Gray Image and Color Image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("Ajith.jpeg")
color_image = cv2.imread("vijay.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

## Histogram of Grayscale Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('Ajith.jpeg')
color_img = cv2.imread('vijay.jpeg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

## Histogram of Color Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('Ajith.jpeg')
color_img = cv2.imread('Vijay.jpeg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

## Histogram Equilization of GrayScale Image
import cv2
gray_img = cv2.imread('Ajith.jpeg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-04-02 214758](https://github.com/syedmokthiyar/Histogram-of-an-images/assets/118787294/76dd4b5b-1717-430a-8c4d-98bdc6657744)

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-04-02 214926](https://github.com/syedmokthiyar/Histogram-of-an-images/assets/118787294/52460d77-d656-4c3c-ab15-11f25143cfef)


### Histogram of Color Image:
![Screenshot 2024-04-02 215901](https://github.com/syedmokthiyar/Histogram-of-an-images/assets/118787294/7011d353-0e69-4e7e-8aaa-c65f7af15191)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-04-02 215327](https://github.com/syedmokthiyar/Histogram-of-an-images/assets/118787294/69f4fedc-7a37-4ae2-bc13-37f37972799f)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
