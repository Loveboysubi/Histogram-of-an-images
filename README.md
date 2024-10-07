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
# Developed By: SUBISHESH P
# Register Number: 212223230220
```
```
# Developed By: RIYA P L
# Register Number: 212223240141
## Input Grayscale Image and Color Image:
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray_image.jpg")
color_image = cv2.imread("color_image.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

## Histogram of Grayscale Image and any channel of Color Image
import cv2
Gray_image = cv2.imread("gray_image.jpg")
Color_image = cv2.imread("color_image.jpg")
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

## Histogram Equalization of Grayscale Image.
import cv2
gray_image = cv2.imread("gray_image.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-10-07 111902](https://github.com/user-attachments/assets/f6ebb699-7e1c-4e09-bfe6-1bd0add118be)

![Screenshot 2024-10-07 111911](https://github.com/user-attachments/assets/f44147c4-4501-4439-ac7d-95982cb5394f)


### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2024-10-07 111946](https://github.com/user-attachments/assets/6a8980f6-60f8-47e7-a54b-e62853e5893d)

![Screenshot 2024-10-07 111958](https://github.com/user-attachments/assets/f82615fd-345e-4125-a0d6-ef9e2d819990)

![Screenshot 2024-10-07 112022](https://github.com/user-attachments/assets/4ac198f4-f6b4-443c-9314-fdbdcc59f693)

![Screenshot 2024-10-07 112029](https://github.com/user-attachments/assets/797ba866-11d7-4a57-bd37-4c11369628f0)

### Histogram Equalization of Grayscale Image.

![Screenshot 2024-10-07 112052](https://github.com/user-attachments/assets/63b8e2d0-01f7-4023-8db4-c53aef6dcbe4)

![Screenshot 2024-10-07 112103](https://github.com/user-attachments/assets/2fc81624-2e7e-45a1-a115-305c75d081bd)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
