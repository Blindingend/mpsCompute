# MPS 的计算方法


## 计算生产关系

先计算各个物品之间的关系，注意**只考虑上一级**而不考虑上上级
因为是下一级的生产需要考虑上一级的需求

C = 2A
D = 2A + 3B + C
E = 3A + 2B + C + 2D
F = 4D

## 正式计算

### 计算毛需求量

1. 需求与其他物品无关
那么直接按照表中给的填
2. 需求与其他物品有关
毛需求量 = 表中给的 + 当月被需求物品**订单投入量**所需要的
_一定记住是订单投入量，因为是生产需要_

### 计算正式投产之前的库存
就填现有库存和入库量，一直填到有毛需求量为止

### 计算净需求量
(净需求量是你库存不够毛需求里你得提前生产的量）
净需求量 = 毛需求量 + 最低安全库存 - 上月计划库存量
（低于0按0算）

### 计算计划订单投入量
生产周期为 T
1. 如果没有批量要求
T 月前计划订单投入量 = 当月净需求量
2. 如果有批量要求
当月净需求量/批量 = P
    1. P = 0 （0 就别算了  (;￢＿￢)   ）
    2. P ≠ 0
    T 月前计划订单投入量 = (int(P)+1) * 批量

### 计算计划订单产出量
根据周期和投入量填就好

### 计算投产之后的库存量
_其实是一个公式不过分开算吧_
当月计划库存量 = 当月计划订单产出量 + 上月计划库存量 - 当月毛需求量
