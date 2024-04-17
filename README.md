# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary packages
<br>

### Step2:
Create the Text using cv2.putText
<br>

### Step3:
Create the structuring element
<br>

### Step4:
Use Opening operation
<br>

### Step5:
Use Closing Operation
<br>

 
## Program:

``` Python
DEVELOPED BY : A.ANBUSELVAM
REGISTER NO : 212222240009
```

### Import the necessary packages

``` Python
import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText

``` Python
img = np.zeros((100, 400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'ETERNITY !', (5, 70), font, 2, (255), 5, cv2.LINE_AA)
```

### Create the structuring element

``` Python
kernel = np.ones((7, 7), np.uint8)
```

### Use Opening operation

``` Python
imgOpening = cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
```

### Use Closing Operation

``` Python
imgClosing = cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
```

### Display Result:

```python
plt.imshow(img, cmap = 'gray')
plt.axis("off")

plt.imshow(imgOpening, cmap = 'gray')
plt.axis("off")

plt.imshow(imgClosing, cmap = 'gray')
plt.axis("off")
```
## Output:

### Display the input Image:

![INPUT](/input.png)
<br>

### Display the result of Opening:

![INPUT](/open.png)
<br>

### Display the result of Closing:

![INPUT](/close.png)
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
