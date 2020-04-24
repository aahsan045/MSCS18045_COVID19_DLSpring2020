# MSCS18045_COVID19_DLSpring2020
This repository contains the Fine-tuned VGG16 &amp; Resnet-18 Models for COVID-detection through chest X-Ray images. 

# Task 1: Training Only FC layers
## VGG16
- Number of Epochs=10
- Learning Rate=0.001
- Momentum=0.9
- Optimizer =SGD
- Number of Neurons in second Last layer= 550
- Batch-Size=128




|     Model: VGG16    |    Data          |    Tp      |    Tn      |    Fp     |    Fn     |
|:-------------------:|------------------|------------|------------|-----------|-----------|
|                     |    Training      |    6390    |    3959    |    691    |    960    |
|                     |    Validation    |    794     |    502     |    91     |    113    |
|                     |    Test          |    860     |    536     |    25     |    79     |




|            Model   VGG16    |    Data          |    Accuracy    |    Precision    |    Recall    |    F1-Measure    |
|-----------------------------|------------------|----------------|-----------------|--------------|------------------|
|                             |    Training      |    86.24       |    90.24        |    86.93     |    88.55         |
|                             |    Validation    |    86.4        |    89.71        |    87.54     |    88.61         |
|                             |    Test          |    93.06       |    97.17        |    91.58     |    94.29         |


## Resnet18
- Number of Epochs=10
- Learning Rate=0.001
- Momentum=0.9
- Optimizer =SGD
- Number of Neurons in second Last layer= 550
- Batch-Size=128



|        Model   Resnet18    |    Data          |    Tp      |    Tn      |    Fp     |    Fn     |
|----------------------------|------------------|------------|------------|-----------|-----------|
|                            |    Training      |    6200    |    4122    |    881    |    797    |
|                            |    Validation    |    751     |    526     |    134    |    89     |
|                            |    Test          |    811     |    556     |    74     |    59     |



|            Model   Renet18    |    Data          |    Accuracy    |    Precision    |    Recall    |    F1-Measure    |
|-----------------------------|------------------|----------------|-----------------|--------------|------------------|
|                             |    Training      |    86.01       |    87.55        |    88.5      |    88.09         |
|                             |    Validation    |    85.13       |    84.85        |    89.40     |    87.07         |
|                             |    Test          |    91.3        |    91.6         |    93.21     |    92.42         |



# Task 2: Training Different Convolutional/FC layers



Note:This repository contains code and results for COVID-19 classification assignment by Deep Learning Spring 2020 course offered at Information Technology University, Lahore, Pakistan. This assignment is only for learning purposes and is not intended to be used for clinical purposes.

