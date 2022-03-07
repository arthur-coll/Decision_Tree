# Decision_Tree

*Baseline:*  

Implementation of a Decision Tree CLassifier from scratch in Python.
Our code use the Information gain (Entropy) as the loss function to build the tree.
The tree is constructed based on some stopping criterion: maximum depth of the tree, minimum number of samples per split.
The user can also specify how many features should be used to grow the tree (choosen randomly). This aspect could be used later to build random forst.

*Code Details:*  
Our implementation is based on Object Oriented Programming. 
The user interact with the DecisionTree class using .fit and .train methods.
Internally the code grows the tree recursively by creating Nodes object.

DecisionTree(min_samples_split=2,max_depth=10, n_feats=None)

      min_samples_split: How many minimum samples to keep on growing the tree, 2 by default
      max_depth: maximum depth of the tree, 10 by default
      n_feats: how many features would be used, if we don't use all of them. We could use a random subset of them, such as in random forest.

.fit(X,y)

      X: input
      y: classes 

.predict(y)

      y: List of inputs to predict

**Exemple**  
``clf = DecisionTree(max_depth=10) ``  
``clf.fit(X_train, y_train)    ``  
``y_pred=clf.predict(X_test)  ``   

**Performance /Comparison with sklearn:**

At the end we compare our performance with decision trees implementation of sklearn.
Our implementation is working pretty well but tend to have slightly lower accuracy with small depth trees but to have slightly higher accuracy zith bigger depth.
