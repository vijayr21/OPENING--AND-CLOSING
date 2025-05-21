# OPENING--AND-CLOSING
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
#NAME:Dakshata G
#REG NO:212223240021
import cv2
import numpy as np
import matplotlib.pyplot as plt

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Dakshata",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image

![WhatsApp Image 2025-05-21 at 15 06 53_e008609e](https://github.com/user-attachments/assets/69795860-38fe-4364-bf6e-b4d292aee235)




### Display the result of Opening

![WhatsApp Image 2025-05-21 at 15 06 53_0865490f](https://github.com/user-attachments/assets/f6ac8562-63ad-4964-b48d-1a5dcaf100be)





### Display the result of Closing


![WhatsApp Image 2025-05-21 at 15 06 54_7ecbdaac](https://github.com/user-attachments/assets/b62efe27-a226-401a-b272-b653bfd1b9f5)





## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
