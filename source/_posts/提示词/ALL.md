---
title: ALL
date: 2023-07-15 09:21:52
categories: [prompt]
tags: [prompt]
---

> "您好，可以帮我按照以下规则解析一个JSON串吗。辛苦啦！"
> 
> "我会给你一个JSON对象格式的字符串，其中key是股票的名称，value是对象数组，称为该股票的K线序列，我会把某只股票的K线序列简称为序列，对象里面几个键的含义是这样的，open代表开盘价，close代表收盘价，high代表最高价，low代表最低价，volume代表成交量，date代表这根K线的时间；我会将最低价简称为低点，将最高价简称为高点；我会将最高价和最低价之间的范围称为该K线的范围，将开盘价和收盘价的范围称为该K线的实体，将最高价到实体上方的范围称为上影线，将最低价到实体下方的范围称为下影线"
>
> "以下属于基础形态"
> "如果序列中存在相邻K线的每一根K线都出现低点抬升或者高点抬升的子序列，那么这个子序列属于连续上升趋势；反之属于连续下降趋势；"
> "如果序列中存在相邻K线的每一根K线都出现低点抬升并且高点抬升的子序列，那么这个子序列属于强连续上升趋势；反之属于强连续下降趋势；"
> "如果序列中存在总体上的低点抬升或者高点抬升的子序列，不需要同时抬升，那么该子序列属于上升通道；反之属于下降通道；如果低点和高点都来回波动，则属于交易区间"
> "任意一波高点总体上的上升随后出现一波低点总体上的下降的现象称为牛旗波段，任意一波低点总体上的下降随后出现一波高点总体上的上升的现象称为熊旗波段。牛旗波段和熊旗波段统称为波段，牛旗波段的最高点称为波动高点，熊旗波段的最低点称为波动低点。上一个波动高点称为前波动高点，上一个波动低点称为前波动低点"
> "在子序列寻找两个波动低点连接起来能让子序列内的大多数的K线在这条线之上，那么这条线就称为该子序列的上升趋势线"
> "在子序列中寻找两个波动高点连接起来能让子序列内的大多数的K线在这条线之下，那么这条线就称为该子序列的上升通道线"
> "如果将上升趋势线平行移动到子序列内的一个波动高点，使得子序列内的大多数的K线在这条线之下，那么这条线就称为上升平行通道线"
> "如果将上升通道线平行移动到子序列内的一个波动低点，使得子序列内的大多数的K线在这条线之上，那么这条线就称为上升平行趋势线"
>
> 
> "您回答的时候请加上所属股票的名称和子序列的时间范围，并且不考虑后面的K线是否打断了这个趋势，只关心子序列本身的趋势"
>

==========

> 
> 
> 
> 
> 
> 如果其间有低点下降，请告诉我低点下降的小范围中时间范围内出现了回调；如果回调幅度没有超过前期上升幅度的一半，则是简单回调，否则是复杂回调"
>
> "如果某只股票的K线序列中存在一个范围的最低价和最高价总体上是递减，你应该回答我这只股票（用真实名称代替）在K线序列的时间范围内（请把时间戳转为可读的时间）是下降趋势；如果其间有高点上升，请告诉我高点上升的小范围中时间范围内出现了回调；如果回调幅度没有超过前期下降幅度的一半，则是简单回调，否则是复杂回调"
>
> "如果某只股票的K线序列的最低价和最高价分别在一个区间内来回波动，你应该回答我这是一个交易区间"
>
> "如果某只股票的K线序列在第?根K线到第?根K线之间，这些K线的范围高度重叠，你应该回答我在K?到K?之间形成了多K线交易区间，如果其中大部分K线的上影线和下影线相对于K线的实体都很长，那么你应该补充回答我这是一个铁丝网形态"
>
>
>
>
>
>
>
>
>
>
>
>
>








