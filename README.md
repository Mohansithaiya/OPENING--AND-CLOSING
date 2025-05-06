# OPENING--CLOSING
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
 
## Program:
```
DEVELOPED BY: MOHAN S
REGISTER NO: 212223240094
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((600,600), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='MOHAN', org=(50, 300), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img):
    fig=plt.figure(figsize=(12,10))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()

img = load_img()
display_img(img)
```
### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (12,12))
```
### Use Opening operation
```python
image=load_img()
opening_img = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
display_img(opening_img)
```
### Use Closing Operation
```python
image=load_img()
closing_img = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
display_img(closing_img)
```
## Output:

### Display the input Image

![Screenshot 2025-05-06 091414](https://github.com/user-attachments/assets/7cf535f2-9be8-4c09-a5a0-9a705671f01c)


### Display the result of Opening

![Screenshot 2025-05-06 091429](https://github.com/user-attachments/assets/57f75c95-b33a-4f80-9fa8-73389eb08e69)


### Display the result of Closing

![Screenshot 2025-05-06 091439](https://github.com/user-attachments/assets/b94d53b6-b90a-434e-8125-734d0bf7c240)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
