# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>


### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

 
## Program:
  Name: shaiklahir
  
  Register Number:212224240148
# Import the necessary packages
```
import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```



# Create the structuring element
```
kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


# Erode the image

```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode, cmap = 'gray')
plt.axis("off")
```


# Dilate the image

```

img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate, cmap = 'gray')
plt.axis("off")
```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/a3a09319-a257-4163-9076-342ce9ffea4b)


### Display the Eroded Image
![WhatsApp Image 2025-04-30 at 00 34 25_f6743555](https://github.com/user-attachments/assets/bcdfd915-0707-476a-8dd0-abbd7061a27b)


### Display the Dilated Image
![WhatsApp Image 2025-04-30 at 00 35 05_ef638ba6](https://github.com/user-attachments/assets/30b33622-b07a-43bd-95c7-187527f1c026)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
