# AlexNet Implementation from Scratch

A PyTorch implementation of AlexNet from the groundbreaking 2012 paper ["ImageNet Classification with Deep Convolutional Neural Networks"](https://papers.nips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf) by Alex Krizhevsky, Ilya Sutskever, and Geoffrey E. Hinton.

![AlexNet Architecture](https://miro.medium.com/v2/resize:fit:1400/1*qyc21qM0oxWEuRaj-XJKcw.png)

## 📖 Paper Summary

AlexNet introduced several key innovations that made deep learning practical:
- **First large-scale CNN**: 8 layers, 60 million parameters
- **ReLU activation**: 6x faster training than traditional tanh/sigmoid  
- **Dropout regularization**: Prevents overfitting in fully-connected layers
- **GPU training**: Pioneered multi-GPU parallel training
- **Data augmentation**: Dramatically increased effective dataset size

**Original Results**: 15.3% top-5 error on ImageNet (vs 26.2% for second place)

## 🚀 Features

- **Faithful architecture**: 5 convolutional + 3 fully-connected layers
- **All original components**: ReLU, LRN, overlapping pooling, dropout
- **Proper weight initialization**: As described in paper
- **Data augmentation**: Random crops, flipping, and PCA color augmentation
- **Training pipeline**: SGD with momentum, weight decay, step LR scheduling
- **10-crop testing**: Same evaluation strategy as original paper
- **Visualization tools**: Feature maps and filter visualization

## 🏗️ Architecture
Input (224×224×3)
↓
Conv1: 96×11×11, stride=4, ReLU, LRN, MaxPool
↓
Conv2: 256×5×5, ReLU, LRN, MaxPool
↓
Conv3: 384×3×3, ReLU
↓
Conv4: 384×3×3, ReLU
↓
Conv5: 256×3×3, ReLU, MaxPool
↓
Flatten → 9216 units
↓
FC6: 4096, ReLU, Dropout
↓
FC7: 4096, ReLU, Dropout
↓
FC8: 1000 classes

