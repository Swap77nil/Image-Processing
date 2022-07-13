# Imageprocessing
http://localhost:8891/notebooks/New%20folder/programp1.ipynb<br>
1)Develope a program to display greyscale image using read and write operation<br>
import cv2<br>
img=cv2.imread('flw1.jpg',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97939356/173812703-83a9050e-d7ab-4586-b13b-d21bf6856040.png)<br>
2) Develope a program to display the image using matplotlib<br> 
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('leaf1.jpg')<br>
plt.imshow(img)<br>
output:<br>
![image](https://user-images.githubusercontent.com/97939356/173813368-136d4654-07a2-40c2-8f6f-d616996be0e9.png)<br>
3)Develop a program to perform Linear Transformation<br>
a) Rotation b) Scaling<br>
from PIL import Image<br>
img=Image.open('bf1.jpg')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
output:<br>
![image](https://user-images.githubusercontent.com/97939356/173813810-4609a005-d140-43af-a3a6-defd18a78376.png)<br>
4)Develop a program to convert Colorstring to RGB color value<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>
output:<br>
![image](https://user-images.githubusercontent.com/97939356/173814159-22c9431c-03ac-485b-b6f7-214a880d96d2.png)<br>
5)Write a program to create image using colors<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br>
output:<br>
![image](https://user-images.githubusercontent.com/97939356/173814503-e00acde1-af74-4c26-89f6-bae047e2f63e.png)<br>
6)Develop a program to visualize the image using various Colorspaces<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread('bf3.jpg')<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
output:<br>
![image](https://user-images.githubusercontent.com/97939356/173814697-38f7d778-75bd-4973-baff-14cdfbc69aea.png)<br>
7)Write a program to display the image attributes<br>
from PIL import Image<br>
image=Image.open('flw3.jpg')<br>
print("Filename",image.filename)<br>
print("Format",image.format)<br>
print("Mode",image.mode)<br>
print("Size",image.size)<br>
print("Width",image.width)<br>
print("Height",image.height)<br>
image.close();<br>
output:<br>
![image](https://user-images.githubusercontent.com/97939356/173815295-6f31699b-4609-44e8-9210-3bb4319a013e.png)<br>
8)Convert the original image to gray scale and then to binary<br>
import cv2<br>
#read the image file<br>
img=cv2.imread("flw22.jpg")<br>
cv2.imshow("RGB",img)<br>
cv2.waitKey(0)<br>
#gray scale<br>
img=cv2.imread("flw22.jpg",0)<br>
cv2.imshow("gray",img)<br>
cv2.waitKey(0)<br>
#binary image<br>
ret,bw_img=cv2.threshold(img,127,255,cv2.THRESH_BINARY)<br>
cv2.imshow("BINARY",bw_img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
![image](https://user-images.githubusercontent.com/97939356/174044748-26dfcc90-888b-4c63-abc3-853fd35d4ce4.png)<br>
![image](https://user-images.githubusercontent.com/97939356/174045047-19658c38-e426-4b83-9d5a-1d2c2ef158c2.png)<br>
![image](https://user-images.githubusercontent.com/97939356/174045302-fde2d346-0049-49a8-8da3-7c63501b68c8.png)<br>
9)Resize the original image<br>
import cv2<br>
img=cv2.imread('FLOWER2.jpg')<br>
print('Original image length width',img.shape)<br>
cv2.imshow('Original image',img)<br>
cv2.waitKey(0)<br>
imgresize=cv2.resize(img,(150,160))<br>
cv2.imshow('Resized image',imgresize)<br>
print('Resized image length width',imgresize.shape)<br>
cv2.waitKey(0)<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940475/174043738-b1cffb6b-41c9-4ce5-bcbf-d8413411edd2.png)<br>
![image](https://user-images.githubusercontent.com/97940475/174043822-d56fdf6b-7f5a-4584-abdb-144f70eb612e.png)<br>
Original image length width (668, 800, 3)<br>
Resized image length width (160, 150, 3)<br>

10)Convert the original image to gray scale and then to binary....<br>
import cv2<br>
img=cv2.imread('FLOWER3.jpeg')<br>
cv2.imshow("RGB",img)<br>
cv2.waitKey(0)<br>
img=cv2.imread('FLOWER3.jpeg',0)<br>
cv2.imshow("Gray",img)<br>
cv2.waitKey(0)<br>
ret,bw_img=cv2.threshold(img,127,255,cv2.THRESH_BINARY)<br>
cv2.imshow("Binary",bw_img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940475/174058087-2bd8b4e6-1cbc-4ef5-8f94-422d48cfdd77.png)<br>
![image](https://user-images.githubusercontent.com/97940475/174046096-495e1297-5069-4b38-9e69-75a50961ca82.png)<br>
![image](https://user-images.githubusercontent.com/97940475/174046187-aed38085-5874-4bc5-9854-85b5c7195113.png)<br>

11)Develop a program to readimage using URL.<br>
from skimage import io<br>
import matplotlib.pyplot as plt<br>
url='https://cdn.theatlantic.com/thumbor/viW9N1IQLbCrJ0HMtPRvXPXShkU=/0x131:2555x1568/976x549/media/img/mt/2017/06/shutterstock_319985324/original.jpg'<br>
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940475/175264633-b00283fc-ac7c-4374-a52b-eb8ef2da7f94.png)<br>

12)Write a program to mask and blur the image.<br>
import cv2<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('R.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175264974-f98220d0-4d07-4eaf-80fc-904dcd6f0afc.png)<br>
hsv_img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
light_orange=(1, 190, 200)<br>
dark_orange=(18, 255, 255)<br>
mask=cv2.inRange(hsv_img,light_orange,dark_orange)<br>
result=cv2.bitwise_and(img,img,mask=mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175265164-61aa903f-f23b-4041-bf82-8f8fa1431b4e.png)<br>
light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175265249-358a969d-837f-43f1-92c2-ac424f66a57e.png)<br>
final_mask=mask+mask_white<br>
final_result=cv2.bitwise_and(img,img,mask=final_mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(final_mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(final_result)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175265334-c8a492a1-29c1-44c2-8283-3f1fab2ab1bd.png)<br>
blur=cv2.GaussianBlur(final_result, (7,7), 0)<br>
plt.imshow(blur)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175265449-7ee022b2-d1b9-4fbd-b77d-583c133ca31e.png)<br>

13)Write a program to mask and blur the image.<br>
import cv2<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('img.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175265765-0035f402-4038-4aba-a256-7d6638d1917c.png)<br>
light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175265866-69c284b7-3ebe-4fc1-8bdb-bb97a9b9094e.png)<br>
blur=cv2.GaussianBlur(result_white, (7,7), 0)<br>
plt.imshow(blur)<br>
plt.show()<br>
![download](https://user-images.githubusercontent.com/97940475/175265927-7ca7c9df-e4aa-4551-9e38-d0f02b402d67.png)<br>

14)Write a program to perform arithmatic operations on images<br>
import cv2<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>

