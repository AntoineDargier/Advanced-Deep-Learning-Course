# Project 1: Hyper-parameters and training basics with Pytorch

### Goal
Test of different architectures (impact of the learning rate, optimizer, loss function) of Deep Learning models on three problems: classification, multilabel classification and regression.

### Contents
1. Data exploration
2. Design the neural network
3. Train the model
4. Hyper-parameters search
5. Evaluate the model

### Language
```Python```

### Libraries
* ```Pytorch```
* ```matplotlib```

### Conclusion
I achieve very good results with these methods, but see that it can be very difficult to find the best parameters for our model to perform well. In fact, the architecture of the model (layers, activation functions), the batch size, the loss function, the learning rate, optimizer, ... can have a big influence on both the accuracy of the model and the training time. In the majority of cases, trying to increase accuracy has a negative impact on the training time and vice versa. We have finally also seen that the fine-tuning of all hyperparameters
is very time-consuming, taking sometimes dozens of minutes for one single value so the trade-off between accuracy and training time should sometimes be re-evaluated considering this.
