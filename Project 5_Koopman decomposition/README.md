# Koopman Decomposition

### Goal
Describe the dynamics of a non-linear dynamical system by means of the Koopman theory

### Language
```Python```

### Contents
1. Toy example: Duffing oscillator
2. Discontinuous in time case with the Koopman operator
3. Continuous in time case with the Lie operator

### Libraries
* ```Pytorch```
* ```scipy```
* ```matplotlib```
* ```numpy```
* ```scikit-learn```

### Conclusion
I implemented two different approaches along this assignment, one designed for discrete case and the other in the continuous case.

To improve the training process in both cases (here the improvements were only asked in the discontinuous case), I set up different actions: 
* add a new term of loss, representing the difference between the loss in the latent space and a normal distribution
* freeze the gradients in the encoder part of the VAE
* introduce weights in order to ponderate each of the terms of the loss and try to balance the order of magnitude for each of them.

With these improvements, the overall results of each process are the following :
* in the discontinuous case with the Koopman operator, I found a final loss after 100 epochs of  6.10−5, for a computation time of 290 seconds.
* in the continuous case with the Lie operator, I found a final loss after 100 epochs of  3.10−6, for a computation time of 280 seconds.

Even though the two methods are very similar in terms of computation time, it seems that learning dynamical systems with neural networks gets more efficient in the continuous case with the Lie operator than in the discontinuous case with the Koopman operator. Indeed, after 100 epochs, the final loss of the first one is up to 20 times lower than the loss of the latter. Taking into account that I tried to improve the training process of it with the previously cited actions, it gives no more doubt that the continuous case is far better in our study.
