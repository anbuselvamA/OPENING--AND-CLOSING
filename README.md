# OPENING-AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages
### Step2:
Create the Text using cv2.putText
### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

## Program:
```
Developed by: SUDHAKAR K
Register Number:212222240107
```
### Display the input Image
```py
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'HAKUNA MATATA', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
### Create the structured element
```py
struct_ele = np.ones((9, 9), np.uint8)
```
### Display the result of Opening
```py
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
### Display the result of Closing
```py
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
## Output:

### Display the input Image


![Screenshot 2024-04-17 090032](https://github.com/Sudhakaroffical/OPENING--AND-CLOSING/assets/118622513/bad781f7-6480-42d1-aa26-5f746f71e721)


### Display the result of Opening
![Screenshot 2024-04-17 090148](https://github.com/Sudhakaroffical/OPENING--AND-CLOSING/assets/118622513/2464d703-8c36-4282-b2f1-5d8c90ae27bd)


### Display the result of Closing
![Screenshot 2024-04-17 090148](https://github.com/Sudhakaroffical/OPENING--AND-CLOSING/assets/118622513/979f37f9-547b-4cd7-bce4-ab3dfc1bd79d)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
