####  量化部分1
##### 股票池+择时的策略
实例：股票池设计思路
 市值因子
 估值因子（PE/TTM）
 超跌因子  A股超跌因子可能更有效
 ST股票的策略
  （适当地使用剔除法）
 再平衡周期
 容量
 择时信号设计（如20min K线，MA3上穿MA200） 注意如何在聚宽实现20min K线

源代码讲解

一些注意事项：对于趋势性策略，退出时间远远比进入时间重要

因子的特殊处理：PE-EP    PB-BP

多因子模型：如何给不同因子打分
  财务因子的处理
  小周期大均线

##### 均值回复策略
简单应用：短期市场反转逻辑——选择过去3月跌的最多的N支股票构建股票池
优化：尺度量价、缺口方式、套利模式

海龟交易代码讲解（基于TB）

策略评估：
风险：收益率的标准差
两个重要比率： 
  夏普比率
  最大回撤
超额收益检验：

#### 金融大数据部分
SQL基础