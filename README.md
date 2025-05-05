# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7

## Algorithm:
Step 1: Import the necessary packages.
Step 2: Create a black image and apply white text using cv2.putText.
Step 3: Define structuring elements (kernels) for morphological operations.
Step 4: Perform erosion on the image using cv2.erode.
Step 5: Perform dilation on the image using cv2.dilate.

## Program:
python
```
# Step 1: Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Step 2: Create the Text using cv2.putText
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text
cv2.putText(img, 'LAHIR', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)

# Display the input Image
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Input Image")
plt.axis('off')
plt.show()

# Step 3: Create the structuring element
kernel = np.ones((5, 5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS, (5, 5))

# Step 4: Erode the image
img_erode = cv2.erode(img, kernel1)

# Display the Eroded Image
plt.imshow(cv2.cvtColor(img_erode, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
plt.show()

# Step 5: Dilate the image
img_dilate = cv2.dilate(img, kernel1)

# Display the Dilated Image
plt.imshow(cv2.cvtColor(img_dilate, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
plt.show()
```
## Output:

***Display the Input Image***

![image](https://github.com/user-attachments/assets/cb3836d6-54b7-441d-86db-4726ed85e768)



***Display the Eroded Image***

![image](https://github.com/user-attachments/assets/e9ebed09-c466-4f6e-ad96-b1e6ef66549e)


***Display the Dilated Image***

![image](https://github.com/user-attachments/assets/7588b0a8-dff8-40da-8d71-ce87ddabb3db)




## Result
Thus, the generated text image was successfully eroded and dilated using Python and OpenCV.
