# K Nearest Neighbors (KNN) 

K-Nearest Neighbors (KNN) is a non‑parametric supervised method: for classification, it predicts the class of a point by a majority vote among its k nearest training points; for regression, it averages their values.
There is no “model training” in the parametric sense—KNN simply stores the training set and computes distances at prediction time. 

* In this dataset There are 9 columns and 768 rows.
* Algorithm Used: K Nearest Neighbors
* Libraries: scikit-learn, pandas, matplotlib, seaborn

🎯 Key Features of a Training Dataset for KNN (Short Insights)
1. Lazy, instance-based learning
KNN doesn't “learn” a model upfront; it stores the entire training set and defers any computation until prediction time. Because of this, every training point is a potential neighbor at query time. KNN is thus called a lazy learner

2. Feature scaling is essential
KNN uses distance metrics (like Euclidean), so features must be on the same scale. Otherwise, large-magnitude features (say income) drown out smaller ones (like age). Always apply StandardScaler or MinMaxScaler before training! 

3. Distance metric matters
* Euclidean (L2) — default for continuous data
* Manhattan (L1) — more robust to outliers
* Minkowski — generalizes both
* Select based on your data’s nature. Different metrics emphasize different aspects of “closeness.” 

4. Avoid high-dimensional noise (“Curse of Dimensionality”)
As feature count increases, distances become increasingly similar, and the concept of “nearest neighbor” loses meaning. Use techniques like PCA, feature selection, or drop irrelevant columns. 

5. Beware of irrelevant features & class imbalance
Irrelevant or redundant features still contribute to distance computations unless removed or down-weighted (since KNN treats all features equally) 
In imbalanced datasets, majority-class neighbors can dominate the vote. Consider resampling or class weighting.
