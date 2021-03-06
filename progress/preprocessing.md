## Preprocessing methods tested for algorithms
1. Baseline correction
2. Standard scaling or scaling with callibrant data
2. apomyoglobin callibrant files for normalizing data


### Baseline correction
1. Baseline correction works only on some ranges, if it is applied on the whole signal it is altering the smaller peaks. For example, for the Pos1.txt spectrum, when an n-degree polynomial is fitted on the spectrum, it is shifting a part of the spectrum to negative axis (minimum = ~ -15000). When the absolute value of negative integer is added, then it is moving the smaller peaks upwards. A differet route is to be taken here.

2. [update] 
    - Upon trying polynomial of degree 3 and degree 5, degree3 seemed to look better visually. ( plot links [`degree_5_image1`](AllResults/Images/problem_with_baseline_correction/Neg 8_degree5.jpg) [`degree_5_image2`](AllResults/Images/problem_with_baseline_correction/Pos 22_degree5.jpg) plot links [`degree_3_image1`](AllResults/Images/Problem_with_baseline_correction/Neg 8_degree3.jpg) [`degree_3_image2`](AllResults/Images/problem_with_baseline_correction/Pos 22_degree3.jpg))
    -  The above images will have three lines 
        -  unProcessed : raw data without any processing. 
        -  Processed, not corrected : Baseline correction is applied. (notice that this goes below zero)
        - Processed, corrected : The absolute value of the minimum is added to the entire spectrum. (This effects the spectrum greatly at higher ranges where the peaks are small)
    - Instead of adding the the absolute value, if the the negative values are flipped to zero then we have these plots ( plot links [`degree_3_zero_image1`](AllResults/Images/problem_with_baseline_correction/Neg 8_make_negative_zero.jpg) [`degree_3_zero_image2`](AllResults/Images/problem_with_baseline_correction/Pos 22_make_negative_zero.jpg) )
        - The plot adjusted with zero value has two lines, normal and the corrected line (any value going below zero is made zero).
        - From these plots, we can see that a major portion of the peaks are getting clipped. 
    - [`reference_paper`](../summaries/2.6.md) : This study uses urine sample, so it could be different from this data. They have 5-degree polynomial which clearly did not work for us. Secondly they only seem to correct the baseline below ~12,000 (as shown in the Figure 2). Can we do the same, if so is there any certain value or can it be anything? 



### Standard scaling data
1. No effect on pca, auc, and hand-crafted features.
   
### Scaling with callibrant
1. All files are associated with a certain callibrant file. The highest peak occuring at 10336 has to be used to normalize the data. 
2. No change in accuracy seen with this normalization.





[`findingFeatures`](findingFeatures.md)

[`methods`](methods.md)

[`main`](progress.md)