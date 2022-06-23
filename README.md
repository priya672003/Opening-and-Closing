### EX.NO : 11

### DATE : 

# <p align="center"> Opening-and-Closing </p> 

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the text image using cv2.putText.

### Step3:

Then create the structuring element for opening and closing

### Step4:

Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:

Plot the images using plt.imshow.

 
## Program:
```python3
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Priya",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')


# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
## Output:

### Display the input Image

![image](https://user-images.githubusercontent.com/81132849/170862863-7519bde6-e640-4f8e-9483-2007d99480cc.png)


### Display the result of Opening

![image](https://user-images.githubusercontent.com/81132849/170862868-b49b83cf-d21d-4ca0-ae59-382de435d5cb.png)


### Display the result of Closing

![image](https://user-images.githubusercontent.com/81132849/170862874-3ff483fd-c41a-4ee9-8880-6d907b5aa099.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
