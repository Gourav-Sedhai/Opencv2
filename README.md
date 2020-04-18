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
