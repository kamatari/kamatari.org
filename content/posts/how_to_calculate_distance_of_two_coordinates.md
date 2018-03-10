---
title: "2点の座標間の距離の求め方"
date: 2018-03-10T21:38:10+09:00
categories : ['tech']
tags : ["math", "python", "numpy"]
draft: false
---
# 座標(x1, x1)と座標(x2, y2)の間の距離
## math library を使ったバージョン
```
>>> import math
>>> x1, y1 = 1, 1
>>> x2, y2 = 10, 10
>>> math.sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2))
12.727922061357855
```

## numpyを使ったバージョン
```
>>> import numpy as np
>>> x1, y1 = 1, 1
>>> x2, y2 = 10, 10
>>> a = np.array([x1, y1])
>>> b = np.array([x2, y2])
>>> np.linalg.norm(a - b)
12.727922061357855
```
