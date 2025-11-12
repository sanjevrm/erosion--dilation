# NAME: SANJEV R M
# REG NO: 212223040186
# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'GOOD EVENING', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image
<img width="450" height="458" alt="Screenshot 2025-10-07 160850" src="https://github.com/user-attachments/assets/7286bda4-dd62-491a-bd54-ce1a8fd8b256" />


### Display the Eroded Image
<img width="447" height="463" alt="Screenshot 2025-10-07 160857" src="https://github.com/user-attachments/assets/63346439-8d21-4339-aaf3-f485943b9b83" />


### Display the Dilated Image
<img width="448" height="456" alt="Screenshot 2025-10-07 160903" src="https://github.com/user-attachments/assets/08aff14d-2f5c-4018-ad7b-ff2716db1ef2" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
