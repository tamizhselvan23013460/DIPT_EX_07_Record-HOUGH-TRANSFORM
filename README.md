
# Name : Tamizhselvan B
# Reg.no : 212223230225
# Exp.No : 7 ( Record-HOUGH TRANSFORM )

# Edge-Linking-using-Hough-Transformm
# Aim:
To write a Python program to detect the lines using Hough Transform.

# Software Required:
Anaconda - Python 3.7

# Algorithm:
## Step1:
Import all the necessary modules for the program.

## Step2:
Load a image using imread() from cv2 module.

## Step3:
Convert the image to grayscale.

## Step4:
Using Canny operator from cv2,detect the edges of the image.

## Step5:
Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.


# Program : 
```py

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 2: Load the image using imread() from cv2 module
image = cv2.imread('Tamizh.jpeg')  # Replace 'image.jpg' with your image path

# Step 3: Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Input image and grayscale image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert image to RGB for displaying
plt.title("Input Image")
plt.axis('off')
plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

# Using Canny operator from cv2, detect the edges of the image
edges = cv2.Canny(gray_image, 50, 150)  # Canny edge detection with threshold values 50 and 150
# Canny Edge Detector output
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')


# Draw detected lines on the original image

for line in lines:
    x1, y1, x2, y2 = line
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)

plt.figure(figsize=(10, 6))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Detected Lines")
plt.axis('off')
plt.show()




```

# Output
## Input image and grayscale image

<img width="360" height="425" alt="image" src="https://github.com/user-attachments/assets/4216f0bb-2a95-4013-9796-c5d83a2339d5" />
<img width="590" height="457" alt="image" src="https://github.com/user-attachments/assets/fa024f9d-0221-4c72-a86c-f37da1098c18" />


## Canny Edge detector output

<img width="577" height="448" alt="image" src="https://github.com/user-attachments/assets/e04fe10f-4c49-4965-a737-09f5bc6912e7" />


## Display the result of Hough transform

<img width="415" height="519" alt="image" src="https://github.com/user-attachments/assets/854baffb-9ab9-4b96-9743-e79c02bf7a4a" />




# Result :
The edges and significant lines in the given image were successfully detected using the Canny Edge Detector and Hough Transform.
