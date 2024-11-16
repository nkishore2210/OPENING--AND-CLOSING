# EX-10:OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:Read the Image:
Load the input color image from a specified path.

### Step-2:Convert to Grayscale:
Transform the color image into a grayscale format for easier processing.

### Step-3:Edge Detection:
Apply an edge detection technique to identify the prominent edges in the grayscale image.

### Step-4:Create Structuring Element:
Define a kernel (structuring element) for use in morphological operations, typically a matrix of ones.

### Step-6:Morphological Operations:
Perform morphological operations:<br>
Opening: Remove small objects from the edges to clean up the image.<br>
Closing: Fill small holes in the detected edges to enhance the structure.

### Step-7:Display Results:
Show the original grayscale image, along with the results of the opening and closing operations for visual comparison.

## Program:

### Developed By : KISHORE N
### Register Number: 212222240049

### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the structuring element
```python
image = cv2.imread("FISH_1.jpg")  
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
![Screenshot 2024-11-16 220423](https://github.com/user-attachments/assets/e85dc3b9-ceab-4b23-8325-a02ee688883e)

### Use Opening operation
```python
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
![Screenshot 2024-11-16 220432](https://github.com/user-attachments/assets/35e0d500-e713-4bf6-86a4-8d7d67cf38ce)

### Use Closing Operation
```python
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
![Screenshot 2024-11-16 220438](https://github.com/user-attachments/assets/29d7e3d0-1de7-4a63-ac19-4cd2d63bb318)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
