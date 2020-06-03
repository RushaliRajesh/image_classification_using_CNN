```python
model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
model.fit(x,y,validation_data=(test_x,test_y), epochs=100)
```
