---
title: "2点間を結ぶ直線の角度の求め方"
date: 2018-03-11T23:30:48+09:00
draft: false
categories : ['tech']
tags : ["math", "python"]
---
# 座標Aと座標Bを結ぶ直線の角度
![radian](/img/calculate_radian.png)

## mathを使ったバージョン
```
>>> import math
>>> x1, y1 = 0, 0
>>> x2, y2 = 5, 5
>>> radian = math.atan2(y2 - y1, x2 - x1)
>>> radian
0.7853981633974483
>>> math.degrees(radian)
45.0
```
