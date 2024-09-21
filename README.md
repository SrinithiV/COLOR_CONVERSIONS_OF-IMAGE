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


### 2.Draw Shapes and Add Text
i) Draw a line from the top-left to the bottom-right of the image.


ii) Draw a circle at the center of the image.


iii) Draw a rectangle around a specific region of interest in the image.



iv) Add the text "OpenCV Drawing" at the top-left corner of the image.

### 3.Image Color Conversion
i) Convert the image from RGB to HSV and display it

ii) Convert the image from RGB to GRAY and display it.

iii)Convert the image from RGB to YCrCb and display it.

iv) Convert the HSV image back to RGB and display it.

### 4.Access and Manipulate Image Pixels
i) Access and print the value of the pixel at coordinates (100, 100).
```python
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![image](https://github.com/user-attachments/assets/5c4eb1f2-e481-4829-9ce1-ecda06bc4df4)

ii) Modify the color of the pixel at (200, 200) to white.
```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[205:210, 205:210] = [255, 255, 255]
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/11a340c2-a55b-442b-85a2-400f3bfd4c67)

### 5.Image Resizing:
Resize the original image to half its size and display it.
```python
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/2ea2e67e-575b-404f-8275-dbe56b323826)


### 6.Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```python
import cv2
image = cv2.imread('scenery.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/42088f34-eab6-4f6a-9c49-60b4d72d369c)
### 7.Image Flipping:
i) Flip the original image horizontally and display it.
```python
import cv2
image = cv2.imread("scenery.jpg")
image = cv2.resize(image,(300,200))
res=cv2.flip(image,1)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/299f4e37-e7b3-429d-8eed-38c2d3630bba)

ii) Flip the original image vertically and display it.
```python
import cv2
image = cv2.imread("scenery.jpg")
image = cv2.resize(image,(300,200))
res=cv2.flip(image,0)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/1caa763e-d7ce-427c-92c6-ad1d493a2dfb)


### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```python
import cv2
img = cv2.imread("scenery.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('Mountains.jpg',img)
```
![image](https://github.com/user-attachments/assets/77cfd09b-aa53-49ff-85ce-61cdb3d03c31)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







