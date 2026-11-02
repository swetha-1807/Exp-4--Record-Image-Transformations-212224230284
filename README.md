# Exp-4--Record-Image-Transformations-212224230284

## NAME : SWETHA K
## REGISTER NUMBER : 212224230284

## Aim

To write a Python program using OpenCV to perform various geometric transformations on an input image, such as translation, scaling, shearing, reflection, rotation, and cropping, and to observe the changes in the image.

## Algorithm

### Algorithm

Step 1: Import the required libraries such as OpenCV, NumPy, and Matplotlib.

Step 2: Read the input image using `cv2.imread()` and display the original image.

Step 3: Create a translation matrix to move the image horizontally and vertically.

Step 4: Apply image translation using `cv2.warpAffine()` and display the translated image.

Step 5: Resize the image using `cv2.resize()` with different scaling factors to increase and decrease its size.

Step 6: Create a shearing matrix and apply horizontal and vertical shearing using `cv2.warpAffine()`.

Step 7: Perform image reflection using `cv2.flip()` to flip the image horizontally, vertically, and along both axes.

Step 8: Create a rotation matrix using `cv2.getRotationMatrix2D()` and rotate the image by the required angle.

Step 9: Crop a specific portion of the image using array slicing by specifying the required coordinates, width, and height.

Step 10: Display all the transformed images using Matplotlib and compare them with the original image.

## Program 

```

import cv2
import numpy as np
import matplotlib.pyplot as plt
