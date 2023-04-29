# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages




### Step2:
Create the text image using cv2.putText.



### Step3:
Then create the structuring image for dilation/erosion.



### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.



### Step5:
Plot the images using plt.imshow.



 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np



# Create the Text using cv2.putText
img1 = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'PAVAN',(5,70),font,2,(255),5,cv2.LINE_AA)


# Create the structuring element
cv2.imshow("Name Image",img1)


# Erode the image and Dilate the image

kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
erodeImage = cv2.erode(img1,kernel1)
dilationImage = cv2.dilate(img1,kernel1)
cv2.imshow("Erode Image",erodeImage)
cv2.imshow("Dilated Image",dilationImage)
cv2.waitKey(0)

cv2.destroyAllWindows()



```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/94828517/235294673-f1979f10-cb48-4207-8ec2-96148fe78c68.png)

### Display the Eroded Image
![image](https://user-images.githubusercontent.com/94828517/235294694-5bafea6c-fa03-4810-bfa0-24f01b7e88a1.png)


### Display the Dilated Image
![image](https://user-images.githubusercontent.com/94828517/235294733-ce5f0e23-9fae-49db-97de-065296542833.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
