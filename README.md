# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Initialize a blank image and add text to it using cv2.putText().

### Step2:
Create a kernel (structuring element) using np.ones() which defines the size and shape for erosion and dilation.

### Step3:
Use cv2.erode() to shrink or thin out the white areas (text) of the image.

### Step4:
Use cv2.dilate() to expand or thicken the white areas (text) of the image.

### Step5:
Show the original, eroded, and dilated images (using cv2.imshow() or save them with cv2.imwrite()).

## Program:
```
Developed by : RIYA P L
Reg no : 212223240141
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Riya',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')

# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![Screenshot 2024-10-24 152618](https://github.com/user-attachments/assets/55791e8f-ade6-4be6-961b-f4a556f20d05)

### Display the Eroded Image
![Screenshot 2024-10-24 152631](https://github.com/user-attachments/assets/a0db6054-f2d8-4c18-b98c-15fa203ddedf)

### Display the Dilated Image
![Screenshot 2024-10-24 152640](https://github.com/user-attachments/assets/0af802da-2659-4e0d-ba91-2f27f6c30d83)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
