# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:E.Kamali
### Register Number: 212222110015


## Output:

### i) Read and display the image

```
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

##OUTPUT 
![307216798-0eb621aa-2159-478d-a410-602ddb5e8251](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/5d51b5e9-eadb-41b3-aeea-7ad210998f30)



### ii)Write the image
```
    import cv2
    image=cv2.imread('images.jpg',0)
    cv2.imwrite('natural.jpg',image)
```
##OUTPUT

![307216903-9d717855-bb9d-41e6-916f-ac3205453f25](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/b2eac78e-94e8-4584-be44-779b3c89e322)


### iii)Shape of the Image
```
    import cv2
    image=cv2.imread('images.jpg',1)
    print(image.shape)
```

##OUTPUT
![307217027-46902cb3-9d2f-4729-98a7-b9e04fc95ca2](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/1c9dce50-ef51-4f94-9cd7-60d39e0b54a8)



### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

##OUTPUT

![307217437-701c00d5-76d0-4a10-a74f-0ba58420a05a](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/1cbcc976-f166-4568-831d-4521954bc4c5)


### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('images.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('natural',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```

##OUTPUT

![307217496-2d007fda-b32b-4d5f-a042-e1f685651395](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/1f93cf1b-095f-4179-ae2f-eede85e2e1e4)

### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('images.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
##OUTPUT

![307217659-4bd1f54d-36e3-4278-afc6-1f60481e10e0](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/5201d541-b3a1-4147-a5a9-86ceee3a8e70)


![307217674-0f5e1f37-6217-4248-bdc1-810937b1a6a3](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/e04c8558-6115-401e-9366-ea8c4ac3b249)


![307217682-fd2452ac-baed-4ed9-8be3-c9045450ee59](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/c1949b82-1ff5-448d-99e1-679a825df04d)


![307217701-a7e6d7e5-5e1f-4ec2-b794-01536c0e1a22](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/548bc41a-7cf9-45de-854c-e3f48e0cb7f0)


![307217756-a58b623e-bf2d-46be-be6d-1c0d8e0911a0](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/f58e712e-e305-4bfd-9aa7-bd2a0803d12e)



### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

##OUTPUT

![307217911-cfe68694-7e42-42f6-80f4-74527dcd997c](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/acccf2c3-9b42-4ac2-b968-2d7b17ee5825)


![307217919-b113c1bd-c1ae-4206-b6c5-3bcf106255f5](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/1ad0512b-c854-4937-b555-5947d5418605)



![307217933-94cf556b-5ce2-4c7e-94e3-7977fc944ad0](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/e5fd5915-85b6-4ff9-894d-f6fe9c7d86e0)



### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

##OUTPUT

![307218032-d54056a6-12fa-4d52-b7fe-9880b7062b73](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/9c2753ab-b9bf-43e3-adf0-609d2be05806)


![307218037-51f1c2dd-8728-4787-a73e-b179843ef075](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/77bebf13-3269-4cbb-8ccf-9b931a6c4a82)


![307218054-a329b99d-058c-4588-b48d-a904500c7937](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/65d2a772-68a2-4c51-860d-f5d925f5423b)



### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('images.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

##OUTPUT

![307218143-e1fac2e4-dc15-45f3-98b5-81c65311f33e](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/d6106171-698b-4750-84af-ad14c9427957)


![307218190-77a67c0d-8c8e-412a-b7be-5adfb8d8fc17](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/b3475358-a366-4c21-8528-2fc13b9cf5f4)

![307218237-551cf5f6-4ea8-46aa-8e5c-5d60898a73e9](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/c1a4a7b7-1764-4e5a-a4b0-5f2948c6800a)


![307218268-0195593d-990e-4ec5-8a59-16d3973df9e0](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/ce884f92-8c75-4370-868b-7553e2b4c8b2)


### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("images.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

##OUTPUT

![307218377-06d3fe79-5611-494f-be36-7cf48571e65f](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/148bd538-dddc-46b6-ba1a-19608b3bf0cf)


![307218396-f2465292-5dc6-4cef-bd2e-f3afa674dddc](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/8dc31356-1874-4aa1-93f1-0cd7b66a50fa)



![307218406-7d5f6dd9-d3a9-4864-9033-973284ce34ae](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/651f8b99-3123-40dc-aa9f-91aaa18c2ccc)


![307218442-608846e6-397f-4ee4-aaa8-16f83f53c916](https://github.com/Kamali22004796/COLOR_CONVERSIONS_OF-IMAGE/assets/120567837/34655f0e-e42c-4dab-84fe-f1158108ba85)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







