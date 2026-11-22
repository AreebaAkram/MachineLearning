## variance & covariance:
spread of data around its mean & covariance measures how two variables change together

High variance shows data points are more scattered

PCA looks for directions in which the data has the greatest variance.
high variance means more scatterness, more scatterness means high influence in predictions

first standardize, then any computation

as the new principal compoenents (features sets) are identified, towards the highes variance in data, they are called eigen vectors. diff eigen vectors has diff varaince in their directions, eigen values displays how much information that direction captures.

it takes that covariance matrix and rotates your coordinate system to align with the spread of your data. as eigen vectors are safe towards linear transformations, they can be stretched, shrink or reversed

## process
The first eigenvector points in the single direction where your data points are most spread out (highest variance). - PCA1 (first new feature)

The second eigenvector points in the next most spread-out direction, with the strict rule that it must be completely perpendicular (orthogonal) to the first one.

eigen value directly proprtional to varince in that direction - high information

** PCA is not about dropping columns it's more about how each feature will contribute to predictions, and PCA task is to find the area where the varaince is greatest irrespective of feature importance**