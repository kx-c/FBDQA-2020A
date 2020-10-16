### 金融基础知识
#### 金融基础概念
- 金融学
  - 狭义：资金融通
  - 广义：研究**跨期**配置**稀缺资源**的一门学科
  - 其他角度：经济学的一个分支
- 金融学的分类
  - 公司金融（融资端）
  - 资产定价（投资端）【focus】
- 金融学假设与概念
  - 基本假设：理性人假说【趋利避害】
  - 边界条件：资源的稀缺性&制度费用
  - 重要概念
    - 选择：trade-off
    - 偏好：风险
    - 效用：满足感和幸福感（效用函数单调递增）
    - 信息：信息不对称，期望通过技术手段获得更多信息
  - 基本原理
    - 收益和风险的trade-off
    - 边际效用递减
  - 四大理论支柱
    - 有效市场假说
    - 均值方差组合
    - CAPM模型
    - 期权定价公式
#### 金融市场与制度
- 金融市场
- 金融资产
  - 资产：有明确产权的任何物品
  - 资产价格：未来现金流的折现值之和
  - 流动性：变现的难易程度
- 交易制度
  - T+1
  - 卖空限制：不允许做空
  - 竞价方式：集合竞价、连续竞价
#### 资产定价与投资学
- 折现现金流模型
$$
P=\sum_{t=1}^{n} \frac{E\left(C F_{t}\right)}{(1+r)^{t}}
$$
#### CAPM模型实证检验
### 聚宽平台简介
- 聚宽SDK
- 聚宽在线平台
### 量化交易策略开发案例
*关注海龟交易法则 尤其加仓部分*
#### 为什么要动手实践
- 程序化自动交易策略需要实现
- 漏洞&细节需要检验
#### 如何选择适合的实践平台
- 聚宽
  - 从股票入门
  - 免安装云平台
  - 主流编程语言
  - 易学习
  - 可接模拟盘和实盘
- 聚宽编程框架
  - 启动：Initialize() 设置交易成本、滑点等 开启实时监测run_daily()
  - 开盘前：run_daily(pl_before_market_open, time='before_open') 准备策略需要的数据
  - 盘中：run_daily(pl_trade, time='every_bar') 根据设定的时间间隔自动调用 处理交易逻辑
  - 收盘后：run_daily(pl_after_market_close,time='after_close')
- 聚宽参数设置
  - 回测时间段
  - 初始资金：改成1000w
  - K线时间级别
- 交易系统的要素
  - 头寸分配为重中之重
#### 如何选择交易标的-股票池
- 从优质股票的集合中，选择近期开始发力上涨的股票
- **股票池+择时=策略基础**
- 选股条件+再平衡（调整成分股的频率）+容量
#### 如何选择交易时机-择时信号
- 技术指标
  - 均线型
  - 趋势型
  - 摆动型
  - 能量型
- 均线交叉
  - 金叉：主要指股票行情指标的短期线向上穿越长期线的交叉
  - 死叉：主要指股票行情指标的短期线向下穿越长期线的交叉