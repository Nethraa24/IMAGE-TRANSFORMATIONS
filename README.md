# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value.

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

### Step6:
Rotate the image using angle function.
## Program:
```python
Developed By: J NETHRAA
Register Number: 212222100031
```

### i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("dhanush.jpg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/df47370a-5469-4976-acfd-1a1f27f407ab)

![4a](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/6d9276e5-9d0e-46dd-ae88-d704ef111005)

![4b](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/873e9c21-0aaf-4745-9645-272ca5b73281)


### ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dhanush.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/177f9fa4-020b-46db-98ec-9c74fe73d7ab)

![4b1](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/86ed795e-26b8-4174-a7c7-cff96ec366f4)

![4b2](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/e2010ed4-9ba3-480e-afa8-8b465e470270)

### iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dhanush.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/69cd719f-0559-4d4f-aa6f-15a78319ecc8)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/e56bc6ef-c31a-48bc-b0ef-55dc6cf40d51)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/5d9c9a4b-6a6c-4261-bdca-4b87dd6e9ae1)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/dc5498d0-feac-4f92-968e-ae06a361e1a2)


### iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dhanush.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/6d909d06-89fc-469a-9379-3cfc95abe739)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/26860bd5-268d-425c-b474-ffce2364b80f)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/444750ad-842f-4c85-a64c-3d5502a5943c)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/82595bd1-d647-4cb1-936d-aa24628250b3)

### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dhanush.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/95b017bc-fa46-42ea-8a31-e5126060fc08)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/b6f1fe1f-361a-4fd3-939b-714f577cf08b)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/43d3bdeb-ff96-4694-98ee-cf1898f4592e)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/1956f42d-5b24-43b0-b8be-a7ddf2b5e985)

### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dhanush.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/37a4c9c2-6429-453a-8051-76f1f72ace76)

![image](https://github.com/Nethraa24/IMAGE-TRANSFORMATIONS/assets/121215786/29f52314-8a38-40e9-9758-3a9a0f6f11a2)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
