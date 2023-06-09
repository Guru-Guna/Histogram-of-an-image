# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.<br>


### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.<br>

### Step3:
Display the histograms with their respective images.<br>

### Step4:
Equalize the grayscale image.<br>

### Step5:
Display the grayscale image.<br>

## Program:


#### Developed By: Gunaseelan G
#### Register Number: 212221230031

```python
import cv2
import matplotlib.pyplot as plt
```
## Write your code to find the histogram of gray scale image and color image channels.

### Gray Image
```python
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
gray_image =cv2.imread('jawa.png',0)
cv2.imshow('gray_image',gray_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
```
### Color Image
```python
import cv2
import matplotlib.pyplot as plt
color_image =cv2.imread('jawa.png',-1)
cv2.imshow('color_image',color_image) 
cv2.waitKey(0) 
cv2.destroyAllWindows()
```


## Write the code to perform histogram equalization of the image.
```python
equ_img = cv2.equalizeHist(gray_image)
```
# Output:
## Input Grayscale Image and Color Image

<br>![](gray_image_G.png)<br>
<br>![](color_image_G.png)<br>


## Histogram of Grayscale Image and any channel of Color Image
#### Grey Image
![1](https://github.com/Guru-Guna/Histogram-of-an-image/assets/93427255/622e1f8f-f28e-47fc-a7e5-d734be625d43)

#### Blue Channel
![2](https://github.com/Guru-Guna/Histogram-of-an-image/assets/93427255/a28fd4df-5479-4f11-9c6b-42b4ef94d077)

#### Green Channel
![3](https://github.com/Guru-Guna/Histogram-of-an-image/assets/93427255/d17541d1-410b-4607-9bc2-8f749e639e19)

#### Red Channel

![4](https://github.com/Guru-Guna/Histogram-of-an-image/assets/93427255/d63759dd-2b1b-4450-b91a-d7f8a4295c81)

## Histogram Equalization of Grayscale Image

![5](https://github.com/Guru-Guna/Histogram-of-an-image/assets/93427255/0f527afc-f05c-48ac-aee3-3313215beb27)


# Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
