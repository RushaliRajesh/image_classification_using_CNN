```python
img_size = 120

training_data=[]

for i in trclasses:
    trpath = os.path.join(trdatadir, i)
    trclass_num = trclasses.index(i)
    for img in os.listdir(trpath):
        img_array = cv2.imread(os.path.join(trpath,img), cv2.IMREAD_GRAYSCALE)
        new_img_array = cv2.resize(img_array,(img_size,img_size))
        training_data.append([new_img_array,trclass_num])
        
testing_data=[]

for i in teclasses:
    tepath = os.path.join(tedatadir, i)
    teclass_num = teclasses.index(i)
    for img in os.listdir(tepath):
        test_array = cv2.imread(os.path.join(tepath,img), cv2.IMREAD_GRAYSCALE)
        new_test_array = cv2.resize(test_array,(img_size,img_size))
        testing_data.append([new_img_array,teclass_num])
```
