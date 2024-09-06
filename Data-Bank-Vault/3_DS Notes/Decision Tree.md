#ml

# Summary

1) What are we trying to predict?

2) What feature (categorical) best gives this classification i,e splits to leaves with TRUE or FALSE.
3) Calculate the total impurity for each branch, choose the one the gives the lowest number (ie best predictor).

![[Pasted image 20240411093348.png]]

A node is pure if it gives a correct classification to its term (i.e no further splitting) We stop when pure.

Output of leaf is the category with the most values.

Decision trees can be [[overfitting]] if the leafs have a small number of values for a dataset, use [[pruning]]. 

Can put limit of tree depth.

Use cross validation to refine the model to better represent the data. (i.e may be more pruned).

---

A decision tree is a {{supervised}} learning algorithm used for both classification and regression tasks. 

Here's how a decision tree works:

**Splitting**: The algorithm starts at the root node (the topmost node) and selects the best feature to split the dataset into subsets. The feature and the split point are chosen based on certain criteria, such as ==Gini impurity== ==or entropy== for classification tasks, and variance reduction for regression tasks. The goal is to make the subsets as homogeneous as possible with respect to the target variable.

**Splitting Criteria**: When building a decision tree, the algorithm considers various features to split the data at each node==. It selects the feature and the split point that minimize the Gini impurity in the resulting child nodes==. The split that reduces impurity the most is chosen.

[[gini impurity]]

==**Recursive Partitioning**==: After the first split, each subset becomes a child node of the root node. The algorithm then recursively applies the splitting process to each child node, creating further splits until certain stopping criteria are met. ==Stopping criteria== may include reaching a maximum tree depth, having nodes with minimum samples, or not improving the purity measure significantly with further splits.

**Leaf Nodes**: Eventually, the splitting process continues until the algorithm reaches leaf nodes, which are nodes with no further splits. ==At each leaf node, the algorithm assigns a class label (for classification)== or predicts a continuous value (for regression) based on t==he majority class== or average value of the samples in that node, respectively.

 **Decision Making**: In practical terms, when deciding which feature to split on, the decision tree algorithm calculates the Gini impurity for each possible split and selects the one that results in the lowest impurity after the split.

**Tree Structure**: The decision tree structure resembles a flowchart, where each internal node represents a decision based on a feature, each branch represents the outcome of that decision, and each leaf node represents a class label or a prediction.

**Predictions**: To make predictions on new data, the algorithm traverses the decision tree from the root node down to a leaf node, following the decision rules based on the input features. Once it reaches a leaf node, it assigns the corresponding class label or prediction.


![[Pasted image 20240404154526.png]]