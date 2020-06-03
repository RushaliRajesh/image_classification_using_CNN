```python
from keras.utils import to_categorical
x=[]
y=[]
for f,l in training_data:
    x.append(f)
    y.append(l)
x = numpy.array(x).reshape(-1,img_size,img_size,1)
y = to_categorical(y)

test_x=[]
test_y=[]
for f,l in testing_data:
    test_x.append(f)
    test_y.append(l)
test_x = numpy.array(test_x).reshape(-1,img_size,img_size,1)
test_y = to_categorical(test_y)
```
