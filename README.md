# Exp-4--Record-Image-Transformations-212224230284

## NAME : SWETHA K
## REGISTER NUMBER : 212224230284

## Aim

To write a Python program using OpenCV to perform various geometric transformations on an input image, such as translation, scaling, shearing, reflection, rotation, and cropping, and to observe the changes in the image.

## Software Used

Anaconda – Python 3.7

Jupyter Notebook / VS Code

OpenCV (cv2)

NumPy

Matplotlib


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

## Developed By: SWETHA K
## Register No: 212224230284

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread(r'C:\Users\admin\Downloads\my photo dipt.jpeg')  
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")  
plt.axis('off')

tx, ty = 100, 50  
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))

plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  
plt.title("Translated Image")  
plt.axis('off')

fx, fy = 5.0, 2.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))
plt.title("Scaled Image")  
plt.axis('off')

shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))

plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))  
plt.title("Sheared Image") 
plt.axis('off')

reflected_image = cv2.flip(image, 2)

plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB)) 
plt.title("Reflected Image")  
plt.axis('off')

(height, width) = image.shape[:2] 
angle = 45  
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)  
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))  

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))  
plt.title("Rotated Image")  
plt.axis('off')

x, y, w, h = 100, 100, 200, 150
cropped_image = image[y:y+h, x:x+w]

plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image")  
plt.axis('off')
```

## Output:

## Original Image

<img width="782" height="562" alt="image" src="https://github.com/user-attachments/assets/098a3d3c-eb29-4cab-9e67-75716519ae8e" />

## Image Translation

<img width="767" height="552" alt="image" src="https://github.com/user-attachments/assets/fd4e646d-ec05-4aed-8fa5-e52fddba7cfc" />

## Image Scaling

<img width="822" height="410" alt="image" src="https://github.com/user-attachments/assets/362ce4a5-f41c-4ee1-89c4-a83033675ea8" />

## Image Shearing

<img width="770" height="562" alt="image" src="https://github.com/user-attachments/assets/160a0c3a-84db-424f-a1a8-18d10ddc5b58" />

## Image Reflection

<img width="742" height="550" alt="image" src="https://github.com/user-attachments/assets/2f25b3ac-50e6-42d4-91c4-57be4e61b970" />

## Image Rotation

<img width="737" height="547" alt="image" src="https://github.com/user-attachments/assets/9abd6dad-722c-4977-87a4-9a89a443e60b" />

## Cropped Image

<img width="820" height="553" alt="image" src="https://github.com/user-attachments/assets/bcee7147-4579-498e-a21f-25991fb68871" />

## Result

Thus, various geometric transformations such as translation, scaling, shearing, reflection, and rotation are successfully performed using OpenCV. These transformations demonstrate how images can be spatially manipulated for different computer vision applications.
