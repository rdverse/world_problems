# Methodology


## Methods implemented using area under curve data


### What algorithms have been tested so far
1. Logistic Regression
2. KNearest Neighbors
3. Random Forest
4. Decision Trees
5. SVM
6. ANN
7. RNN

| Algorithm | Acuracy | Feature used|
|:-----------: | :--------: | :--------: |
 Random Forest | 92.3% | AUC | 
| xgboost | 94.5% | AUC |
| ANN/RNN | 85.71% | AUC | 
| SVM | 76.4% | AUC |
| Logistic Regression | 91.7%  | AUC |
| KNN | 92.2% | AUC |
| DT | 85.5%| AUC |


### Dimensionality Reduction
1. Used PCA to generate 2, 10, 20, 30, 40, 50,..100 components and fit a random forest model. 
2. PCA on the raw data in the important ranges - 
3. 


## Methods implemented using hand-crafted featues
1. (Mean, median, mode, kurtosis, skewness, etc.,) ()
2. With scaling


[`findingFeatures`](findingFeatures.md)

[`Preprocessing`](preprocessing.md)

[`main`](progress.md)