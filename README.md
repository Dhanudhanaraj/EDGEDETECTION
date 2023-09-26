# EDGE DETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the rgb image to gray scale image.

### Step3:
Use filters for smoothing the image to reduce the noise.


### Step4:
Apply the respective filters - Sobel, Laplacian edge detector and Canny edge detector.

### Step5:
Display the filtered image using plot and imshow.


## Program:
```
DEVELOPED BY:DHANUMALYA D
REGISTER NUMBER:212222230030
```

# Import the packages
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dip2.png")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```


# SOBEL EDGE DETECTOR
## SOBEL X:
```
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()
```
## SOBEL Y:
```
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()
```
## SOBEL XY:
```
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()
```

# CANNY EDGE DETECTOR
```
canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()


```
## Output:
### SOBEL EDGE DETECTOR
## SOBEL X:
![Screenshot from 2023-09-26 22-35-08](https://github.com/Dhanudhanaraj/EDGEDETECTION/assets/119218812/9185e182-d657-4563-8413-650314e2c1ee)

## SOBEL Y:
![Screenshot from 2023-09-26 22-35-17](https://github.com/Dhanudhanaraj/EDGEDETECTION/assets/119218812/258432b3-e0f7-4495-9df0-d461b9728b80)

## SOBEL XY:
![Screenshot from 2023-09-26 22-35-24](https://github.com/Dhanudhanaraj/EDGEDETECTION/assets/119218812/fcaf24a3-6dff-4fe8-b85f-e81d3c0a9859)


### LAPLACIAN EDGE DETECTOR
![Screenshot from 2023-09-26 22-35-30](https://github.com/Dhanudhanaraj/EDGEDETECTION/assets/119218812/a6987dfc-dfac-4daf-941b-b669329dcbd4)



### CANNY EDGE DETECTOR
![Screenshot from 2023-09-26 22-35-37](https://github.com/Dhanudhanaraj/EDGEDETECTION/assets/119218812/92784546-4cb8-4edd-a74a-0d41d7e05ab4)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
