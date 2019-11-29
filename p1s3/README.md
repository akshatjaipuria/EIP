Accuracy on test data is: 82.55

model = Sequential()
model.add(SeparableConv2D(32, 3, 3, border_mode='same', input_shape=(32, 32, 3), use_bias=False, kernel_regularizer=l2(0.01))) #32 #3
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(SeparableConv2D(32, 3, 3, border_mode='same', use_bias=False, kernel_regularizer=l2(0.01))) #32 #5
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(SeparableConv2D(32, 3, 3, use_bias=False, kernel_regularizer=l2(0.01))) #30 #7
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(MaxPooling2D(pool_size=(2, 2))) #15 #8

model.add(SeparableConv2D(64, 3, 3, border_mode='same', use_bias=False, kernel_regularizer=l2(0.01))) #15 #12
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(SeparableConv2D(64, 3, 3, border_mode='same', use_bias=False, kernel_regularizer=l2(0.01))) #15 #16
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(SeparableConv2D(64, 3, 3, use_bias=False, kernel_regularizer=l2(0.01))) #13 #20
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(MaxPooling2D(pool_size=(2, 2))) #6 #22

model.add(SeparableConv2D(128, 3, 3, border_mode='same', use_bias=False, kernel_regularizer=l2(0.01))) #6 #30
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(SeparableConv2D(128, 3, 3, border_mode='same', use_bias=False, kernel_regularizer=l2(0.01))) #6 #38
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(SeparableConv2D(256, 3, 3, use_bias=False, kernel_regularizer=l2(0.01))) #4 #46
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.2))
model.add(MaxPooling2D(pool_size=(2, 2))) #2 #50

model.add(SeparableConv2D(num_classes, 1, 1)) #2 #50

model.add(GlobalAveragePooling2D())
model.add(Activation('softmax'))


Epoch 1/50

Epoch 00001: LearningRateScheduler setting learning rate to 0.005.
390/390 [==============================] - 35s 90ms/step - loss: 1.3859 - acc: 0.4925 - val_loss: 1.8355 - val_acc: 0.5350
Epoch 2/50

Epoch 00002: LearningRateScheduler setting learning rate to 0.0047619048.
390/390 [==============================] - 30s 77ms/step - loss: 1.0295 - acc: 0.6324 - val_loss: 1.2800 - val_acc: 0.5931
Epoch 3/50

Epoch 00003: LearningRateScheduler setting learning rate to 0.0045454545.
390/390 [==============================] - 30s 78ms/step - loss: 0.8946 - acc: 0.6851 - val_loss: 0.8385 - val_acc: 0.7061
Epoch 4/50

Epoch 00004: LearningRateScheduler setting learning rate to 0.0043478261.
390/390 [==============================] - 30s 77ms/step - loss: 0.8060 - acc: 0.7174 - val_loss: 0.8949 - val_acc: 0.6972
Epoch 5/50

Epoch 00005: LearningRateScheduler setting learning rate to 0.0041666667.
390/390 [==============================] - 30s 77ms/step - loss: 0.7562 - acc: 0.7337 - val_loss: 0.7140 - val_acc: 0.7489
Epoch 6/50

Epoch 00006: LearningRateScheduler setting learning rate to 0.004.
390/390 [==============================] - 30s 77ms/step - loss: 0.7160 - acc: 0.7502 - val_loss: 0.7744 - val_acc: 0.7317
Epoch 7/50

Epoch 00007: LearningRateScheduler setting learning rate to 0.0038461538.
390/390 [==============================] - 30s 77ms/step - loss: 0.6896 - acc: 0.7582 - val_loss: 0.7542 - val_acc: 0.7404
Epoch 8/50

Epoch 00008: LearningRateScheduler setting learning rate to 0.0037037037.
390/390 [==============================] - 31s 78ms/step - loss: 0.6636 - acc: 0.7674 - val_loss: 0.7151 - val_acc: 0.7567
Epoch 9/50

Epoch 00009: LearningRateScheduler setting learning rate to 0.0035714286.
390/390 [==============================] - 30s 77ms/step - loss: 0.6409 - acc: 0.7758 - val_loss: 0.7262 - val_acc: 0.7457
Epoch 10/50

Epoch 00010: LearningRateScheduler setting learning rate to 0.0034482759.
390/390 [==============================] - 30s 78ms/step - loss: 0.6288 - acc: 0.7798 - val_loss: 0.6681 - val_acc: 0.7676
Epoch 11/50

Epoch 00011: LearningRateScheduler setting learning rate to 0.0033333333.
390/390 [==============================] - 30s 78ms/step - loss: 0.6037 - acc: 0.7879 - val_loss: 0.6043 - val_acc: 0.7913
Epoch 12/50

Epoch 00012: LearningRateScheduler setting learning rate to 0.0032258065.
390/390 [==============================] - 30s 78ms/step - loss: 0.5964 - acc: 0.7904 - val_loss: 0.6853 - val_acc: 0.7652
Epoch 13/50

