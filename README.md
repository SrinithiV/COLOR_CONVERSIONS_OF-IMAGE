## Exp.No:01
## COLOR_CONVERSIONS_OF_IMAGE
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
o	Access and print the value of the pixel.

o	Modify the color of the pixel at (300, 300) to white.

### Step5:
o	Resize the original image to half its size and display it.

### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 300x300 pixel area starting at (50, 50)) and display it.

### Step7:
o	Flip the original image horizontally and display it.

o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.

### Program:
### Developed By: SRINITHI V
### Register Number: 212222110046
### 1.Read and display the image
Load an image from your local directory and display it.
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('cat.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')
plt.title("Original Image")
plt.axis('off') 
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/69b64e4f-4bc1-4068-a8e6-5ceb92ca1477)

### 2.Draw Shapes and Add Text
i) Draw a line from the top-left to the bottom-right of the image.
```python
img_rgb.shape
```
(830, 980, 3)
```python
line_img = cv2.line(img_rgb, (0, 0), (980, 830), (255, 0, 0), 2)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/217572e9-e07d-4742-89c1-fcdab5e8ebdc)

ii) Draw a circle at the center of the image.
```python
img = cv2.imread('cat.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```
(830, 980, 3)
```python
circle_img = cv2.circle(img_rgb,(500,400),150,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/e0b1ca33-ee0d-4e6c-95b0-99fdba4ed886)

iii) Draw a rectangle around a specific region of interest in the image.
```python
img = cv2.imread('cat.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```
(830, 980, 3)
```python
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (980, 830), (0, 0, 255), 10)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/c1f4920d-33ff-4285-8d17-cc2eea057146)

iv) Add the text "OpenCV Drawing" at the top-left corner of the image.
```python
img = cv2.imread('cat.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (20, 50), cv2.FONT_HERSHEY_SIMPLEX, 1.5, (255, 255, 255), 10)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/4e3db98c-2d3f-4203-841a-05c2e54b7e1c)

### 3.Image Color Conversion
i) Convert the image from RGB to HSV and display it
```python
img = cv2.imread('cat.png', cv2.IMREAD_COLOR)
image_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```
#### Output:
![image](https://github.com/user-attachments/assets/be048117-3353-49ed-86b0-5836a7a4467e)

```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```
#### Output:
![image](https://github.com/user-attachments/assets/aba2ca91-2fe5-42bd-a8d6-81d64cf0e51a)

ii) Convert the image from RGB to GRAY and display it.
```python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```
#### Output:
![image](https://github.com/user-attachments/assets/ca721135-4d9a-486d-b6f3-c67fde72dd79)

iii)Convert the image from RGB to YCrCb and display it.
```python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```
#### Output:
![image](https://github.com/user-attachments/assets/67d516b0-0d3b-4f0b-a369-967f0a91684b)

iv) Convert the HSV image back to RGB and display it.
```python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```
#### Output:
![image](https://github.com/user-attachments/assets/0a0cdd19-38e2-4e98-9de9-bd78fcc218df)

### 4.Access and Manipulate Image Pixels
i) Access and print the value of the pixel at coordinates (100, 100).
```python
img[200:500, 200:500] = [255, 255, 255]
```
ii) Modify the color of the pixel at (300, 300) to white.
```python
image_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/ca085e97-e429-4ce4-82f7-4762f93e3e5e)

### 5.Image Resizing:
```python
image = cv2.imread('cat.png') 
image.shape
```
(830, 980, 3)
```python
resized_image = cv2.resize(image, (980 // 2, 830 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
```
(415, 490, 3)
```python
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/7cfbed92-11bf-4e10-a7e2-390991a97cf0)

### 6.Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 300x300 pixel area starting at (50, 50)) and display it.
```python
image = cv2.imread('cat.png') 
image.shape
```
(830, 980, 3)
```python
roi = image[50:350, 50:350]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
#### Output:
![image](https://github.com/user-attachments/assets/007b4e4d-7969-45ea-84fe-a7171dd34d4c)

### 7.Image Flipping:
i) Flip the original image horizontally and display it.
```python
image = cv2.imread('cat.png')
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```
#### Output:
![image](https://github.com/user-attachments/assets/7fee8c6e-5bc5-4509-a955-f3c64aa6bfb5)

ii) Flip the original image vertically and display it.
```python
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
#### Output:
![image](https://github.com/user-attachments/assets/8c20a262-c2a3-4187-9e54-9860b8bf0e2b)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
