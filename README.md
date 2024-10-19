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
# Create a blank image (100 pixels high, 400 pixels wide)
img = np.zeros((100, 400), dtype='uint8')

# Create the Text using cv2.putText
cv2.putText(img, 'Riya', (60, 70), cv2.FONT_HERSHEY_SIMPLEX, 2, (255), 5)
cv2.imshow("Original Image" , img)

# Create the structuring element
kernel = np.ones((5, 5), np.uint8)

# Erode the image
eroded_img = cv2.erode(img, kernel, iterations=1)
cv2.imshow("Eroded Image" ,eroded_img)

# Dilate the image
dilated_img = cv2.dilate(img, kernel, iterations=1)
cv2.imshow("Dilated Image" , dilated_img)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
![Screenshot 2024-10-19 085805](https://github.com/user-attachments/assets/5b5b643f-caae-4b59-9e5e-810c1681164f)

### Display the Eroded Image
![Screenshot 2024-10-19 085821](https://github.com/user-attachments/assets/3ae0d1df-dff1-4176-862d-6ce664f342ca)

### Display the Dilated Image
![Screenshot 2024-10-19 085834](https://github.com/user-attachments/assets/e0ce41e3-4425-4993-8005-7eb1afc21703)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
