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
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation



 
## Program:

``` Python

# Name:Dhivya Dharshini B
# Reg no :212223240031
import cv2
import numpy as np
import matplotlib.pyplot as plt

# 1. Setup: Create a black image and draw white text
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Dhivya', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
kernel = np.ones((3, 3), np.uint8)

# 2. Perform Morphological Operations (The missing code)
# Opening operation: useful for removing small white noise
open_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Closing operation: useful for filling small holes in objects
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# 3. Plotting
plt.figure(figsize=(12, 4))

# Subplot 1: Input Image
plt.subplot(1, 3, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image")
plt.axis('off')

# Subplot 2: Opening Operation
plt.subplot(1, 3, 2)
plt.imshow(cv2.cvtColor(open_image, cv2.COLOR_BGR2RGB))
plt.title("Opening Operation")
plt.axis('off')

# Subplot 3: Closing Operation
plt.subplot(1, 3, 3)
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))
plt.title("Closing Operation")
plt.axis('off')

plt.tight_layout()
plt.show() # Use plt.show() to display the plot in an interactive environment



```
## Output:

### Display the input Image
<img width="234" height="237" alt="image" src="https://github.com/user-attachments/assets/2d03cfe0-4ceb-49c7-a0eb-60211c54d88c" />


### Display the result of Opening
<img width="225" height="239" alt="image" src="https://github.com/user-attachments/assets/7f69c621-a623-4f0b-acb6-6060e12d6127" />


### Display the result of Closing
<img width="222" height="236" alt="image" src="https://github.com/user-attachments/assets/d55881a6-e7e9-4c94-a563-5eeb2aad7565" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
