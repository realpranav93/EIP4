### Copy and paste your Logs for 20 epochs:



```
/usr/local/lib/python3.6/dist-packages/ipykernel_launcher.py:8: UserWarning: Update your `Conv2D` call to the Keras 2 API: `Conv2D(10, (3, 3), activation="relu", input_shape=(28, 28, 1..., use_bias=False)`
  

Model: "sequential_2"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_9 (Conv2D)            (None, 26, 26, 10)        90        
_________________________________________________________________
batch_normalization_8 (Batch (None, 26, 26, 10)        40        
_________________________________________________________________
conv2d_10 (Conv2D)           (None, 24, 24, 18)        1620      
_________________________________________________________________
batch_normalization_9 (Batch (None, 24, 24, 18)        72        
_________________________________________________________________
conv2d_11 (Conv2D)           (None, 22, 22, 18)        2916      
_________________________________________________________________
batch_normalization_10 (Batc (None, 22, 22, 18)        72        
_________________________________________________________________
dropout_3 (Dropout)          (None, 22, 22, 18)        0         
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 11, 11, 18)        0         
_________________________________________________________________
conv2d_12 (Conv2D)           (None, 11, 11, 10)        180       
_________________________________________________________________
batch_normalization_11 (Batc (None, 11, 11, 10)        40        
_________________________________________________________________
conv2d_13 (Conv2D)           (None, 9, 9, 16)          1440      
_________________________________________________________________
batch_normalization_12 (Batc (None, 9, 9, 16)          64        
_________________________________________________________________
conv2d_14 (Conv2D)           (None, 7, 7, 18)          2592      
_________________________________________________________________
dropout_4 (Dropout)          (None, 7, 7, 18)          0         
_________________________________________________________________
batch_normalization_13 (Batc (None, 7, 7, 18)          72        
_________________________________________________________________
conv2d_15 (Conv2D)           (None, 7, 7, 10)          180       
_________________________________________________________________
batch_normalization_14 (Batc (None, 7, 7, 10)          40        
_________________________________________________________________
conv2d_16 (Conv2D)           (None, 1, 1, 10)          4910      
_________________________________________________________________
flatten_2 (Flatten)          (None, 10)                0         
_________________________________________________________________
activation_2 (Activation)    (None, 10)                0         
=================================================================
Total params: 14,328
Trainable params: 14,128
Non-trainable params: 200
_________________________________________________________________
Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 7s 113us/step - loss: 0.1650 - acc: 0.9476 - val_loss: 0.0544 - val_acc: 0.9820
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0544 - acc: 0.9834 - val_loss: 0.0335 - val_acc: 0.9890
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0413 - acc: 0.9871 - val_loss: 0.0327 - val_acc: 0.9901
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0338 - acc: 0.9892 - val_loss: 0.0343 - val_acc: 0.9894
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0295 - acc: 0.9905 - val_loss: 0.0313 - val_acc: 0.9898
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0263 - acc: 0.9913 - val_loss: 0.0237 - val_acc: 0.9928
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0234 - acc: 0.9925 - val_loss: 0.0250 - val_acc: 0.9918
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 6s 92us/step - loss: 0.0200 - acc: 0.9934 - val_loss: 0.0230 - val_acc: 0.9928
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 5s 91us/step - loss: 0.0194 - acc: 0.9939 - val_loss: 0.0265 - val_acc: 0.9924
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0173 - acc: 0.9945 - val_loss: 0.0219 - val_acc: 0.9934
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0167 - acc: 0.9943 - val_loss: 0.0262 - val_acc: 0.9929
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0153 - acc: 0.9949 - val_loss: 0.0229 - val_acc: 0.9926
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0147 - acc: 0.9953 - val_loss: 0.0215 - val_acc: 0.9936
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 5s 87us/step - loss: 0.0127 - acc: 0.9959 - val_loss: 0.0224 - val_acc: 0.9938
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0117 - acc: 0.9963 - val_loss: 0.0225 - val_acc: 0.9940
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0116 - acc: 0.9963 - val_loss: 0.0233 - val_acc: 0.9935
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0119 - acc: 0.9962 - val_loss: 0.0257 - val_acc: 0.9933
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0106 - acc: 0.9965 - val_loss: 0.0244 - val_acc: 0.9934
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0098 - acc: 0.9971 - val_loss: 0.0216 - val_acc: 0.9935
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 5s 87us/step - loss: 0.0094 - acc: 0.9968 - val_loss: 0.0214 - val_acc: 0.9937
```
### Copy and paste the result of your model.evaluate (on test data): 

```
[0.021371671529706874, 0.9937]
```

### Strategy you have taken to achieve the said results:

1. Started with an architecture where we expand in number of kernels using 3X3 kernels and then contract the kernels using a 1X1 layer.
2. Now given that MNIST is fairly simple data, I have started with less number of kernel(10) to start instead of traditional 32 kernels.
3. Then built architecture with 13.2K parameters and trained the model with out of bound validation accuracy reaching ~99.3%. 
4. Increased the parameters to 14.2K parameters and so model training plateau after 14th epoch at 99.35%. My hypothesis is to increase regualarization and bring testing accuracy near to training acuracy which was very high at ~99.8%
5. So, finally increased the `Dropout % from 15% to 20%` and finally acheived the 99.4% on 16th Epoch.

