# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>Import the required libraries: OpenCV (cv2), NumPy, and Matplotlib for image processing and visualization.


### Step2:
<br>Create a blank black image (500×500) and add the text "Open and Close" using cv2.putText().

### Step3:
<br>
Create a 3×3 kernel (matrix of ones) to be used for morphological operations.
### Step4:
<br>Display the original image and apply Opening operation (cv2.MORPH_OPEN), which performs erosion followed by dilation.

### Step5:
<br>
Apply Closing operation (cv2.MORPH_CLOSE), which performs dilation followed by erosion, and display the processed image.
 
## Program:

``` Python
## OPENING--AND-CLOSING
### DEVELOPED BY : VENKATA MOHAN N
### REG NO : 212224230298
     

# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Open and Close', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)




# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')



# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)


# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')


# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Output:

### Display the input Image
<br>
<br>
<br>
<br><img width="552" height="521" alt="image" src="https://github.com/user-attachments/assets/801e146d-b94c-470a-a45d-8c8dbc579a74" />

<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
<br>
<br><img width="562" height="510" alt="image" src="https://github.com/user-attachments/assets/7350b2c7-4799-4a82-8ca5-73adbe06d989" />

<br>

### Display the result of Closing
<br>
<br>
<br>
<br><img width="1087" height="147" alt="image" src="https://github.com/user-attachments/assets/01d8ea87-696e-41f3-a894-461d2ce4216f" />

<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
