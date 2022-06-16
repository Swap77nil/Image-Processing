# Image-Processing<br>
http://localhost:8889/notebooks/swap/program1.ipynb<br>
Program 1:<br>
import cv2<br>
img=cv2.imread('blue.jpg',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

<br>
Program 2:<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('leaf1.jpg')<br>
plt.imshow(img)<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97939356/173813368-136d4654-07a2-40c2-8f6f-d616996be0e9.png)
![Screenshot 2022-06-15 161934](https://user-images.githubusercontent.com/98145032/173815255-f95445d5-72e1-4318-a569-303caa92e8d1.png)<br>
<br>
3:
from PIL import Image<br>
img=Image.open('butterfly1.jpg')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
<br>
4:
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br><br>
<br>
5:
import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=mping.imread('plant1.jpg')<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
OUTPUT:<br>
![Screenshot 2022-06-15 162257](https://user-images.githubusercontent.com/98145032/173815385-69c271f2-9c88-4a29-b227-82b8c19e6f77.png)<br>
<br>
6:
from PIL import Image<br>
img=Image.open('plant1.jpg')<br>
print('Filename:',img.filename)<br>
print('Format:',img.format)<br>
print('Mode:',img.mode)<br>
print('Size:',img.size)<br>
print('Width:',img.width)<br>
print('Height:',img.height)<br>
img.close()<br>
OUTPUT:<br>
![Screenshot 2022-06-15 162538](https://user-images.githubusercontent.com/98145032/173815512-6ecc0eb6-03aa-4f73-8771-e178125146a8.png)
<br>
<br>
7:
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>
OUTPUT:<br>
![Screenshot 2022-06-15 162807](https://user-images.githubusercontent.com/98145032/173815622-3e93c08c-63fe-47c1-b2cb-2ed4297301d2.png)
<br>
8:
import cv2
img=cv2.imread('blue.jpg')
print('original image length width',img.shape)
cv2.imshow('original image',img)
cv2.waitKey(0)
#to show resized image
imgresize=cv2.resize(img,(150,160))
cv2.imshow('Resized image',imgresize)
print('Resized image length width',imgresize.shape)
cv2.waitKey(0)
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/98145032/174045246-7e960d12-d8ab-4519-94f1-48c823315080.png)
