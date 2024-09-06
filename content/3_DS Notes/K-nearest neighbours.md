---
tags:
  - ml
  - "#classifer"
---


It is a [[non-parametric]] method used for classification and regression. A sample is classified by a majority vote of its neighbors, with the sample being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small).

[[K-nearest neighbours]] is a {{[[Supervised]]}} so requires labelled training.
<!--SR:!2024-04-08,4,270-->

[[K-nearest neighbours]] works by;; When a new data point needs classification, KNN looks for its K nearest neighbors in the training data, based on their similarity in features. The algorithm examines the class labels of these neighbors and assigns the most common class to the new data point.
<!--SR:!2024-04-08,4,270-->