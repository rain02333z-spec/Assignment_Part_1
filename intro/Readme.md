# Data Mining – Assignment Part 1  
**Report**

Group members:  
- Name 1 (Matrikelnummer)  
- Name 2 (Matrikelnummer)  
- Name 3 (Matrikelnummer)  

Date: 03.12.2025


## 1. Introduction



## 2. Data Description



## 3. Question 1 – Data Exploration

### 3.1 (a)



### 3.2 (b)
describe() 只会显示数值列，对其他非数字列不会进行描述


### 3.3 (c)



### 3.4 (d)
IDS-2-DATA  PPT 108页  Over-sampling  Under-sampling
针对肥胖分类数据悬殊，我们应该采用 欠采样多数数据或者过采样少数数据，来达到平衡不同类的数据量。防止LLM出现精确度高但是召回率低的问题。
采样前应该先把NA 去掉，防止他被识别为一个类。



### 3.5 (e)



### 3.6 (f)
bins=20 bins更大会产生空箱，太小会丢失信息。
这个是Equal-width binning  等宽分箱


### 3.7 (g)
可以，从直方图可以看出整体呈现右偏长尾，且高charges人群基本都是obese 肥胖人群。BMI和charges呈现一定的正相关关系，但不绝对。


### 3.8 (h)
无论是BMI，children还是age ，三组点云呈上下分层，说明吸烟者总体的charge显著高于非吸烟者。同时随着年龄增大，charge呈上升趋势，说明了age与charge的正相关性。


### 3.9 (i)
Weaker positive correlation
弱正相关 两个变量总体上同向变化但是关系不强


### 3.10 (j)
 1.无法回答。从boxplot中只能看出吸烟者总体charge更高，但是boxplot不展示精确的人数，我们只能看出两种人群的占比差异，而无法比较数量上的区别。
 2.不存在，没从图中看到下侧离群值。
 3.否，中位数应该是小于均值。因为可以看到数据分布右偏，说明charge大的占比更多，均值应该比中位数要大。
 4.是的。

## 4. Question 2 – Decision Trees

### 4.1 (a)



### 4.2 (b)
wishful-thinking model 准确率更高，因为在测试集中low的占比更高，使用众数模型只能代表训练集的特征，但是这一点在测试集中并没有体现所以最后结果还不如单纯的wishful-thinking model。


### 4.3 (c)
max_depth为1  精确度最高  且最简单


### 4.4 (d)
根据图像可知年龄高于44.5且不吸烟的个体户会被预测为medium
对于“42 岁、男性、BMI=36、2 个孩子、不吸烟、居住在西北（northwest）”的个体 预测为low


## 5. Question 3 – Clustering (K-means)



### 5.1 (a)



### 5.2 (b)



### 5.3 (c)



### 5.4 (d)



### 5.5 (e)



## 6. Question 4 – Regression



### 6.1 (a)
不适合，charges没有均匀的分布在回归线两侧，大多数点偏离回归线过大。


### 6.2 (b)



## 7. Question 5 – Support Vector Machines



### 7.1 (a)

只采用BMI，smoker_yes,age 三个特征和全特征的混淆矩阵一样，说明其他feature都没用或影响极小。通过查看ceof也可以发现这一点。其中最重要的是smoker_yes。

### 7.2 (b)

accuracy和precision 都是一样的 因为混淆矩阵一样，具体原因同上。 和我的预期相同

### 7.3 (c)
标准化之后的准确率和召回率都更高一点，但在3特征情况下结果一样，这种优势只体现在全特征都参与计算的情况。


### 7.4 (d)
c越大准确率越高，C控制了训练对错误答案的惩罚，C越小对错误的分类越包容。所以C大的时候会更加拟合，准确率也会更大。


### 7.5 (e)
因为不同特征间数值范围区别很大，如果不做归一化部分特征数值极大会主导距离的计算，所以归一化某种程度上避免了这种问题，让每一个特征的“权重”一样了。这样就更加的公平，准确率就更高了。


## 8. Question 6 – Neural Networks and Naive Bayes



### 8.1 (a)



### 8.2 (b)

数据标准化+隐藏层神经元搜索。   从1到50改变隐藏层神经元数 寻找最好的参数。 
Best hidden size: 18
Best test accuracy: 0.996268656716418

Confusion matrix (best MLP, scaled, 1 hidden layer):
[[ 33   0   0]
 [  0 131   0]
 [  0   1 103]]
准确率大大提高

### 8.3 (c)

标准化缩放过后 使用朴素贝叶斯分类器反而精确率降低了。因为朴素贝叶斯本身对数据尺度就不敏感，而MLP则非常吃尺度。
标准化并不带来明显收益，甚至略有下降
