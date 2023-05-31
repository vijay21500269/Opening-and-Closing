# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.




### Step2:
Create the Text using cv2.putText.



### Step3:
Create the structuring element.



### Step4:
Use Opening operation.



### Step5:
Use Closing Operation.

### Step6:
Print the output and end the program.



 
## Program:
~~~
Developed by: Vijay R
Register number: 212221230121
~~~

``` Python
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 7
cv2.putText(text_image," VIJAY ",(3,70),font,3,(240),3,cv2.LINE_AA)
plt.title("ORIGINAL IMAGE")
plt.imshow(text_image)
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))


# Use Opening operation

open_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("OPENING")
plt.imshow(open_image)
plt.axis('off')


# Use Closing Operation


close_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("CLOSING")
plt.imshow(close_image)
plt.axis('off')


```
## Output:

### Display the input Image

![img1]()
### Display the result of Opening
![img2]()

### Display the result of Closing
![img3]()

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
