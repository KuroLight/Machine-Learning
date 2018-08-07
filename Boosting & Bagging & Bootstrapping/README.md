# What is the difference between Boosting, Bagging and Bootstrapping

都是B开头，这几个术语和集成学习（Ensemble）有关。

## Ensemble 集成学习

集成学习：实用多个（几百几千）个同样算法的模型做综合决策，最终得到“正确”的分类。Boosting和Bagging等技术，可以提升统计模型的鲁棒性（Robustness），从而降低方差（Variance）。

## Bootstrapping

Bootstrap，核心是可放回的随机采样（重采样），它允许模型和算法更好的理解数据的偏差（Bias）、方差（Variance）和特征（Features）。每个样本群有不同的偏向，综合不同的样本群特征，可以得到更加鲁棒的模型。

使用Bootstrapping也可以测试解决方案的稳定性，它可以识别出过拟合且未使用不同方差数据集进行测试的模型。

另外，计算力的提升，让更加多次数的重排列、重采样变得可能。

## Bagging

Bagging，实际上是指Bootstrap Aggregator。关键在**随机采样**，各个**弱学习器**之间没有依赖关系，可以并行拟合。

Bagging的作用，是降低只在训练数据上准确率较高的模型的方差——也就是过拟合。

Bagging的过程：
我们有n个样本的训练集，每次**有放回**随机采样m个样本，用于同时训练**弱学习器**（相同的单一模型），然后对进行投票。

### Decision Tree 决策树

决策树是容易过拟合的一种算法，所以我们有随机森林（Random Forest）算法。随机森林是Bagging算法的一个特例。

1. RF使用CART决策树作为弱学习器
+ 根据随机样本特征中选择最优的特征作为决策树的左右树，而不是所有样本特种的最优特征，所以提升了模型的繁华（Generalization）能力
+ 最后进行投票

## Boosting

Boosting，是使用加权平均值使**弱**的学习器变强的一种算法。Boosting特点是各个**弱学习器**之间有依赖关系，每个模型会决定下一个模型要关注的特征。

## Conclusion 总结

Boosting和Bagging都能够有效降低方差-集成方法通常优于单个模型。（Kaggle制胜法宝-ensemble）
Boosting解决过拟合问题上更优，但是可能导致性能问题。

## Translation 中英对照

* 集成学习 ensemble
* 鲁棒性 robustness
* 方差 variance
* 随机森林 random forest

## Reference 引用
* [Bagging与随机森林算法原理小结](https://www.cnblogs.com/pinard/p/6156009.html)
* [如何构建稳固的机器学习算法：Boosting&Bagging](https://www.jiqizhixin.com/articles/2017-11-25-2)