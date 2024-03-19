# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
### Step2:
Load the image file in the program.
### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
### Step4:
Display the modified image output.
### Step5:
End the program.

## Program:
```python
Developed By: SIVABALAN S
Register Number: 212222240100
```
i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sea.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,20],
               [0,1,10],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sea.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows, cols, dims = input_image.shape
M = np.float32([[1.5,0,0],
               [0,1.8,0],
               [0,0,1]])
scaled_image = cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```


iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sea.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
M_x = np.float32([[1,0.5,0],
                 [0,1,0],
                 [0,0,1]])
M_y = np.float32([[1,0,0],
                 [0.5,1,0],
                 [0,0,1]])
shared_image_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols*1.5),int(rows*1.5)))
shared_image_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(shared_image_xaxis)
plt.show()
plt.axis('off')
plt.imshow(shared_image_yaxis)
plt.show()
```
iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sea.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows,cols,dim = input_image.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x = cv2.warpPerspective(input_image,M_x,(int(cols),int(rows)))
reflect_y = cv2.warpPerspective(input_image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()
```

v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sea.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows,cols,dim = input_image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 
```

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sea.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.imshow(input_image)
plt.show()
cropped_img=input_image[50:200 ,50:500]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### Original Image
![sea](https://github.com/sivabalan28/IMAGE-TRANSFORMATIONS/assets/113497347/f8274680-e2fc-4a70-806b-23b1b1669125)

### i)Image Translation
![transl](https://github.com/sivabalan28/IMAGE-TRANSFORMATIONS/assets/113497347/9587337d-1c58-489e-b3a2-436a52c8972b)


### ii) Image Scaling
![WhatsApp Image 2024-03-19 at 11 32 27_6b4476b0](https://github.com/sivabalan28/IMAGE-TRANSFORMATIONS/assets/113497347/812c5529-93e9-48b4-b13f-cb22ea544b64)

### iii)Image shearing
![WhatsApp Image 2024-03-19 at 11 32 28_a80deb41](https://github.com/sivabalan28/IMAGE-TRANSFORMATIONS/assets/113497347/5fba3fc8-e21c-4dbf-bf91-4295d96fb342)

### iv)Image Reflection
![WhatsApp Image 2024-03-19 at 11 32 28_6e446d8b](https://github.com/sivabalan28/IMAGE-TRANSFORMATIONS/assets/113497347/7158a231-5057-44cf-b364-993ca8d05f5d)

### v)Image Rotation
![WhatsApp Image 2024-03-19 at 11 32 29_d741bcc8](https://github.com/sivabalan28/IMAGE-TRANSFORMATIONS/assets/113497347/fd0c3181-a4ab-4895-89f4-af3b2397a538)

### vi)Image Cropping
![WhatsApp Image 2024-03-19 at 11 32 28_79a40964](https://github.com/sivabalan28/IMAGE-TRANSFORMATIONS/assets/113497347/d096f44e-b60f-448a-8979-1de10fbf6fb3)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
