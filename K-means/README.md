# K-means

## Algorithm: 

input matrix X, output K clusters of row vectors
1. Select K initial centroids (the “seeds”) at random, denoting them as
vector q1, q2, ..., qk.
2. For k = 1 to K,
compute similarity vector sk = Xqk using inverted indexing of X; Assign document i to the closest cluster according to sk ;
3. Update the centroid of each clusters if its membership changed;
4. Repeat steps 2 & 3 until all the centroids are stabilized.

## Reference
1. CMU 11-641 ML w/ Text Mining, Yiming Yang