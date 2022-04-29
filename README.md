# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
#Developed By: Dineshkumar S
#Register Number: 212220230012
#Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
pic=cv2.imread("hot air baloon.jpg")
pic=cv2.cvtColor(pic,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(pic)
plt.show()
r,c,d=pic.shape
M = np.float32([[1,0,50],
               [0,1,75],
               [0,0,1]])
translated_img = cv2.warpPerspective(pic,M,(c,r))
plt.axis("off")
plt.imshow(translated_img)
plt.show()

#Image Scaling
M = np.float32([[1.5,0,0],
               [0,1.5,0],
               [0,0,1]])
scaled_img = cv2.warpPerspective(pic,M,(c*2,r*2))
plt.axis("off")
plt.imshow(scaled_img)
plt.show()

#Image shearing
M_x = np.float32([[1,0.5,0],
                 [0,1,0],
                 [0,0,1]])
M_y = np.float32([[1,0,0],
                 [0.25,1,0],
                 [0,0,1]])
sheared_img_x = cv2.warpPerspective(pic,M_x,(int(c*1.5),int(r*1.5)))
sheared_img_y = cv2.warpPerspective(pic,M_y,(int(c*1.5),int(r*1.5)))
plt.axis("off")
plt.imshow(sheared_img_x)
plt.show()
plt.axis("off")
plt.imshow(sheared_img_y)
plt.show()

#Image Reflection
M_x = np.float32([[1,0,0],
                 [0,-1,r],
                 [0,0,1]])
M_y = np.float32([[-1,0,c],
                 [0,1,0],
                 [0,0,1]])
reflected_img_x = cv2.warpPerspective(pic,M_x,(int(c),int(r)))
reflected_img_y = cv2.warpPerspective(pic,M_y,(int(c),int(r)))
plt.axis("off")
plt.imshow(reflected_img_x)
plt.show()
plt.axis("off")
plt.imshow(reflected_img_y)
plt.show()

#Image Rotation
angle = np.radians(25)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
                [np.sin(angle),np.cos(angle),0],
                [0,0,1]])
rotated_img = cv2.warpPerspective(pic,M,(int(c),int(r)))
plt.axis("off")
plt.imshow(rotated_img)
plt.show()

#Image Cropping
cropped_img = pic[100:400,300:500]
plt.axis("off")
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![Screenshot (51)](https://user-images.githubusercontent.com/75234807/165893140-d7bea756-434c-42fa-ba7c-5808b9f0b7fb.png)

### ii) Image Scaling
![Screenshot (52)](https://user-images.githubusercontent.com/75234807/165893168-0da7fb4b-2364-4815-9e54-bc0775f63260.png)

### iii)Image shearing
![Screenshot (67)](https://user-images.githubusercontent.com/75234807/165893215-e503fa1e-7a69-4f61-a7a1-a65fd9cc8950.png)

### iv)Image Reflection
![Screenshot (68)](https://user-images.githubusercontent.com/75234807/165893178-99414d5e-9de8-4d3b-9f40-cc1c893061e4.png)

### v)Image Rotation
![Screenshot (69)1](https://user-images.githubusercontent.com/75234807/165893186-2476575b-7198-421f-ae86-4edf38c147e5.png)

### vi)Image Cropping
![Screenshot (69)](https://user-images.githubusercontent.com/75234807/165893192-355a4205-955d-4ad9-b122-b2f2d5293cd3.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
