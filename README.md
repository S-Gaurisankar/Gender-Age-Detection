# Gender-Age-detection
This repository is part of a deep learning project that focuses on predicting the gender and age of individuals using the Talhassner dataset.
The project employs convolutional neural networks (CNNs) and transfer learning techniques to achieve accurate and reliable predictions.

## **Dataset**
The Talhassner dataset is a well-known collection of facial images that encompasses a diverse range of individuals across various age groups and genders. It provides an ideal foundation for training and evaluating our prediction model. The dataset is available here: https://talhassner.github.io/home/projects/Adience/Adience-data.html

## Model Architecture
### Gender -
Model: "sequential"
```
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 46, 46, 36)        360       
                                                                 
 conv2d_1 (Conv2D)           (None, 44, 44, 48)        15600     
                                                                 
 max_pooling2d (MaxPooling2D  (None, 22, 22, 48)       0         
 )                                                               
                                                                 
 dropout (Dropout)           (None, 22, 22, 48)        0         
                                                                 
 conv2d_2 (Conv2D)           (None, 20, 20, 72)        31176     
                                                                 
 conv2d_3 (Conv2D)           (None, 18, 18, 72)        46728     
                                                                 
 max_pooling2d_1 (MaxPooling  (None, 9, 9, 72)         0         
 2D)                                                             
                                                                 
 dropout_1 (Dropout)         (None, 9, 9, 72)          0         
                                                                 
 flatten (Flatten)           (None, 5832)              0         
                                                                 
 dense (Dense)               (None, 2304)              13439232
```

### Age -
```
Model: "sequential_1"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_4 (Conv2D)           (None, 48, 48, 32)        320       
                                                                 
 batch_normalization (BatchN  (None, 48, 48, 32)       128       
 ormalization)                                                   
                                                                 
 max_pooling2d_2 (MaxPooling  (None, 24, 24, 32)       0         
 2D)                                                             
                                                                 
 global_average_pooling2d (G  (None, 32)               0         
 lobalAveragePooling2D)                                          
                                                                 
 flatten_1 (Flatten)         (None, 32)                0         
                                                                 
 dense_2 (Dense)             (None, 128)               4224      
                                                                 
 batch_normalization_1 (Batc  (None, 128)              512       
 hNormalization)                                                 
                                                                 
 dropout_2 (Dropout)         (None, 128)               0         
                                                                 
 dense_3 (Dense)             (None, 64)                8256
```



