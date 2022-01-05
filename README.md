

# Develop a Program to perform linear transformation on a image 

import cv2

image = cv2.imread('baby1.jpg')

height, width = image.shape[:2]

center = (width/2, height/2)

rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=90, scale=1)

rotated_image = cv2.warpAffine(src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow('Original image', image)
cv2.imshow('Rotated image', rotated_image)

cv2.waitKey(0)

cv2.imwrite('rotated_image.jpg', rotated_image)

output
![image](https://user-images.githubusercontent.com/96234626/148198022-8d429fdf-4095-44ae-9147-bfe3ac042b5c.png)
![image](https://user-images.githubusercontent.com/96234626/148198198-0b6633ce-68c7-4355-8890-3ce26d787124.png)
