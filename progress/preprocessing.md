## Preprocessing methods tested for algorithms
1. Baseline correction
2. Standard scaling or scaling with callibrant data
2. apomyoglobin callibrant files for normalizing data


### Baseline correction
1. Baseline correction works only on some ranges, if it is applied on the whole signal it is altering the smaller peaks. For example, for the Pos1.txt spectrum, when an n-degree polynomial is fitted on the spectrum, it is shifting a part of the spectrum to negative axis (minimum = ~ -15000). When the absolute value of negative integer is added, then it is moving the smaller peaks upwards. A differet route is to be taken here.

### Standard scaling data
1. No effect on pca, auc, and hand-crafted features.
   
### Scaling with callibrant
1. All files are associated with a certain callibrant file. The highest peak occuring at 10336 has to be used to normalize the data. 
2. No change in accuracy seen with this normalization.





[`findingFeatures`](findingFeatures.md)

[`methods`](methods.md)

[`main`](progress.md)