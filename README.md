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
Give the input text using cv2.putText()
### Step3: 
Perform opening operation and display the result
### Step4: 
Similarly, perform closing operation and display the result
### Step5: 
End the program
## Program:
### Developed by : K  MADHAVA REDDY
### Register number : 212223240064
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'PUSHPA',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis('off')


# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")



# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")




```
## Output:

### Display the input Image
![image](https://github.com/Madhavareddy09/OPENING--AND-CLOSING/assets/145742470/7d13c0ce-1ae8-4fdd-b8a1-feae05e444f4)


### Display the result of Opening
![image](https://github.com/Madhavareddy09/OPENING--AND-CLOSING/assets/145742470/be56cb0a-de47-4ff1-9d0f-04b520e62cbf)


### Display the result of Closing
![image](https://github.com/Madhavareddy09/OPENING--AND-CLOSING/assets/145742470/ea3d96dc-5b48-4301-a08c-b55893846103)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
