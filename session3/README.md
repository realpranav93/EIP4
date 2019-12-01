### 1. Final Validation score of base model:
```
Accuracy on test data is: 82.36
```

### 2. Model Validation Definition:
```
model2 = Sequential()
#receptive field , number of channels , output size
model2.add(SeparableConv2D(48, 3, 3, border_mode='same', input_shape=(32, 32, 3))) #  3x3, 48c, 32x32
model2.add(Activation('relu'))
model2.add(BatchNormalization())
model2.add(SeparableConv2D(96, 3, 3,border_mode = 'same')) # 5x5,48c, 32x32
model2.add(BatchNormalization())
model2.add(Activation('relu'))
model2.add(MaxPooling2D(pool_size=(2, 2))) # 6x6,48c, 16x16
model2.add(Dropout(0.25))



model2.add(SeparableConv2D(48, 1, 1)) # 6x6, 48c,16x16
model2.add(Activation('relu'))
model2.add(BatchNormalization())
model2.add(SeparableConv2D(96, 3, 3,border_mode='same')) # 10x10, 96c, 16x16
model2.add(Activation('relu'))
model2.add(BatchNormalization())
model2.add(MaxPooling2D(pool_size=(2, 2))) # 12x12, 96c, 8x8
model2.add(Dropout(0.25))



model2.add(SeparableConv2D(96, 1, 1))# 12x12, 96c, 8x8
model2.add(Activation('relu'))
model2.add(BatchNormalization())
model2.add(SeparableConv2D(192, 3, 3, border_mode='same')) # 20x20, 192c, 8x8
model2.add(Activation('relu'))
model2.add(BatchNormalization())
model2.add(Dropout(0.25))


model2.add(SeparableConv2D(10,1,1)) # 20x20, 10c, 8x8
model2.add(Activation('relu'))
model2.add(BatchNormalization())
model2.add(SeparableConv2D(10, 8, 8)) # 48x48, 10c, 1x1

model2.add(Flatten())
model2.add(Activation('softmax'))
# Compile the model
model2.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])

model2.summary()
```

### 3. 50 epochs log: 

