# Image-Processing<br>
http://localhost:8889/notebooks/swap/program1.ipynb<br>
Program 1:<br>
import cv2<br>
img=cv2.imread('blue.jpg',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
OUTPUT:<br>

<br>
Program 2:<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('leaf1.jpg')<br>
plt.imshow(img)<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/98145032/173810032-9d9e8ce2-0cbe-48e3-8f65-770193caf0a6.png)<br>
<br>
from PIL import Image<br>
img=Image.open('butterfly1.jpg')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br><br>
<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=mping.imread('plant1.jpg')<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/98145032/173810598-1c1e6298-ebd9-40d3-93af-6d50f2c39717.png)<br>
<br>
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
![image](https://user-images.githubusercontent.com/98145032/173811041-904aae41-7e07-4d86-a615-63afab6f5e5d.png)<br>
<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/98145032/173811477-123c679c-062c-473b-b6c5-2c7f8df61686.png)<br>

