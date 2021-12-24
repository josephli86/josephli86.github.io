---
title: Backtrader-Analyzers
date: 2021-12-24 13:45:05
tags:
- backtrader
- 量化投资
- python
---

# Analyzers 

Analyzer提供了记录、分析投资策略的容器。

## 基本调用方法

```python
cerebro = bt.Cerebro()

# 添加Analyzer容器
cerebro.addanalyzer(bt.analyzers.ExistingAnalyzerClasses, _name = "UserDefinedName")

# 其他步骤

# 执行策略
theResult = cerebro.run()

# 提取Analyzer数据
theResult[0].UserDefinedName.get_analysis()

```

## Analyzer自带的类树
backtrader.Analyzer()是Analyzer基础类。所有其他Analyzers都是Analyzer的子类。已存的类结构树如下所示：

|----Analyzer()
       |----Transactions()
       |----TradeAnalyzer()
       |----TimeReturn()
       |----SQN()
       |----SharpeRatio()
       |----Returns()
       |----PyFolio()
       |----PositionsValue()
       |----PeriodStats()
       |----LogReturnsRolling()
       |----DrawDown()

### PyFolio



