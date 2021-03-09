

## Which features to use?

| Feature | Accuracy Files60|Accuracy Files158|
|:-----------: | :--------: | :--------: |
 Hand-crafted features | | - | 
| Raw Data |  | - |
| Raw Data with PCA |  | - | 
| Raw Data within important ranges|  |-|
| Area under the curve | 92% |-|
|AUC data when normalized with maximum value| 91.7%| 66.6% |
| AUC with PCA | 90% | |
| AUC ion | 92.3% | |
| AUC charge | 91.4% | |



## Finding the best feature among AUC values
<ul>
<li> Default feature importance
<li> Drop feature importance
<li> Permutation feature importance
<li> Analysis on partial dependence plots
<li> SHAP
<li> LIME
</ul>

1. Default feature importance : sklearn uses mean decrease in impurity (or gini importance). This is usually computed by measuring the amount of uncertaininty  reduced in classification. For this reason, the default feature importances are inconcsistent especially when the algorithm is iterated over 50 times to train and test The creators of Random Forest, [`Breiman and Cutler`](https://www.stat.berkeley.edu/~breiman/RandomForests/cc_home.htm#varimp) posit that adding up the gini scores is more consistent with the permutation feature importance.

2. Drop feature importance : Dropping one feature at a time and training the algorithm is a brute force approach to compute the performace scores for each feature. In this procedure, one column at a time is dropped while the rest of the features are used for training. Then the resultant accuracy is subtracted from the baseline accuracy which gives the performance accuracy. To make the performance accuracy to correlate with the performace score, performance score is given as performance score = 1 - performance accuracy. 

3. Permutation feature importance : First a baseline model is created which is trained on all the available features. Then taking one feature at a time, a random peturbation is applied and the algorithm is retrained. The performace score is computed by subtracting the new score from baseline score.

For 1,2,3 The higher the performace score, the more imoportant the feature is.

4. Partial dependence plots, univariate distributions, multivariate distribution plots provide certain visual cues, that tells us how each feature plays a role in contributing towards model prediction. These plots can be found in [`here`](../utils/feature_importance_plots.md)


5. SHAP : 


6. LIME : 



## Other features to explore
1. Finding features using genetic algorithm
2. Issue 1: What is the criteria for creating segments or separating peaks?




[`Preprocessing`](preprocessing.md)

[`methods`](methods.md)

[`main`](progress.md)
