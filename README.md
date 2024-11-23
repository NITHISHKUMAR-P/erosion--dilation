# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).

### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.

### Step4:
Display the eroded image using cv2.imshow.

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
 
## Program:
```
DEVELOPED BY: Nithishkumar P
REG NO: 212221230070
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'NITHISHKUMAR P', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
### Create the structuring element
```
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
```
### Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
### Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/753d2a45-3caf-4059-b674-fcd86c9cc3f6)



### Display the Eroded Image

![image](https://github.com/user-attachments/assets/dcd4aa48-5544-45b4-b131-3a4b694b699b)



### Display the Dilated Image
![image](https://github.com/user-attachments/assets/444dd9b5-150b-47c0-8ec6-37ee011cfe14)





## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