```


/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:12: UserWarning: The semantics of the Keras 2 argument `steps_per_epoch` is not the same as the Keras 1 argument `samples_per_epoch`. `steps_per_epoch` is the number of batches to draw from the generator at each epoch. Basically steps_per_epoch = samples_per_epoch/batch_size. Similarly `nb_val_samples`->`validation_steps` and `val_samples`->`steps` arguments have changed. Update your method calls accordingly.
  if sys.path[0] == '':
/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:12: UserWarning: Update your `fit_generator` call to the Keras 2 API: `fit_generator(<keras_pre..., validation_data=(array([[[..., verbose=1, steps_per_epoch=390, epochs=50)`
  if sys.path[0] == '':

Epoch 1/50
390/390 [==============================] - 15s 38ms/step - loss: 1.6541 - acc: 0.3961 - val_loss: 1.4494 - val_acc: 0.4830
Epoch 2/50
390/390 [==============================] - 12s 31ms/step - loss: 1.2209 - acc: 0.5607 - val_loss: 1.2658 - val_acc: 0.5579
Epoch 3/50
390/390 [==============================] - 12s 31ms/step - loss: 1.0440 - acc: 0.6296 - val_loss: 1.0845 - val_acc: 0.6164
Epoch 4/50
390/390 [==============================] - 12s 31ms/step - loss: 0.9395 - acc: 0.6663 - val_loss: 0.9933 - val_acc: 0.6602
Epoch 5/50
390/390 [==============================] - 12s 31ms/step - loss: 0.8703 - acc: 0.6914 - val_loss: 0.8823 - val_acc: 0.6926
Epoch 6/50
390/390 [==============================] - 12s 31ms/step - loss: 0.8157 - acc: 0.7112 - val_loss: 0.8721 - val_acc: 0.7038
Epoch 7/50
390/390 [==============================] - 12s 31ms/step - loss: 0.7677 - acc: 0.7284 - val_loss: 0.7814 - val_acc: 0.7295
Epoch 8/50
390/390 [==============================] - 12s 31ms/step - loss: 0.7228 - acc: 0.7454 - val_loss: 0.7695 - val_acc: 0.7347
Epoch 9/50
390/390 [==============================] - 12s 31ms/step - loss: 0.6913 - acc: 0.7562 - val_loss: 0.7965 - val_acc: 0.7327
Epoch 10/50
390/390 [==============================] - 12s 31ms/step - loss: 0.6602 - acc: 0.7669 - val_loss: 0.7008 - val_acc: 0.7576
Epoch 11/50
390/390 [==============================] - 12s 31ms/step - loss: 0.6415 - acc: 0.7715 - val_loss: 0.8295 - val_acc: 0.7214
Epoch 12/50
390/390 [==============================] - 12s 31ms/step - loss: 0.6156 - acc: 0.7851 - val_loss: 0.7462 - val_acc: 0.7541
Epoch 13/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5995 - acc: 0.7887 - val_loss: 0.7322 - val_acc: 0.7590
Epoch 14/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5786 - acc: 0.7964 - val_loss: 0.7009 - val_acc: 0.7700
Epoch 15/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5638 - acc: 0.8001 - val_loss: 0.7215 - val_acc: 0.7690
Epoch 16/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5534 - acc: 0.8054 - val_loss: 0.5988 - val_acc: 0.7964
Epoch 17/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5394 - acc: 0.8098 - val_loss: 0.6215 - val_acc: 0.7916
Epoch 18/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5251 - acc: 0.8165 - val_loss: 0.6181 - val_acc: 0.7915
Epoch 19/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5146 - acc: 0.8178 - val_loss: 0.6233 - val_acc: 0.7937
Epoch 20/50
390/390 [==============================] - 12s 31ms/step - loss: 0.5101 - acc: 0.8202 - val_loss: 0.5856 - val_acc: 0.8035
Epoch 21/50
390/390 [==============================] - 12s 32ms/step - loss: 0.4983 - acc: 0.8251 - val_loss: 0.6618 - val_acc: 0.7859
Epoch 22/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4894 - acc: 0.8263 - val_loss: 0.6012 - val_acc: 0.8028
Epoch 23/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4792 - acc: 0.8306 - val_loss: 0.6483 - val_acc: 0.7935
Epoch 24/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4790 - acc: 0.8315 - val_loss: 0.5995 - val_acc: 0.7972
Epoch 25/50
390/390 [==============================] - 12s 32ms/step - loss: 0.4618 - acc: 0.8364 - val_loss: 0.5771 - val_acc: 0.8072
Epoch 26/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4583 - acc: 0.8383 - val_loss: 0.5895 - val_acc: 0.8068
Epoch 27/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4576 - acc: 0.8396 - val_loss: 0.6108 - val_acc: 0.8020
Epoch 28/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4494 - acc: 0.8399 - val_loss: 0.6062 - val_acc: 0.8007
Epoch 29/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4419 - acc: 0.8430 - val_loss: 0.5951 - val_acc: 0.8066
Epoch 30/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4401 - acc: 0.8436 - val_loss: 0.6165 - val_acc: 0.8025
Epoch 31/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4299 - acc: 0.8490 - val_loss: 0.6005 - val_acc: 0.8040
Epoch 32/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4260 - acc: 0.8482 - val_loss: 0.5331 - val_acc: 0.8196
Epoch 33/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4182 - acc: 0.8526 - val_loss: 0.6727 - val_acc: 0.7939
Epoch 34/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4160 - acc: 0.8541 - val_loss: 0.6265 - val_acc: 0.7988
Epoch 35/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4186 - acc: 0.8504 - val_loss: 0.6108 - val_acc: 0.8054
Epoch 36/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4085 - acc: 0.8550 - val_loss: 0.5985 - val_acc: 0.8105
Epoch 37/50
390/390 [==============================] - 12s 31ms/step - loss: 0.4079 - acc: 0.8552 - val_loss: 0.5521 - val_acc: 0.8192
Epoch 38/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3960 - acc: 0.8593 - val_loss: 0.6045 - val_acc: 0.8082
Epoch 39/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3964 - acc: 0.8580 - val_loss: 0.6310 - val_acc: 0.8018
Epoch 40/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3961 - acc: 0.8594 - val_loss: 0.6085 - val_acc: 0.8101
Epoch 41/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3873 - acc: 0.8618 - val_loss: 0.5783 - val_acc: 0.8139
Epoch 42/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3873 - acc: 0.8619 - val_loss: 0.5585 - val_acc: 0.8173
Epoch 43/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3837 - acc: 0.8651 - val_loss: 0.5960 - val_acc: 0.8139
Epoch 44/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3790 - acc: 0.8651 - val_loss: 0.6058 - val_acc: 0.8125
Epoch 45/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3793 - acc: 0.8653 - val_loss: 0.6481 - val_acc: 0.8028
Epoch 46/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3706 - acc: 0.8677 - val_loss: 0.5875 - val_acc: 0.8132
Epoch 47/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3692 - acc: 0.8685 - val_loss: 0.6258 - val_acc: 0.8101
Epoch 48/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3712 - acc: 0.8683 - val_loss: 0.6030 - val_acc: 0.8118
Epoch 49/50
390/390 [==============================] - 12s 31ms/step - loss: 0.3698 - acc: 0.8666 - val_loss: 0.5713 - val_acc: 0.8144
Epoch 50/50
390/390 [==============================] - 12s 32ms/step - loss: 0.3591 - acc: 0.8723 - val_loss: 0.5400 - val_acc: 0.8278
Model took 611.62 seconds to train

Accuracy on test data is: 82.78


```
