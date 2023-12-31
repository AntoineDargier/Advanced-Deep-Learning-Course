# Graph Neural Networks (GNNs)

### Goal
 Node (multi-level) classification task: predict, for a given PPI graph, the correct node's labels.

### Language
```Python```

### Contents
1. Load dataset
2. Define a baseline
3. Design a better model

### Libraries
* ```Pytorch```
* ```torch_geometric```
* ```numpy```
* ```matplotlib```
* ```scikit-learn```

### Conclusion
The model having the best performance among those I tried to implement is deeply inspired by the GAT algorithm. It consists in 3 successive GATv2Layer, which are basically an evolution correcting the static attention problem of the initial GATLayer, the attention layer described in the pre-cited article. Then the results (having the size equal to the multiplication of the hidden_size and num_heads parameters) are sent into a LeakyReLU layer and finally to a Linear layer, which is used for the final categorization of each input in the correct number of categories. I conducted a finetuning of the parameters of this model in order to define: the number of successive GATv2Layers and the number of heads to use as our model can work through the multi-head attention process. I found that the best results were found for a number of successive attention layers equal to 3 and a number of heads equal to 2.

I obtained a final F1-Score equal to 0.9784 on the last run (between 0.95 and 0.98 according to the tries). This result is very good, particularly when compared to the Basic Model constructed with GCNLayer whose result is generally not far from 0.6.

The model we built converges also in a really short time compared to the Basic one. Indeed, after 50 epochs, the F1-score is already above 0.9 in the first case, whereas I can not identify any convergence in the second one, which seems not to have converged even after 200 epochs.
