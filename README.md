# OPENING--AND-CLOSING
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
### Name: Arunmozhi Varman T
### Register Number: 212223230022
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((300,700), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='VARMAN', org=(50,200), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img,title="Original Image"):
    fig=plt.figure(figsize=(10,8))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    ax.set_title(title, fontsize=16)
    plt.show()

img = load_img()
display_img(img)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (12,12))

image=load_img()
opening_img = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
display_img(opening_img,"Opening Image")

image=load_img()
closing_img = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
display_img(closing_img,"Closing Image")
```
## Output:
### Display the input Image
![image](https://github.com/user-attachments/assets/afffce7a-d8d2-4a25-a0ff-dda03c289529)


### Display the result of Opening
![image](https://github.com/user-attachments/assets/819ae4ae-50a4-4e98-8064-5025b2d6c430)


### Display the result of Closing
![image](https://github.com/user-attachments/assets/b8d19ec5-7bcd-44d7-ade2-cd72cdfbcab6)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
