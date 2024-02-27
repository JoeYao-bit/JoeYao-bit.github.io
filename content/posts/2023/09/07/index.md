---
title: "Distinctive topology path planning"
description: "This is a versatile tangent graph-based topologically distinctive path planning algorithm for grid maps. This method significantly enhances the efficiency of search topology distinctive paths, thereby optimizing the overall process of trajectory optimization or motion planning."
date: 2023-09-07T06:52:49+08:00
draft: false
---

We proposed a tangent graph-based topologically distinctive path planning. It leverages the property that tangents form locally shortest paths, ensuring that any two locally shortest paths belong to different topologies.

Compared to existing algorithms, our approach requires no indicator to determine whether two paths belong to the same topology. Furthermore, it eliminates the need to repeat the search for multiple paths, as all distinctive paths can be found in a single search. 

And to address the challenge of the exponential growth in queue size during breadth-first search, we propose a priority limitation technique. This approach significantly reduces the time cost of searching for multiple paths while preserving computational complexity.

Comparison of total time cost to get multiple paths
![alt 属性文本](images/RJ_mean_map.png  "")

Our method's mean time cost to get each path as number of paths increases

![alt 属性文本](images/RJ_mean.png "100 paths, in 8.2ms")

Source code: https://github.com/JoeYao-bit/TangentTopologyPathPlanning

Map source: https://movingai.com/benchmarks/grids.html