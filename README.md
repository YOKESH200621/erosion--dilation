
```
Developed by : YOKESH I
Register no  : 212224230313 
```

# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale.
### Step2:
Define a structuring element (kernel) for morphological operations.
### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.
### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.
### Step5:
Display and compare the original, eroded, and dilated images.
 
## Program:
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Good Morning', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```

# Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```

# Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/0b5cd778-5e41-42e1-b883-c8c76727fc71)

### Display the Eroded Image

![image](https://github.com/user-attachments/assets/1b4fb613-3cba-4bda-8f7f-7a43d553fb72)

### Display the Dilated Image

![image](https://github.com/user-attachments/assets/7f46c73f-999e-43bb-a834-24df3d03a339)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
