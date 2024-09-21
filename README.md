# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Load an image from your local directory and display it.

### Step2:
o	Draw a line from the top-left to the bottom-right of the image.

o	Draw a circle at the center of the image.

o	Draw a rectangle around a specific region of interest in the image.

o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.

o	Convert the image from RGB to GRAY and display it.

o	Convert the image from RGB to YCrCb and display it.

o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).

o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.

### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

### Step7:
o	Flip the original image horizontally and display it.

o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.

##### Program:
### Developed By: SRINITHI V
### Register Number: 212222110046

## Output:
### 1.Read and display the image
Load an image from your local directory and display it.
```python
import cv2
import matplotlib.pyplot as plt

image=cv2.imread('i.jpg',1)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.axis('off')  
plt.show()
```
![1](https://github.com/user-attachments/assets/c85d3258-4bb0-4630-b9a7-770a93fd62d5)

### 2.Draw Shapes and Add Text
i) Draw a line from the top-left to the bottom-right of the image.
```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("i.jpg")
img=cv2.resize(img,(400,300))
res = cv2.line(img,(0,0),(400,300),(0, 0, 255),10)
image_rgb = cv2.cvtColor(res, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb) 
plt.axis('off') 
plt.show()
```
![2](https://github.com/user-attachments/assets/c07b8b75-e082-49c5-87a5-88549f5a2ac0)

ii) Draw a circle at the center of the image.
```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("i.jpg")
img=cv2.resize(img,(400,300))
res=cv2.circle(img,(200,150),100,(0, 255, 0),10)
image_rgb = cv2.cvtColor(res, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.axis('off') 
plt.show()
```
![3](https://github.com/user-attachments/assets/0b3d7e04-5d91-4384-b781-63b0c7a5394f)

iii) Draw a rectangle around a specific region of interest in the image.
```python
import cv2
import matplotlib.pyplot as plt

image = cv2.imread("i.jpg")
image = cv2.resize(image, (400, 300))      
res_img = cv2.rectangle(image,(100, 100),(300, 200),(255,0,0),10)
image_rgb = cv2.cvtColor(res_img, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.axis('off') 
plt.show()
```
![4](https://github.com/user-attachments/assets/70629468-bb1d-4443-877f-4811ddab4960)

iv) Add the text "OpenCV Drawing" at the top-left corner of the image.
```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("i.jpg")
res = cv2.putText(img,"OpenCV Drawing",(10, 50) ,cv2.FONT_HERSHEY_SIMPLEX,2,(255, 0, 0) ,3, cv2.LINE_AA)
image_rgb = cv2.cvtColor(res,cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.axis('off')  
plt.show()
```
![5](https://github.com/user-attachments/assets/acb6a46c-7a59-43d7-ab19-1576da96400d)

### 3.Image Color Conversion
i) Convert the image from RGB to HSV and display it
```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("i.jpg")
image_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.imshow(image_rgb)
plt.title('Original RGB Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image_hsv)
plt.title('HSV Image')
plt.axis('off')
plt.show()
```
![6](https://github.com/user-attachments/assets/3e10f45e-4118-4c96-b308-301e50cb636b)

ii) Convert the image from RGB to GRAY and display it.
```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("i.jpg")
image_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.figure(figsize=(10, 5))

plt.subplot(1, 2, 1)
plt.imshow(image_rgb)
plt.title('Original RGB Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image_gray, cmap='gray')
plt.title('Grayscale Image')
plt.axis('off')
plt.show()
```
![7](https://github.com/user-attachments/assets/7ac99224-e490-401d-a6e1-7c2aed228ea9)

iii)Convert the image from RGB to YCrCb and display it.
```python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)

plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.imshow(image_rgb)
plt.title('Original RGB Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(image_ycrcb)
plt.title('YCrCb Image')
plt.axis('off')
plt.show()
```
![8](https://github.com/user-attachments/assets/b890827f-177d-406b-b66a-b67d3da3efaa)

iv) Convert the HSV image back to RGB and display it.
```python
image_rgb_converted=cv2.cvtColor(image_hsv,cv2.COLOR_HSV2RGB)

plt.figure(figsize=(10,5))
plt.subplot(1,2,1)
plt.imshow(image_hsv)
plt.title('HSV Image')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(image_rgb_converted)
plt.title('RGB Image')
plt.axis('off')
plt.show()
```
![9](https://github.com/user-attachments/assets/d2a600b8-00b0-4e0a-8cd0-c72108385a5c)

### 4.Access and Manipulate Image Pixels
i) Access and print the value of the pixel at coordinates (100, 100).
```python
import cv2
image=cv2.imread("i.jpg")
image = cv2.resize(image, (400, 300))  
pixel_value = image[100, 100]
print(f'Pixel value at (100, 100): {pixel_value}')
```
![Screenshot 2024-09-21 183109](https://github.com/user-attachments/assets/5682b79b-8a2e-428d-8649-8a464cefeb9d)

ii) Modify the color of the pixel at (200, 200) to white.
```python
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('i.jpg')
image = cv2.resize(image,(400,300))
image= cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(10,5))
plt.subplot(1,2,1)
plt.imshow(image)
plt.title('ORIGINAL IMAGE')
plt.axis('off')

image[205:210, 205:210] = [255, 255, 255]

plt.subplot(1,2,2)
plt.imshow(image)
plt.title('MODIFIED IMAGE')
plt.axis('off')
```
![10](https://github.com/user-attachments/assets/3b95260c-321b-4829-82ee-f523b15844bb)

### 5.Image Resizing:
```python
import cv2
image = cv2.imread('i.jpg')
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![11](https://github.com/user-attachments/assets/0104fa41-0394-43d5-bb7b-01a99b3c3df4)

### 6.Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```python
import cv2
image = cv2.imread('i.jpg')
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![12](https://github.com/user-attachments/assets/d7502768-860c-4fd7-bb6b-9a2d79a0b415)

### 7.Image Flipping:
i) Flip the original image horizontally and display it.
```python
import cv2
image = cv2.imread("i.jpg")
image = cv2.resize(image,(400,300))
res=cv2.flip(image,1)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![13](https://github.com/user-attachments/assets/0b4a83ff-67b3-4ab0-8246-df2bbfa1047a)

ii) Flip the original image vertically and display it.
```python
import cv2
image = cv2.imread("i.jpg")
image = cv2.resize(image,(400,300))
res=cv2.flip(image,0)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![14](https://github.com/user-attachments/assets/40cdf040-b92d-407d-b84e-dd6cd53d40a8)

### 8.Write and Save the Modified Image
Save the final modified image to your local directory.
```python
import cv2
img = cv2.imread("i.jpg")
img = cv2.resize(img,(400,300))
cv2.imwrite('Lokesh.jpg',img)
```
![Screenshot 2024-09-21 183642](https://github.com/user-attachments/assets/c6cbf4f0-e35f-4e36-ae5b-796d7cb0cf0e)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







