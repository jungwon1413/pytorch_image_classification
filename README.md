# PyTorch Image Classification on __CUSTOM__ Fashion MNIST

## Models
This repo is for self-learning on 'image classification' methods, using deep learning. I consists for 5 different models:
- WideResNet
- DenseNet
- Dual Path Network (DualPathNet)
- ResNet w/ Shake-Shake regularization (96 Dims)
- ResNet w/ Shake-Shake regularization (64 Dims)

## Hardware
The models are trained using following hardware:
- 1080 ti (dual-GPU is ready, but could not use due to error issue)
- Ryzen 2700X
- 64GB RAM

## Benchmarks
Here are some benchmarks of the models I trained.

| Model Name | # of Parameters | Accuracy (Prec@1) | Time Estimated (Not Measured) | # of Epochs |
| ------------- | --------------- | :---------------: | ----------------------: | -------------- |
| WideResNet | 36478906 | 93.2775 | Around 7 Hrs | 200
| DenseNet   | 768730 | 93.77 | Around 3~4 Hrs | 300
| DualPathNet | 47751450 | 93.21 | Around 6 Hrs (Not sure) | 200
| ResNet w/ Shake-Shake (96d) | 26330026 | 93.7275 | Around 40 Hrs | 1800
| ResNet w/ Shake-Shake (96d) | 11708362 | 93.725 | Around 25 Hrs | 1800

## Hyperparameters
! Notice: Fashion-MNIST dataset has new ratio (Train 30000, Test 40000) !

- WideResNet

| Seed # | Epochs | Mini-Batch Size | Initial lr | Momentum | Nesterov | 
| ---- | ---- | ---- | ---- | ---- | ---- |
| 40000 | 200 | 256 | 0.1 | 0.9 | True

| Weight Decay Rate | # of Layers | Widen factor | Drop rate | Augment Method |
| ---- | ---- | ---- | ---- | ---- |
| 5e-4 | 28 | 10 | 0 | Random Crop & Flip
