# Flow of the Covid Project from the start

## Datasets
1. Files60 - Data from 60 athletes that is giving good results so far.
2. Files158 - All data files

## DImensionality reduction
1) PCA 
   <ol type = 'a'>
   <li> On raw data
   <li> Area under the curve
</ol>

## Ion counts or charge intensity?
Ion counts is better as charge intensity is suppressing smaller peaks and showing as a smooth line.


## Area under curve? (point wise or integer wise?)
Integer wise area under curve calculation is more correct mathematically. It will also prevent any errors while calculating areas in irregularly spaced intervals.


## Main paths
1) Create a workflow for preprocessing the signals. [`Preprocessing`](preprocessing.md)
2) Automatic features selection using ML. [`findingFeatures`](findingFeatures.md) 
3) Try to increase the prediction accuracy of the machine learning models. [`methods`](methods.md)