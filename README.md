# hands-on-deep-learning-using-tensorflow-2.0

重读 CNN 网络的经典论文，并用 tensorflow 2.0 手撸一遍经典模型，感受一下实测数据

硬件环境: GTX 1080(GPU) + i7 7700k(CPU) + 16G Memory


## 1. 从 AlexNet 到 ResNet -- 越来越深的 CNN 模型


注：LeNet5 过于简单，复现优先级低。


#### 1.1 AlexNet  -- CNN 网络奠基工作的代表

code and result: [AlexNet on MNIST and Cifar10 Datasets](code/01-AlexNet-on-MNIST-and-Cifar10-dataset.ipynb)

观点：AlexNet 在 cifar10 上展示了 CNN 网络的潜力。70% 的正确率，在容错率较高的场景下，具备一定的使用价值。


#### 1.2 Vgg -- 暴力加深的收官之作

code and result: [VggNet on Cifar10 Datasets](code/02-VggNet.ipynb)

观点：

1. VggNet 成功的把网络做的更深了，模型的算法性能也有了不错的提升(70% - 78%)
2. 运行时间增加 10 倍，也很明显。计算的能效比已经不那么高了。


#### 1.3 ResNet -- 弹性加深

code and result: [ResNet on Cifar10 Datasets](code/03-ResNet.ipynb)

观点：

1. ResNet 的性能和能效比，都好于 VggNet。碾压式的进步。
2. 当前实现版本，过拟合很严重，是改进的重点。


## 环境搭建

见 [Ubuntu 18.04 搭建 cuda10.1+tensorflow2.1+python3.7](https://zhuanlan.zhihu.com/p/45041445)

```bash
$ pip install -r requirements.txt
```

## 背景知识学习路径

1. Tensorflow 2.0 Tutorials: [https://www.tensorflow.org/tutorials](https://www.tensorflow.org/tutorials)
2. Keras Introduction: [https://keras.io/](https://keras.io/)
3. Getting started with the Keras Sequential model: [https://keras.io/getting-started/sequential-model-guide/](https://keras.io/getting-started/sequential-model-guide/)
4. Getting started with the Keras functional API: [https://keras.io/getting-started/functional-api-guide/](https://keras.io/getting-started/functional-api-guide/)
