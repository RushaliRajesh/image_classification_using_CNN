```python
import tensorflow as tf
import keras
import os
import numpy
import cv2
import matplotlib.pyplot as plt

trdatadir = r"C:\Users\lenovo\Desktop\simpdataset\data\train"
trclasses = ["cats","dogs"]

tedatadir = r"C:\Users\lenovo\Desktop\simpdataset\data\test"
teclasses = ["cats","dogs"]

for i in trclasses:
    trpath = os.path.join(trdatadir, i)
    for img in os.listdir(trpath):
        img_array = cv2.imread(os.path.join(trpath,img), cv2.IMREAD_GRAYSCALE)
        #plt.imshow(img_array,cmap="gray")
        #plt.show()
        
        

for i in teclasses:
    tepath = os.path.join(tedatadir, i)
    for img in os.listdir(tepath):
        test_array = cv2.imread(os.path.join(tepath,img), cv2.IMREAD_GRAYSCALE)
        #plt.imshow(test_array,cmap="gray")
        #plt.show()
       
```
