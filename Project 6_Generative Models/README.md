# Generative Models

### Goal
Use generative models (GANs, VAEs, Normalizing flows) to generate more data or better understand the data at hand. Mathematical understanding.

### Language
```Python```

### Contents
1. Generative Adversarial Networks (GANs)
2. Variational AutoEncoders (VAEs)
3. Normalizing flows

### Librairies
* ```Pytorch```
* ```scikit-learn```
* ```numpy```
* ```matplotlib```

### Conclusion
In this lab, we have implemented and compared the performances of three models: GANs, VAEs and Normalizing flows. Here is the conclusion we can have following our analysis:

* GANs: GANs have several advantages: they can be used of very various applications, and are capable of generating high-quality, realistic images. However, they are very difficult to train, and it can take a lot of time. A big other problem of GANs is that they can be unstable and prone to mode collapse, where the generator produces a limited set of samples that do not represent the full data distribution.
* VAEs: VAEs are very powerful tooks, because they can work with a lot of different data, whether they are labeled or not. A big drawback of VAEs is the fact that they can generate samples that are blurry or less sharp than GANs. This is caused by the way data distributions are recovered, and loss functions are calculated.
* Normalizing flows: it is a very interesting model, which provide a robust distribution approximation. The main problem of normalizing flows method is that it is very computationally expensive, with models taking several times as long as GANs to generate images of the same resolution. These methods are moreover limited by density estimation performance issues compared to state-of-the-art autoregressive models, and they may suffer from the "bottleneck" problem, where the transformation function is forced to compress the information into a lower-dimensional space.