Epoch 00013: LearningRateScheduler setting learning rate to 0.003125.
390/390 [==============================] - 30s 77ms/step - loss: 0.5819 - acc: 0.7962 - val_loss: 0.6178 - val_acc: 0.7867
Epoch 14/50

Epoch 00014: LearningRateScheduler setting learning rate to 0.003030303.
390/390 [==============================] - 30s 77ms/step - loss: 0.5699 - acc: 0.8000 - val_loss: 0.7288 - val_acc: 0.7434
Epoch 15/50

Epoch 00015: LearningRateScheduler setting learning rate to 0.0029411765.
390/390 [==============================] - 30s 78ms/step - loss: 0.5511 - acc: 0.8080 - val_loss: 0.6508 - val_acc: 0.7721
Epoch 16/50

Epoch 00016: LearningRateScheduler setting learning rate to 0.0028571429.
390/390 [==============================] - 30s 77ms/step - loss: 0.5482 - acc: 0.8090 - val_loss: 0.7601 - val_acc: 0.7407
Epoch 17/50

Epoch 00017: LearningRateScheduler setting learning rate to 0.0027777778.
390/390 [==============================] - 30s 78ms/step - loss: 0.5393 - acc: 0.8121 - val_loss: 0.5844 - val_acc: 0.7947
Epoch 18/50

Epoch 00018: LearningRateScheduler setting learning rate to 0.0027027027.
390/390 [==============================] - 31s 78ms/step - loss: 0.5315 - acc: 0.8122 - val_loss: 0.5495 - val_acc: 0.8072
Epoch 19/50

Epoch 00019: LearningRateScheduler setting learning rate to 0.0026315789.
390/390 [==============================] - 30s 77ms/step - loss: 0.5221 - acc: 0.8155 - val_loss: 0.7079 - val_acc: 0.7587
Epoch 20/50

Epoch 00020: LearningRateScheduler setting learning rate to 0.0025641026.
390/390 [==============================] - 30s 78ms/step - loss: 0.5164 - acc: 0.8181 - val_loss: 0.6303 - val_acc: 0.7831
Epoch 21/50

Epoch 00021: LearningRateScheduler setting learning rate to 0.0025.
390/390 [==============================] - 30s 77ms/step - loss: 0.5097 - acc: 0.8222 - val_loss: 0.5508 - val_acc: 0.8111
Epoch 22/50

Epoch 00022: LearningRateScheduler setting learning rate to 0.0024390244.
390/390 [==============================] - 30s 77ms/step - loss: 0.5010 - acc: 0.8249 - val_loss: 0.5542 - val_acc: 0.8045
Epoch 23/50

Epoch 00023: LearningRateScheduler setting learning rate to 0.0023809524.
390/390 [==============================] - 30s 78ms/step - loss: 0.4954 - acc: 0.8263 - val_loss: 0.6158 - val_acc: 0.7916
Epoch 24/50

Epoch 00024: LearningRateScheduler setting learning rate to 0.0023255814.
390/390 [==============================] - 30s 77ms/step - loss: 0.4907 - acc: 0.8276 - val_loss: 0.5539 - val_acc: 0.8096
Epoch 25/50

Epoch 00025: LearningRateScheduler setting learning rate to 0.0022727273.
390/390 [==============================] - 30s 78ms/step - loss: 0.4788 - acc: 0.8313 - val_loss: 0.6798 - val_acc: 0.7706
Epoch 26/50

Epoch 00026: LearningRateScheduler setting learning rate to 0.0022222222.
390/390 [==============================] - 30s 77ms/step - loss: 0.4764 - acc: 0.8321 - val_loss: 0.5365 - val_acc: 0.8184
Epoch 27/50

Epoch 00027: LearningRateScheduler setting learning rate to 0.002173913.
390/390 [==============================] - 30s 78ms/step - loss: 0.4700 - acc: 0.8338 - val_loss: 0.6254 - val_acc: 0.7881
Epoch 28/50

Epoch 00028: LearningRateScheduler setting learning rate to 0.0021276596.
390/390 [==============================] - 30s 78ms/step - loss: 0.4720 - acc: 0.8343 - val_loss: 0.5725 - val_acc: 0.8033
Epoch 29/50

Epoch 00029: LearningRateScheduler setting learning rate to 0.0020833333.
390/390 [==============================] - 30s 78ms/step - loss: 0.4560 - acc: 0.8400 - val_loss: 0.5361 - val_acc: 0.8179
Epoch 30/50

Epoch 00030: LearningRateScheduler setting learning rate to 0.0020408163.
390/390 [==============================] - 30s 78ms/step - loss: 0.4583 - acc: 0.8379 - val_loss: 0.5299 - val_acc: 0.8194
Epoch 31/50

Epoch 00031: LearningRateScheduler setting learning rate to 0.002.
390/390 [==============================] - 30s 77ms/step - loss: 0.4489 - acc: 0.8425 - val_loss: 0.6016 - val_acc: 0.7983
Epoch 32/50

