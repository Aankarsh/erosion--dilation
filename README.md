## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step-1:
Create a black image of size 100x600 pixels.

## Step-2:
Use a specified font to write the word "Lifestyle" on the image at a defined position.

## Step-3:
Show the image containing the text without axis labels.

## Step-4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).

## Step-5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.

## Step-6:
Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
## Program:
### DEVELOPED BY : AANKARSH J
### REG NO : 212223233001

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background (RGB: 0, 0, 0)
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text (RGB: 255, 255, 255)
cv2.putText(img, 'JANARTHANAN K', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```


# Create the structuring element

```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
## Output:

### Display the input Image
<br>
<br>
<img width="515" height="102" alt="download" src="https://github.com/user-attachments/assets/825ed548-bb14-4080-ae74-411b3fb0811a" />


<br>
<br>
<br>

### Display the structured elements
<br>
<br>
<img width="339" height="716" alt="image" src="https://github.com/user-attachments/assets/27094d89-a8f8-4105-9fa0-f54322c55c8e" />


<br>
<br>
<br>


### Display the Eroded Image
<br>
<br>

<img width="515" height="102" alt="download" src="https://github.com/user-attachments/assets/b66d5a37-3080-42b8-a8be-d3f20892863d" />


<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>


<img width="515" height="102" alt="download" src="https://github.com/user-attachments/assets/38813f05-fdb1-42c7-bf37-4250da8f8378" />



<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
