# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate  the image

 
## Program:
```
DEVELOPED BY: ARSHATHA.P
REGISTER NO.: 212222230012
```

###  Import the necessary packages
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```py
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"ARSHA",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```
###  Create the structuring element
```py
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
plt.imshow(img)
plt.axis('off')
```
### Erode the image
```py
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
### Dilate the image
```py
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image:
![image](https://github.com/arshatha-palanivel/erosion--dilation/assets/118682484/7146580c-c30a-4c8f-9ff2-0ae3f509bea1)



### Display the Eroded Image:
![image](https://github.com/arshatha-palanivel/erosion--dilation/assets/118682484/4665ece6-9ba5-485d-85f4-161b7f6a94fa)



### Display the Dilated Image:
![image](https://github.com/arshatha-palanivel/erosion--dilation/assets/118682484/04a1c971-ec47-43b9-ad03-dc7914b7edbb)



### Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
