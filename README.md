# DIPT-basic-image-manupilation
# DiptExp
# Basic image manipulation
#NAVEEN S -212222240070

```
import cv2

image = cv2.imread('Apollo.jpeg', cv2.IMREAD_GRAYSCALE)

height, width = image.shape
print("Width:", width)
print("Height:", height)

plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off')
plt.show()

cv2.imwrite('Apollo-11-launch.png', image)
import cv2

image_color = cv2.imread('NZ.jpeg', cv2.IMREAD_COLOR)

print("Color Image Shape:", image_color.shape)

image_gray = cv2.cvtColor(image_color, cv2.COLOR_BGR2GRAY)

print("Grayscale Image Shape:", image_gray.shape)

plt.figure(figsize=[10, 10])
plt.imshow(image_gray, cmap='gray')
plt.axis('off')
plt.show()
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('NZ Boat.jpeg', cv2.IMREAD_COLOR)

cropped_img = img[3:500, 3:500]  

resized_img = cv2.resize(cropped_img, None, fx=2, fy=2, interpolation=cv2.INTER_LINEAR)

flipped_img = cv2.flip(resized_img, 1)

plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1]) 
plt.axis('on')
plt.show()
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('Apollo.jpeg')

text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_PLAIN
font_scale = 3
font_color = (255, 255, 255) 
font_thickness = 2

(text_width, text_height), _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_width)   
text_y = image.shape[0] - 50 

cv2.putText(image, text, (text_x, text_y), font_face, font_scale, font_color, font_thickness)


rect_color = (255,0,255)  
top_left = (100,180) 
bottom_right = (image.shape[1] - 100, image.shape[0] - 200) 

cv2.rectangle(image, top_left, bottom_right, rect_color, 3)

plt.figure(figsize=[10, 10])
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('NZ.jpeg', cv2.IMREAD_COLOR)

print(image.shape)

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

print(gray_image.shape)

plt.figure(figsize=(10, 8))
plt.imshow(gray_image, cmap='gray')
plt.axis('on')
plt.show()

```
# Output:
![download](https://github.com/user-attachments/assets/ef163de2-5bb1-47d3-8e0d-8acf2656aac9)
![download](https://github.com/user-attachments/assets/ea839fd1-e240-45ab-a683-1d42ec2f78b8)
![download](https://github.com/user-attachments/assets/19b0ae56-90f3-4a59-9d50-3e08a05c9937)
![download](https://github.com/user-attachments/assets/16f60b87-3108-43ad-b744-659f02e7c81b)
![download](https://github.com/user-attachments/assets/1850efaa-0e09-4036-98db-e9a330454d94)

