# SVM - Support Vector Machine - 支持向量机

## 概括

支持向量机是增加了距离限制的感知机。它属于有监督学习算法。  
基本来说，SVM是一条直线，可以完全划分**线性可分**的两类数据，同时，这条分界线处在两个分类的中间，距离这两类**最近**的一个或多个数据点一样远。

## what is Support Vector and what is Machine - 为什么叫支持向量机

机（器）是说它是一个分类器。支持向量指的是离分界线最近的**数据点**，一旦这些点不存在了，分界的直线位置可能就要变化。换言之，这些数据点（Vectors）支持（Support）了这个分类器（Machine）

## Maximum Margin - 最大间隔

## Kernel Trick - 核

## Hyperplane

## Scikit-learn Example - sklearn [例子](http://scikit-learn.org/dev/modules/generated/sklearn.svm.SVC.html#sklearn.svm.SVC)

```python3
>>> import numpy as np
>>> X = np.array([[-1, -1], [-2, -1], [1, 1], [2, 1]])
>>> y = np.array([1, 1, 2, 2])
>>> from sklearn.svm import SVC
>>> clf = SVC(gamma='auto')
>>> clf.fit(X, y)
SVC(C=1.0, cache_size=200, class_weight=None, coef0=0.0,
    decision_function_shape='ovr', degree=3, gamma='auto', kernel='rbf',
    max_iter=-1, probability=False, random_state=None, shrinking=True,
    tol=0.001, verbose=False)
>>> print(clf.predict([[-0.8, -1]]))
[1]
```

## More

支持分类的支持向量机可以推广到解决**回归**问题，我们称它**支持向量回归**

## Translation - 中英对照表

```list
Support Vector Machine              支持向量机/器
Classification Machine              分类器
Support Vector                      支持向量
Perceptron                          感知机/器
Perceptron Learning Algorithm/PLA   感知机学习算法
Supervised Learning                 有监督学习
Data Point                          数据点
Regression                          回归
```