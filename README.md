# OPENING AND CLOSING
## AIM:
To implement Opening and Closing using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

## PROGRAM:
```python
/*
Developed by   : Lokesh Krishnaa M
Register Number: 212220230030
*/
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
img=np.zeros((100,600),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Lokesh Krishnaa M',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()
# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()
# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()
```
## OUTPUT:
### Display the input Image
![lok](https://user-images.githubusercontent.com/75234646/172284030-7871299d-8902-4549-b3ca-4ff4cf4d47de.png)
### Display the result of Opening:
![lok 2](https://user-images.githubusercontent.com/75234646/172284038-d241361d-191c-4fb0-b2a5-90a6e5cde8d7.png)
### Display the result of Closing
![lok3](https://user-images.githubusercontent.com/75234646/172284051-c3c1b88d-444d-40b1-9a60-f645c167d0cc.png)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
