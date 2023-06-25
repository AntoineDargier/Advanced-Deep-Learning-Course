# Transfer Learning

### Goal
Use of Transfer Learning and Data Augmentation to improve challenging context, in which few data and resources are available.

### Laguage
```Python```

### Contents
1. Training set creation
2. Testing procedure
3. Baseline model (implementation from scratch)
4. Transfer Learning with ResNet models (pretrained ResNet34 model)
5. Data augmentation

### Libraries
* ```Pytorch```
* ```torchvision```
* ```matplotlib```
* ```numpy```

### Conclusion
When we implement ResNet18 from scratch with our small train set, we can see that the model is clearly overfitting: we have 100% accuracy on the train set, but only 21.48% on the test set. So we need to find solutions to this issues. A first one can be transfer learning from a pretrained model ; a second one can be to try data augmentation to have a bigger train set.
After this first analysis, we try to use a pretrained model. We choose ResNet34 model, which we adapt to our task with transfer learning: we create new layers that we train alone in a first part, before learning the whole model to our task. With this method, we achieve to reach 100% accuracy on the train set, and 27.27% on the test set. We can see now that transfer learning is a good solution when train set is very small, because there is always overfitting but the results are better on the test set.
Finally, we tried data augmentation to improve the size of our training set. We implement transformations on our data, such as andomHorizontalFlip, RandomCrop, GaussianBlur, ColorJitter. This method seems here pretty efficient, because we succeed to achieve very good performance, with 95% accuracy on our train set, and 24.68% on the test set in 40 epochs. So the performance on the train set is a little bit lower, but the generalization on the test set is better.

| Model | Number of  epochs | Train accuracy | Test accuracy |
|:------:|:------:|:------:|:------:|
|   ResNet18 from scratch  | 20 | 100% | 21.48% |
|   ResNet34 with Transfer Learning | 60 | 100% | 27.27% |
|   ResNet18 with Data Augmentation  | 40 | 95% | 24.68% |
