# 书法字骨架提取
提取骨架图像的算法采用本文提出的基于 Z-S 算法改进的单像素化处理算法。
利用欧式距离对图像中书法字骨架进行相似度的计算，利用所求得的相似度值来评价作品在整体结构方面与原始字帖图像的相似度。
用这种方式可以大致的得到两张图片的基本相似度，其骨架可以体现书法字的主体结构，书法字骨架图像的相似度即可视为是两者在整体结构上的相似度。

#笔画提取
#加载参考模块图像。计算参考模块的Hu矩。定义九宫格的位置和权重。
遍历九宫格的位置，对每个位置：
a. 提取当前位置的模块图像。b. 计算当前模块的Hu矩。
计算每个模块Hu矩与参考模块Hu矩之间的皮尔逊相关系数。根据权重计算加权和。

