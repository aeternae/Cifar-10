# Cifar-10
对CIFAR-10数据集的分类是机器学习中一个公开的基准测试问题，其任务是对一组32x32RGB的图像进行分类，这些图像涵盖了10个类别：飞机，汽车，鸟，猫，鹿，狗，青蛙，马，船以及卡车。
![](./pic/dataset.png)

#### 为了熟悉掌握经典的DeepLearning Model以及Tensorflow的使用，我构建了多种模型对cifar10数据集进行分类。<br>
#### 在终端运行步骤如下：python Vgg19.py (以Vgg19模型为例）

```
!python Vgg19.py
Using TensorFlow backend.

======Loading data======
Loading ../input0/data_batch_1 : 10000.
Loading ../input0/data_batch_2 : 10000.
Loading ../input0/data_batch_3 : 10000.
Loading ../input0/data_batch_4 : 10000.
Loading ../input0/data_batch_5 : 10000.
Loading ../input0/test_batch : 10000.
Train data: (50000, 32, 32, 3) (50000, 10)
Test data : (10000, 32, 32, 3) (10000, 10)
======Load finished======
======Shuffling data======
======Prepare Finished======
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
block1_conv1 (Conv2D)        (None, 32, 32, 64)        1792      
_________________________________________________________________
batch_normalization_1 (Batch (None, 32, 32, 64)        256       
_________________________________________________________________
activation_1 (Activation)    (None, 32, 32, 64)        0         
_________________________________________________________________
block1_conv2 (Conv2D)        (None, 32, 32, 64)        36928     
_________________________________________________________________
batch_normalization_2 (Batch (None, 32, 32, 64)        256       
_________________________________________________________________
activation_2 (Activation)    (None, 32, 32, 64)        0         
_________________________________________________________________
block1_pool (MaxPooling2D)   (None, 16, 16, 64)        0         
_________________________________________________________________
block2_conv1 (Conv2D)        (None, 16, 16, 128)       73856     
_________________________________________________________________
batch_normalization_3 (Batch (None, 16, 16, 128)       512       
_________________________________________________________________
activation_3 (Activation)    (None, 16, 16, 128)       0         
_________________________________________________________________
block2_conv2 (Conv2D)        (None, 16, 16, 128)       147584    
_________________________________________________________________
batch_normalization_4 (Batch (None, 16, 16, 128)       512       
_________________________________________________________________
activation_4 (Activation)    (None, 16, 16, 128)       0         
_________________________________________________________________
block2_pool (MaxPooling2D)   (None, 8, 8, 128)         0         
_________________________________________________________________
block3_conv1 (Conv2D)        (None, 8, 8, 256)         295168    
_________________________________________________________________
batch_normalization_5 (Batch (None, 8, 8, 256)         1024      
_________________________________________________________________
activation_5 (Activation)    (None, 8, 8, 256)         0         
_________________________________________________________________
block3_conv2 (Conv2D)        (None, 8, 8, 256)         590080    
_________________________________________________________________
batch_normalization_6 (Batch (None, 8, 8, 256)         1024      
_________________________________________________________________
activation_6 (Activation)    (None, 8, 8, 256)         0         
_________________________________________________________________
block3_conv3 (Conv2D)        (None, 8, 8, 256)         590080    
_________________________________________________________________
batch_normalization_7 (Batch (None, 8, 8, 256)         1024      
_________________________________________________________________
activation_7 (Activation)    (None, 8, 8, 256)         0         
_________________________________________________________________
block3_conv4 (Conv2D)        (None, 8, 8, 256)         590080    
_________________________________________________________________
batch_normalization_8 (Batch (None, 8, 8, 256)         1024      
_________________________________________________________________
activation_8 (Activation)    (None, 8, 8, 256)         0         
_________________________________________________________________
block3_pool (MaxPooling2D)   (None, 4, 4, 256)         0         
_________________________________________________________________
block4_conv1 (Conv2D)        (None, 4, 4, 512)         1180160   
_________________________________________________________________
batch_normalization_9 (Batch (None, 4, 4, 512)         2048      
_________________________________________________________________
activation_9 (Activation)    (None, 4, 4, 512)         0         
_________________________________________________________________
block4_conv2 (Conv2D)        (None, 4, 4, 512)         2359808   
_________________________________________________________________
batch_normalization_10 (Batc (None, 4, 4, 512)         2048      
_________________________________________________________________
activation_10 (Activation)   (None, 4, 4, 512)         0         
_________________________________________________________________
block4_conv3 (Conv2D)        (None, 4, 4, 512)         2359808   
_________________________________________________________________
batch_normalization_11 (Batc (None, 4, 4, 512)         2048      
_________________________________________________________________
activation_11 (Activation)   (None, 4, 4, 512)         0         
_________________________________________________________________
block4_conv4 (Conv2D)        (None, 4, 4, 512)         2359808   
_________________________________________________________________
batch_normalization_12 (Batc (None, 4, 4, 512)         2048      
_________________________________________________________________
activation_12 (Activation)   (None, 4, 4, 512)         0         
_________________________________________________________________
block4_pool (MaxPooling2D)   (None, 2, 2, 512)         0         
_________________________________________________________________
block5_conv1 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
batch_normalization_13 (Batc (None, 2, 2, 512)         2048      
_________________________________________________________________
activation_13 (Activation)   (None, 2, 2, 512)         0         
_________________________________________________________________
block5_conv2 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
batch_normalization_14 (Batc (None, 2, 2, 512)         2048      
_________________________________________________________________
activation_14 (Activation)   (None, 2, 2, 512)         0         
_________________________________________________________________
block5_conv3 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
batch_normalization_15 (Batc (None, 2, 2, 512)         2048      
_________________________________________________________________
activation_15 (Activation)   (None, 2, 2, 512)         0         
_________________________________________________________________
block5_conv4 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
batch_normalization_16 (Batc (None, 2, 2, 512)         2048      
_________________________________________________________________
activation_16 (Activation)   (None, 2, 2, 512)         0         
_________________________________________________________________
block5_pool (MaxPooling2D)   (None, 1, 1, 512)         0         
_________________________________________________________________
flatten (Flatten)            (None, 512)               0         
_________________________________________________________________
fc_cifa10 (Dense)            (None, 4096)              2101248   
_________________________________________________________________
batch_normalization_17 (Batc (None, 4096)              16384     
_________________________________________________________________
activation_17 (Activation)   (None, 4096)              0         
_________________________________________________________________
dropout_1 (Dropout)          (None, 4096)              0         
_________________________________________________________________
fc2 (Dense)                  (None, 4096)              16781312  
_________________________________________________________________
batch_normalization_18 (Batc (None, 4096)              16384     
_________________________________________________________________
activation_18 (Activation)   (None, 4096)              0         
_________________________________________________________________
dropout_2 (Dropout)          (None, 4096)              0         
_________________________________________________________________
predictions_cifa10 (Dense)   (None, 10)                40970     
_________________________________________________________________
batch_normalization_19 (Batc (None, 10)                40        
_________________________________________________________________
activation_19 (Activation)   (None, 10)                0         
=================================================================
Total params: 39,002,738
Trainable params: 38,975,326
Non-trainable params: 27,412
_________________________________________________________________
Using real-time data augmentation.
Epoch 1/100
391/391 [==============================] - 43s 111ms/step - loss: 2.4759 - acc: 0.5209 - val_loss: 3.6772 - val_acc: 0.4180
Epoch 2/100
391/391 [==============================] - 36s 92ms/step - loss: 2.0195 - acc: 0.6558 - val_loss: 2.1722 - val_acc: 0.6227
Epoch 3/100
391/391 [==============================] - 36s 92ms/step - loss: 1.8080 - acc: 0.7055 - val_loss: 2.3335 - val_acc: 0.5706
Epoch 4/100
391/391 [==============================] - 36s 92ms/step - loss: 1.6727 - acc: 0.7231 - val_loss: 1.7589 - val_acc: 0.6809
Epoch 5/100
391/391 [==============================] - 36s 92ms/step - loss: 1.5210 - acc: 0.7493 - val_loss: 1.6463 - val_acc: 0.6937
Epoch 6/100
391/391 [==============================] - 36s 91ms/step - loss: 1.4301 - acc: 0.7607 - val_loss: 1.9281 - val_acc: 0.6090
Epoch 7/100
391/391 [==============================] - 36s 91ms/step - loss: 1.3477 - acc: 0.7723 - val_loss: 1.5058 - val_acc: 0.7201
Epoch 8/100
391/391 [==============================] - 36s 92ms/step - loss: 1.2675 - acc: 0.7809 - val_loss: 1.6144 - val_acc: 0.6805
Epoch 9/100
391/391 [==============================] - 36s 92ms/step - loss: 1.2028 - acc: 0.7910 - val_loss: 2.0555 - val_acc: 0.5970
Epoch 10/100
391/391 [==============================] - 36s 91ms/step - loss: 1.1809 - acc: 0.7904 - val_loss: 1.4655 - val_acc: 0.6751
...... ......
Epoch 90/100
391/391 [==============================] - 38s 98ms/step - loss: 0.3097 - acc: 0.9912 - val_loss: 0.5824 - val_acc: 0.9182
Epoch 91/100
391/391 [==============================] - 33s 85ms/step - loss: 0.3085 - acc: 0.9908 - val_loss: 0.5806 - val_acc: 0.9177
Epoch 92/100
391/391 [==============================] - 38s 97ms/step - loss: 0.3064 - acc: 0.9918 - val_loss: 0.5804 - val_acc: 0.9198
Epoch 93/100
391/391 [==============================] - 33s 85ms/step - loss: 0.3038 - acc: 0.9922 - val_loss: 0.5804 - val_acc: 0.9199
Epoch 94/100
391/391 [==============================] - 38s 97ms/step - loss: 0.3059 - acc: 0.9920 - val_loss: 0.5903 - val_acc: 0.9182
Epoch 95/100
391/391 [==============================] - 33s 85ms/step - loss: 0.3013 - acc: 0.9937 - val_loss: 0.5855 - val_acc: 0.9191
Epoch 96/100
391/391 [==============================] - 38s 98ms/step - loss: 0.3042 - acc: 0.9914 - val_loss: 0.5829 - val_acc: 0.9191
Epoch 97/100
391/391 [==============================] - 33s 85ms/step - loss: 0.3043 - acc: 0.9912 - val_loss: 0.5804 - val_acc: 0.9198
Epoch 98/100
391/391 [==============================] - 38s 97ms/step - loss: 0.3010 - acc: 0.9926 - val_loss: 0.5804 - val_acc: 0.9209
Epoch 99/100
391/391 [==============================] - 33s 85ms/step - loss: 0.3004 - acc: 0.9928 - val_loss: 0.5821 - val_acc: 0.9196
Epoch 100/100
391/391 [==============================] - 38s 97ms/step - loss: 0.2992 - acc: 0.9927 - val_loss: 0.5814 - val_acc: 0.9211
```

![](./pic/history.png)
