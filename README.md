# Note of CS231n
@Author AnhangZhang
=================

## Class1
------------------
神经网络算法：训练函数+测试函数

KNN：K最近邻算法，选定K值进行分类。
如：Manhattan distance曼哈顿距离（依赖坐标轴，量化元素多适用，如：工作年限与薪资），Euclidean distance欧几里得距离（未知元素多适用）。  

超参数：在开始学习过程之前设置值的参数，量化准确率取最佳。如：K/distance metric
如何设置超参数：
1）训练集（train）+验证集（validation）+测试集（test）。用训练集（部分已知的）训练多组K，然后在验证集（剩余部分已知的）验证，取best放在test（未见过的数据）上跑。
2）交叉验证：训练数据分成若干份，每一部分都为验证集。训练大部分，验证一份，然后test，直到所有份数验证完毕，每组超参数如此，可以选出最优的超参数。
PS：要打乱测试集。  

KNN总结：不适用于图像。
1）运算时间长。
2）向量化的距离函数不适用图像。
3）维度灾难。KNN需要密集的点分布在图片上，导致训练数据的量指数倍增加。 
（一维度4points，二维度16points，三维度4^3points）


## Class2
-------------------
线性分类：f(x,W), x from Image, W为参数/权重，会得出若干组分数描述若干类别，越靠近Image分数越高。
缺点：过于简单不灵活
