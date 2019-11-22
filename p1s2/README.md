Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.001.
60000/60000 [==============================] - 14s 239us/step - loss: 0.0252 - acc: 0.9914 - val_loss: 0.0247 - val_acc: 0.9931
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0007581501.
60000/60000 [==============================] - 7s 123us/step - loss: 0.0232 - acc: 0.9927 - val_loss: 0.0228 - val_acc: 0.9935
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0006105006.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0215 - acc: 0.9930 - val_loss: 0.0216 - val_acc: 0.9935
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0005109862.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0194 - acc: 0.9937 - val_loss: 0.0212 - val_acc: 0.9930
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0004393673.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0194 - acc: 0.9939 - val_loss: 0.0212 - val_acc: 0.9932
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0003853565.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0172 - acc: 0.9944 - val_loss: 0.0218 - val_acc: 0.9930
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0003431709.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0173 - acc: 0.9941 - val_loss: 0.0204 - val_acc: 0.9932
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0003093102.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0168 - acc: 0.9948 - val_loss: 0.0212 - val_acc: 0.9935
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0002815315.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0161 - acc: 0.9947 - val_loss: 0.0219 - val_acc: 0.9927
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0002583312.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0158 - acc: 0.9947 - val_loss: 0.0201 - val_acc: 0.9943
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0002386635.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0154 - acc: 0.9946 - val_loss: 0.0203 - val_acc: 0.9934
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.0002217787.
60000/60000 [==============================] - 7s 123us/step - loss: 0.0144 - acc: 0.9952 - val_loss: 0.0188 - val_acc: 0.9937
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0002071251.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0143 - acc: 0.9953 - val_loss: 0.0191 - val_acc: 0.9940
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0001942879.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0139 - acc: 0.9953 - val_loss: 0.0191 - val_acc: 0.9943
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0001829491.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0143 - acc: 0.9954 - val_loss: 0.0201 - val_acc: 0.9941
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0001728608.
60000/60000 [==============================] - 7s 123us/step - loss: 0.0132 - acc: 0.9957 - val_loss: 0.0186 - val_acc: 0.9942
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000163827.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0135 - acc: 0.9957 - val_loss: 0.0194 - val_acc: 0.9933
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0001556905.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0143 - acc: 0.9955 - val_loss: 0.0183 - val_acc: 0.9941
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0001483239.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0125 - acc: 0.9961 - val_loss: 0.0186 - val_acc: 0.9939
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000141623.
60000/60000 [==============================] - 7s 123us/step - loss: 0.0130 - acc: 0.9957 - val_loss: 0.0186 - val_acc: 0.9937


[0.018621038327012503, 0.9937]


I would like to tell a bit about what I infered while going through the 8 codes, that helped me figure out the approach about how to  build the model from ground.

Initially, we had a very basic, random model. SO we increased the no. of channels and depth to have a proper model. Now, we had to use small number of parameters, therefore we reduced them by reducing the no. of layers and no. of channels. Though, this could have affected our model a lot, it didnt. This led us to a conclusion that our image dataset might not be complex enough to require very large no. of feature maps and a receptive field of 7x7 was enough to capture the complex features. Now, batch normalization could help our model learn easily by normalizing the images along with small inclease in the no. of channels helped significantly. But by now, we could easily see some over fitting as though the changes showed significant upgrade in test accuracy, it didn't work well with the test. Regularization was an option here, so we went for dropout. Though this reduced the gap between the two accuracies, the training loss was not getting significant reductions in the later epoches. Therefore, using lesser learning rates helped skip local minima trap and adjusting the model a bit in terms of no. of parameters led us to a good result.

This understanding helped me to begin from scratch and analyse, what the model was actually going through and how to overcome that and build the required model.
