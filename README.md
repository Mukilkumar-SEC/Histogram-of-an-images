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
# Developed By: Mukil kumar v
# Register Number: 212222230087


```python
import cv2
import matplotlib.pyplot as plt
```
## Write your code to find the histogram of gray scale image and color image channels.

### Gray Image

hist = cv2.calcHist([gray_image],[0],None,[256],[0,255])
```
### Color Image 

#### Chanel Blue
```python
h1 = cv2.calcHist([color_image],[0],None,[256],[0,255]) 
```
#### Chanel Green
```python
h2 = cv2.calcHist([color_image],[1],None,[256],[0,255]) 
```
#### Chanel Red
```python
h3 = cv2.calcHist([color_image],[2],None,[256],[0,255]) 
```

## Display the histogram of gray scale image and any one channel histogram from color image

### Gray Image
```python
import cv2
import matplotlib.pyplot as plt
gray_image =cv2.imread('E640.png',0)
cv2.imshow('gray_image',gray_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
```
### Color Image
```python
import cv2
import matplotlib.pyplot as plt
color_image =cv2.imread('C640.png',-1)
cv2.imshow('color_image',color_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
```

## Write the code to perform histogram equalization of the image.
```python
equ_img = cv2.equalizeHist(gray_image)
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/b197f787-6a49-474f-9c17-b21c01b5e38a)
![image](https://github.com/user-attachments/assets/597fe1d8-0503-4f98-8ce2-98fef417fb44)


### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/user-attachments/assets/794f0c46-be67-40c8-b29f-75247e95d480)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/30c676b0-2436-468d-a3b3-bf17b8c54ef8)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
