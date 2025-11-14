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



### 6.2 (b)



## 7. Question 5 – Support Vector Machines



### 7.1 (a)



### 7.2 (b)



### 7.3 (c)



### 7.4 (d)



### 7.5 (e)



## 8. Question 6 – Neural Networks and Naive Bayes



### 8.1 (a)



### 8.2 (b)



### 8.3 (c)



## 9. Conclusion



## 10. References
