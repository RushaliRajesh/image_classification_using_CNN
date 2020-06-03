```python
from keras.models import Sequential
from keras.layers import Dense, Conv2D, Flatten, MaxPooling2D, Conv2D, Dropout

model = Sequential()

model.add(Conv2D(32, kernel_size = 5, activation = 'relu',input_shape=(img_size,img_size,1)))  
model.add(MaxPooling2D(pool_size = (2,2) , strides = 2))
model.add(Conv2D(64, kernel_size = 5, activation = 'relu'))
model.add(MaxPooling2D(pool_size = (2,2) , strides = 2))

model.add(Flatten())
model.add(Dense(32, activation='relu'))
model.add(Dropout(0.4))
model.add(Dense(2, activation='softmax'))

```