Epoch 00032: LearningRateScheduler setting learning rate to 0.0019607843.
390/390 [==============================] - 31s 78ms/step - loss: 0.4553 - acc: 0.8395 - val_loss: 0.5238 - val_acc: 0.8213
Epoch 33/50

Epoch 00033: LearningRateScheduler setting learning rate to 0.0019230769.
390/390 [==============================] - 31s 78ms/step - loss: 0.4440 - acc: 0.8434 - val_loss: 0.5420 - val_acc: 0.8122
Epoch 34/50

Epoch 00034: LearningRateScheduler setting learning rate to 0.0018867925.
390/390 [==============================] - 30s 77ms/step - loss: 0.4396 - acc: 0.8460 - val_loss: 0.5480 - val_acc: 0.8126
Epoch 35/50

Epoch 00035: LearningRateScheduler setting learning rate to 0.0018518519.
390/390 [==============================] - 31s 78ms/step - loss: 0.4346 - acc: 0.8465 - val_loss: 0.5519 - val_acc: 0.8119
Epoch 36/50

Epoch 00036: LearningRateScheduler setting learning rate to 0.0018181818.
390/390 [==============================] - 30s 78ms/step - loss: 0.4321 - acc: 0.8477 - val_loss: 0.5408 - val_acc: 0.8126
Epoch 37/50

Epoch 00037: LearningRateScheduler setting learning rate to 0.0017857143.
390/390 [==============================] - 31s 79ms/step - loss: 0.4279 - acc: 0.8476 - val_loss: 0.5290 - val_acc: 0.8206
Epoch 38/50

Epoch 00038: LearningRateScheduler setting learning rate to 0.001754386.
390/390 [==============================] - 31s 78ms/step - loss: 0.4230 - acc: 0.8507 - val_loss: 0.5072 - val_acc: 0.8250
Epoch 39/50

Epoch 00039: LearningRateScheduler setting learning rate to 0.0017241379.
390/390 [==============================] - 31s 78ms/step - loss: 0.4214 - acc: 0.8513 - val_loss: 0.5131 - val_acc: 0.8249
Epoch 40/50

Epoch 00040: LearningRateScheduler setting learning rate to 0.0016949153.
390/390 [==============================] - 30s 78ms/step - loss: 0.4146 - acc: 0.8533 - val_loss: 0.5489 - val_acc: 0.8143
Epoch 41/50

Epoch 00041: LearningRateScheduler setting learning rate to 0.0016666667.
390/390 [==============================] - 30s 77ms/step - loss: 0.4159 - acc: 0.8541 - val_loss: 0.5254 - val_acc: 0.8207
Epoch 42/50

Epoch 00042: LearningRateScheduler setting learning rate to 0.0016393443.
390/390 [==============================] - 30s 78ms/step - loss: 0.4133 - acc: 0.8532 - val_loss: 0.4817 - val_acc: 0.8350
Epoch 43/50

Epoch 00043: LearningRateScheduler setting learning rate to 0.0016129032.
390/390 [==============================] - 30s 77ms/step - loss: 0.4094 - acc: 0.8558 - val_loss: 0.5149 - val_acc: 0.8216
Epoch 44/50

Epoch 00044: LearningRateScheduler setting learning rate to 0.0015873016.
390/390 [==============================] - 30s 77ms/step - loss: 0.4105 - acc: 0.8537 - val_loss: 0.4929 - val_acc: 0.8301
Epoch 45/50

Epoch 00045: LearningRateScheduler setting learning rate to 0.0015625.
390/390 [==============================] - 30s 78ms/step - loss: 0.4035 - acc: 0.8582 - val_loss: 0.5445 - val_acc: 0.8149
Epoch 46/50

Epoch 00046: LearningRateScheduler setting learning rate to 0.0015384615.
390/390 [==============================] - 31s 78ms/step - loss: 0.4063 - acc: 0.8556 - val_loss: 0.5011 - val_acc: 0.8282
Epoch 47/50

Epoch 00047: LearningRateScheduler setting learning rate to 0.0015151515.
390/390 [==============================] - 30s 77ms/step - loss: 0.3963 - acc: 0.8587 - val_loss: 0.4890 - val_acc: 0.8339
Epoch 48/50

Epoch 00048: LearningRateScheduler setting learning rate to 0.0014925373.
390/390 [==============================] - 31s 79ms/step - loss: 0.3969 - acc: 0.8604 - val_loss: 0.4779 - val_acc: 0.8374
Epoch 49/50

Epoch 00049: LearningRateScheduler setting learning rate to 0.0014705882.
390/390 [==============================] - 30s 77ms/step - loss: 0.3963 - acc: 0.8599 - val_loss: 0.5145 - val_acc: 0.8244
Epoch 50/50

Epoch 00050: LearningRateScheduler setting learning rate to 0.0014492754.
390/390 [==============================] - 30s 78ms/step - loss: 0.3970 - acc: 0.8601 - val_loss: 0.4848 - val_acc: 0.8364
Model took 1521.19 seconds to train

Accuracy on test data is: 83.64
