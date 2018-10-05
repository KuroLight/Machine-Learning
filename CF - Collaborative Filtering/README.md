# 协同过滤

## Memory-based CF

example:
given user-movie matrix of rating scores, 

for a query pair (userA, movieA),
find knn users (using dot product/ cosine similarity) vectors of userA, compute the score using mean or weighted(dot products or cosine as weights) sum

## Item-based CF

example:
given user-movie matrix of rating scores, X
compute the association matrix A = X.T@X

for a query pair (userA, movieA),
find knn movies  (using dot product/ cosine similarity) vectors of movieA, find the ones that userA has rated using matrix X, and compute the score using mean or weighted(dot products or cosine as weights) sum

## bias reduction