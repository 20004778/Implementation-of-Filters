# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.

### Step2
For performing smoothing operation on a image.
```python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
Weighted average filter
```python
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
Gaussian Blur
```python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```
Median filter
```python
median_blur=cv2.medianBlur(image,11)
```

### Step3
For performing sharpening on a image.

Laplacian Kernel
```python
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```
Laplacian Operator
```python
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```

### Step4
Display all the images with their respective filters.
 

## Program:
### Developed By   : SURYA R
### Register Number: 212220230052

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()
```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()
```
ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

![Screenshot (101)](https://user-images.githubusercontent.com/75236145/167680531-0cc154bb-ea3a-4c0a-a145-09aa00b54207.png)

ii) Using Weighted Averaging Filter

![Screenshot (102)](https://user-images.githubusercontent.com/75236145/167680551-46f4559e-f623-4055-a28d-369b328357a0.png)

iii) Using Gaussian Filter

![Screenshot (103)](https://user-images.githubusercontent.com/75236145/167680578-e1f3acc8-fab9-4f44-ba79-0d125fa91015.png)

iv) Using Median Filter
![Screenshot (104)](https://user-images.githubusercontent.com/75236145/167681225-2144132a-2ac3-4039-b3c6-47f01cf86eaa.png)


### 2. Sharpening Filters


i) Using Laplacian Kernal
![Screenshot (105)](https://user-images.githubusercontent.com/75236145/167680677-7ee76cb8-9c17-4a4f-800e-b9891cd992d0.png)


ii) Using Laplacian Operator
![Screenshot (106)](https://user-images.githubusercontent.com/75236145/167680704-291fb847-bb4c-4e70-84e2-3e03821826dd.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
