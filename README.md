# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:

##
Step1:
Import cv2 and save and image as filename.jpg

##
Step2:
Use imread(filename, flags) to read the file.

##
Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

##
Step4:
Split and merge the image using cv2.split and cv2.merge commands.

##
Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By:S.Meena
# Register Number:212221240028
# i) Convert BGR and RGB to HSV and GRAY
import cv2
bike_color_image= cv2.imread('bike.jpg')
cv2.imshow ('Original image', bike_color_image)
hsv_image= cv2.cvtColor (bike_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_image)
hsv_image1 = cv2.cvtColor (bike_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_image1)
gray_image= cv2.cvtColor (bike_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_image)
gray_image1 = cv2.cvtColor (bike_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()




# ii)Convert HSV to RGB and BGR
import cv2
bike_HSV_image= cv2.imread('bike.jpg')
cv2.imshow('Original HSV image',bike_HSV_image)
RGB_image = cv2.cvtColor(bike_HSV_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',RGB_image )
BGR_image = cv2.cvtColor(bike_HSV_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllwindows()




# iii)Convert RGB and BGR to YCrCb
import cv2
bikeImage = cv2.imread('bike.jpg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(bikeImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(bikeImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()



# iv)Split and Merge RGB Image
import cv2
image = cv2.imread('bike.jpg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()



# v) Split and merge HSV Image
import cv2
image = cv2.imread('bike.jpg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (23)](https://user-images.githubusercontent.com/94677128/162784114-6e0ba995-07eb-440f-914d-c75b440827c2.png)


### ii) HSV to RGB and BGR
![Screenshot (24)](https://user-images.githubusercontent.com/94677128/162784794-e7d3ff46-306e-4154-b1dc-bcb5a72bff44.png)



### iii) RGB and BGR to YCrCb
![Screenshot (25)](https://user-images.githubusercontent.com/94677128/162784646-f8d003ab-5acf-4043-adab-1fa1566d2571.png)


### iv) Split and merge RGB Image
![Screenshot (26)](https://user-images.githubusercontent.com/94677128/162784929-e00223c0-3a0d-4966-b448-1bc109bf2557.png)


### v) Split and merge HSV Image
![Screenshot (27)](https://user-images.githubusercontent.com/94677128/162785038-0ab8a1d5-deef-459d-8b42-40f363d8a86f.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
