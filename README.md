# MSCS18045_COVID19_DLSpring2020
This repository contains the Fine-tuned VGG16 &amp; Resnet-18 Models for COVID-detection through chest X-Ray images.
# Pre-Requisites:
- Python 3.7+
- Pytorch
- Numpy
- Google Colab(Optinal)
- Gpu (Optional)

# Dataset Details:
| Class    | # of images in training set | # of images in validation set | # of images in test set |
|----------|-----------------------------|-------------------------------|-------------------------|
| Infected | 4,919                       | 615                           | 615                     |
| Normal   | 7,081                       | 885                           | 885                     |


# Task 1: Training Only FC layers
## VGG16


### Confusion Matrix


|     Model: VGG16    |    Data          |    Tp      |    Tn      |    Fp     |    Fn     |
|:-------------------:|------------------|------------|------------|-----------|-----------|
|                     |    Training      |    6390    |    3959    |    691    |    960    |
|                     |    Validation    |    794     |    502     |    91     |    113    |
|                     |    Test          |    860     |    536     |    25     |    79     |


### Results

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

### Confusion Matrix:

|        Model   Resnet18    |    Data          |    Tp      |    Tn      |    Fp     |    Fn     |
|----------------------------|------------------|------------|------------|-----------|-----------|
|                            |    Training      |    6200    |    4122    |    881    |    797    |
|                            |    Validation    |    751     |    526     |    134    |    89     |
|                            |    Test          |    811     |    556     |    74     |    59     |


### Results: 

|            Model   Renet18    |    Data          |    Accuracy    |    Precision    |    Recall    |    F1-Measure    |
|-----------------------------|------------------|----------------|-----------------|--------------|------------------|
|                             |    Training      |    86.01       |    87.55        |    88.5      |    88.09         |
|                             |    Validation    |    85.13       |    84.85        |    89.40     |    87.07         |
|                             |    Test          |    91.3        |    91.6         |    93.21     |    92.42         |



# Task 2: Training Different Convolutional/FC layers

For this task, Three different tasks have been performed by unfreezing the different layers. These tasks can be categorized as following: 

- Unfreezing only one Convolutional Layer for VGG16/Resnet18.
- Unfreezing more than one Convolutional(s) for VGG16/Resnet18.
- Training on whole VGG16/Resnet18 model with All layers. 

I am only showing the results here for training on All Network. 

## VGG16
### Confusion Matrix:

|        Model   VGG16    |    Data          |    Tp      |    Tn      |    Fp     |    Fn     |
|-------------------------|------------------|------------|------------|-----------|-----------|
|                         |    Training      |    6825    |    4304    |    256    |    615    |
|                         |    Validation    |    853     |    520     |    32     |    95     |
|                         |    Test          |    878     |    582     |    7      |    33     |


### Results:

|            Model   VGG16    |    Data          |    Accuracy    |    Precision    |    Recall    |    F1-Measure    |
|-----------------------------|------------------|----------------|-----------------|--------------|------------------|
|                             |    Training      |    92.7        |    96.38        |    91.73     |    94.00         |
|                             |    Validation    |    91.53       |    96.38        |    89.97     |    93.07         |
|                             |    Test          |    97.33       |    99.29        |    96.37     |    97.77         |


## Resnet 18

### Confusion Matrix:

|        Model   Resnet18    |    Data          |    Tp      |    Tn      |    Fp     |    Fn     |
|----------------------------|------------------|------------|------------|-----------|-----------|
|                            |    Training      |    6634    |    4429    |    447    |    490    |
|                            |    Validation    |    805     |    557     |    80     |    58     |
|                            |    Test          |    865     |    585     |    20     |    30     |


### Results:

|            Model   Resnet18    |    Data          |    Accuracy    |    Precision    |    Recall    |    F1-Measure    |
|--------------------------------|------------------|----------------|-----------------|--------------|------------------|
|                                |    Training      |    92.19       |    93.68        |    93.12     |    93.40         |
|                                |    Validation    |    90.8        |    90.9         |    93..27    |    92.105        |
|                                |    Test          |    96.66       |    97.74        |    96.64     |    97.19         |



Note:This repository contains code and results for COVID-19 classification assignment by Deep Learning Spring 2020 course offered at Information Technology University, Lahore, Pakistan. This assignment is only for learning purposes and is not intended to be used for clinical purposes.

