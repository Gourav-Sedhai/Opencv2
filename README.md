# Opencv2
Python for Image and Video Processing with OpenCV
----------------------------------------------------------------------------------------------- 
#sript1.py
 
import cv2

img = cv2.imread("galaxy.jpg", 0)

print(type(img))
print(img)Python for Image and Video Processing with OpenCV

print(img.shape)
print(img.ndim)

resized_image = cv2.resize(img,(int(img.shape[1]/2), int(img.shape[0]/2)))
cv2.imshow("galaxy", resized_image)
cv2.imwrite("galaxy_resized.jpg", resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
----------------------------------------------------------------------------------------------
#script2.py

import cv2
import glob

images=glob.glob("*.jpg")

for image in images:
    img=cv2.imread(image,0)
    re=cv2.resize(img,(100,100))
    cv2.imshow("Hey",re)
    cv2.waitKey(500)
    cv2.destroyAllWindows()
    cv2.imwrite("resized_"+image,re)
----------------------------------------------------------------------------------------------------
#script3.py

import cv2

face_cascade = cv2.CascadeClassifier("haarcascade_frontalface_default.xml")

img = cv2.imread("news.jpg")
gray_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

faces = face_cascade.detectMultiScale(gray_img,
scaleFactor=1.1,
minNeighbors=5)

for x, y, w, h in faces:
    img = cv2.rectangle(img, (x,y), (x+w,y+h), (0,255,0), 3)

print(type(faces))
print(faces)

resized = cv2.resize(img, (int(img.shape[1]/3), int(img.shape[0]/3)))

cv2.imshow("Gray", resized)
cv2.waitKey(0)
cv2.destroyAllWindows
------------------------------------------------------------------------------------------------