#Reading image file<br>
img1=cv2.imread('FLOWER1.jpg')<br>
img2=cv2.imread('BUTTERFLY3.jpg')<br>

#Applying numpy addition on images<br>
fimg1 = img1 + img2<br>
plt.imshow(fimg1)<br>
plt.show()<br>

#saving the output images<br>
cv2.imwrite('output.jpg',fimg1)<br>
fimg2 = img1 - img2<br>
plt.imshow(fimg2)<br>
plt.show()<br>

#saving the output image<br>
cv2.imwrite('output.jpg',fimg2)<br>
fimg3 = img1 * img2<br>
plt.imshow(fimg3)<br>
plt.show()<br>

#saving the output image<br>
cv2.imwrite('output.jpg',fimg3)<br>
fimg4 = img1 / img2<br>
plt.imshow(fimg4)<br>
plt.show()<br>

#saving the output image<br>
cv2.imwrite('output.jpg',fimg4)<br>

OUTPUT:<br>
![download](https://user-images.githubusercontent.com/97940475/175266340-77562e3d-46e1-47a3-bce0-06e1115edc7b.png)<br>
![download](https://user-images.githubusercontent.com/97940475/175266390-7b4b0af4-0ecb-4b60-bb4e-f67a7b53f3c6.png)<br>
![download](https://user-images.githubusercontent.com/97940475/175266441-6fc61c5e-4eb5-4540-909d-d8f05efe33c5.png)<br>
![download](https://user-images.githubusercontent.com/97940475/175266508-9e240717-910e-439b-9719-beb6a97b96b9.png)<br>

15)Develop the program to change the image to different color spaces.<br>
import cv2 <br>
img=cv2.imread("PLANT5.jpg")<br>
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<br>
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<br>
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)<br>
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)<br>
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)<br>
cv2.imshow("GRAY image",gray)<br>
cv2.imshow("HSV image",hsv)<br>
cv2.imshow("LAB image",lab)
cv2.imshow("HLS image",hls)<br>
cv2.imshow("YUV image",yuv)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940475/175266819-0c7f15f6-d04e-4065-9baa-86e3a93d83e2.png)<br>
![image](https://user-images.githubusercontent.com/97940475/175266936-c8cedc80-94c2-45f0-ac13-a9ba7f1b5c85.png)<br>
![image](https://user-images.githubusercontent.com/97940475/175267057-08276b48-6976-4691-b99f-38e396e39478.png)<br>
![image](https://user-images.githubusercontent.com/97940475/175267228-3c8c3fef-f28a-42e2-8b36-316f25c2dd32.png)<br>
![image](https://user-images.githubusercontent.com/97940475/175267310-752ec506-b426-4088-bbef-933e68b2e6be.png)<br>

16)Program to create an image using 2D array<br>
import cv2 as  c<br>
import numpy as np<br>
from PIL import Image<br>
array=np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('IMAGES.jpg')<br>
img.show()<br>
c.waitKey(0)<br>

OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940475/175268623-22cefe1a-fb53-46e1-9e3d-fce04be704b5.png)<br>

17) Bitwise Operations:<br>
#Bitwise Operations<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
image1 = cv2.imread('bb1.jpg',1)<br>
image2 = cv2.imread('leaf1.jpg')<br>
ax=plt.subplots(figsize=(15,10))<br>
bitwiseAnd = cv2.bitwise_and(image1,image2)<br>
bitwiseOr = cv2.bitwise_or(image1,image2)<br>
bitwiseXor = cv2.bitwise_xor(image1,image2)<br>
bitwiseNot_img1 = cv2.bitwise_not(image1)<br>
bitwiseNot_img2 = cv2.bitwise_not(image2)<br>
plt.subplot(151)<br>
plt.imshow(bitwiseAnd)<br>
plt.subplot(152)<br>
plt.imshow(bitwiseOr)<br>
plt.subplot(153)<br>
plt.imshow(bitwiseXor)<br>
plt.subplot(154)<br>
plt.imshow(bitwiseNot_img1)<br>
plt.subplot(155)<br>
plt.imshow(bitwiseNot_img2)<br>
cv2.waitKey(0)<br>
OUTPUT:<br>
![ss1](https://user-images.githubusercontent.com/98145032/176410703-91e4581a-8e6f-48c9-ae1f-30b86ea064f9.png)<br>

18) Blurring Image<br>
#Blurring<br>
import cv2<br>
import numpy as np<br>
image=cv2.imread('bb1.jpg')<br>
cv2.imshow('original image',image)<br>
cv2.waitKey(0)<br>
#gaussian blur<br>
Gaussian=cv2.GaussianBlur(image,(7,7),0)<br>
cv2.imshow('Gaussian Blurring',Gaussian)<br>
cv2.waitKey(0)<br>
#median blur<br>
median=cv2.medianBlur(image,5)<br>
cv2.imshow('Median Blurring',median)<br>
cv2.waitKey(0)<br>
#Bilateral Blur<br>
bilateral =cv2.bilateralFilter(image,9,75,75)<br>
cv2.imshow('Bilateral Blurring',bilateral)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
OUTPUT:<br>
![s1](https://user-images.githubusercontent.com/98145032/176411205-6180e983-5b65-4919-a1fd-0511d978cb97.png)<br>
![s2](https://user-images.githubusercontent.com/98145032/176411287-55dcdd26-a8f2-4743-a994-55bb18d68276.png)<br>
![s3](https://user-images.githubusercontent.com/98145032/176411331-f62501a3-9e9a-4ac0-869e-b281f50bb8df.png)<br>
![s4](https://user-images.githubusercontent.com/98145032/176411360-50e236a5-fc2b-4877-b9a6-5028b6c91673.png)<br>

19) Image Enhancement<br>
#Image Enhancement<br>
from PIL import Image<br>
from PIL import ImageEnhance<br>
image = Image.open('bb1.jpg')<br>
image.show()<br>
enh_bri = ImageEnhance.Brightness(image)<br>
brightness=1.5<br>
image_brightened = enh_bri.enhance(brightness)<br>
image_brightened.show()<br>
enh_col = ImageEnhance.Color(image)<br>
color=1.5<br>
image_colored = enh_col.enhance(color)<br>
image_colored.show()<br>
enh_con = ImageEnhance.Contrast(image)<br>
contrast=1.5<br>
image_contrasted = enh_con.enhance(contrast)<br>
image_contrasted.show()<br>
enh_sha = ImageEnhance.Sharpness(image)<br>
sharpness=3.0<br>
image_sharped = enh_sha.enhance(sharpness)<br>
image_sharped.show()<br>
OUTPUT:<br>
![ss3](https://user-images.githubusercontent.com/98145032/176411676-ff69e930-53c6-4b0c-8cf0-68ea9c5956b7.png)<br>

20) Morphological Operations<br>
#Morphological operations<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
from PIL import Image,ImageEnhance<br>
img=cv2.imread('bb1.jpg',0)<br>
ax=plt.subplots(figsize=(20,10))<br>
kernel= np.ones((5,5),np.uint8)<br>
opening=cv2.morphologyEx(img,cv2.MORPH_OPEN, kernel)<br>
closing=cv2.morphologyEx(img, cv2.MORPH_CLOSE,kernel)<br>
erosion=cv2.erode(img,kernel,iterations=1)<br>
dilation=cv2.dilate(img,kernel,iterations=1)<br>
gradient=cv2.morphologyEx(img,cv2.MORPH_GRADIENT,kernel)<br>
plt.subplot(151)<br>
plt.imshow(opening)<br>
plt.subplot(152)<br>
plt.imshow(closing)<br>
plt.subplot(153)<br>
plt.imshow(erosion)<br>
plt.subplot(154)<br>
plt.imshow(dilation)<br>
plt.subplot(155)<br>
plt.imshow(gradient)<br>
cv2.waitKey(0)<br>
OUTPUT:<br>
![sss4](https://user-images.githubusercontent.com/98145032/176411996-1a40e1c3-256a-4c21-8ecb-c2c864d169bc.png)<br>

21) Grayscale Slicing with Background<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('cat1.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
             z[i][j]=image[i][j]<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing with background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/98145032/178703361-4fb593b3-9431-45e0-95f3-66ddf428ec10.png)<br>

22) Grayscale Slicing without Background<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('cat1.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
             z[i][j]=0<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing with background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/98145032/178703582-30604e53-2037-4bf7-abc6-9b3e2c0905da.png)<br>

23) Saving Grayscale Image<br>
import cv2<br>
OriginalImg=cv2.imread('bb1.jpg')<br>
GrayImg=cv2.imread('bb1.jpg',0)<br>
isSaved=cv2.imwrite('E:/img.jpg',GrayImg)<br>
cv2.imshow('Disaplay Original Image',OriginalImg)<br>
cv2.imshow('Disaplay Grayscale Image',GrayImg)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
if isSaved:<br>
    print('The image is successfully saved.')<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/98145032/178704421-96d38372-96e9-4b7c-a966-285d80f148ff.png)<br>
![image](https://user-images.githubusercontent.com/98145032/178704216-c3b3e6e8-05b0-44a0-9155-2c9c4babfc83.png)<br>





