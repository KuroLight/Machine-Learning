# LR versus Linear SVM

## SAME

1. supervised learning classifier
2. Linear classifier
3. Deterministic model

## DIFFERENCES

### Loss function

1. LR: min cross entropy
2. SVM: max margin

### Data

1. LR: based on probability, need to balance data
2. SVM: no need to balance data

### Probability

1. LR: based on probability, output is a probability
2. SVM: no probability

### Feature Scaling

1. LR: based on probability, basically no need to do feature scaling, but if we want to add regularizor, we need normalization
2. SVM: based on distance, need normalization

### Regularization

1. LR: add regularizor to generalize better (经验风险最小化)
2. SVM: itself is optimize weights minimization, (自带结构风险最小化)

### Kernel

1. LR: too high complexity
2. SVM: kernel trick, low complexity

### In Practice

1. LR: good for large scale data, good for online learning
2. SVM: good for small data

## Reference

1. [【机器学习】Linear SVM 和 LR 的联系和区别](https://blog.csdn.net/haolexiao/article/details/70191667)