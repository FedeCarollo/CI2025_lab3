# Shortest Path
In this lab we were required to implement shortest path algorithms.

## A* implementation
For positive edge weights problems I used an implmentation of A* algorithm, using as heuristic the euclidean distance already used during problem generation.

I compared cost results with `nx`'s implementatio of Dijkstra to ensure that my algorithm found the optimal solution.

## Bellman Ford implementation
For negative edge weights, I implemented and used Bellman-Ford Algorithm and compared to `nx`'s Bellman Ford algorithm to ensure I achieved the same results.

## Sanity check
We were required to compute optimal paths between all pairs of nodes, but it is clearly unfeasible when problem size grows.

In particular, the Bellman Ford solution of a single instance, for all combinations, can get up to `O(n^4)` when density is high, which means it will provide results in a time proprtional to `n=1000 -> 10^(12)`, and it is required to do for many many instances of the same problem. I deemed it not useful to wait several months if not years to solve completely those instances, so I introduced some sanity check limits to ensure I got the results in time.

## Results
I saved all solutions in `results`, each file contains the problem instance information, and json results contain
```
example

  {
    "source": 0,    
    "target": 1,        
    "my_cost": 567.0,
    "nx_cost": 567.0,
    "my_time": 0.0,                     #In seconds
    "nx_time": 0.002574920654296875,    #In seconds
    "equal": true                       #If my cost vs nx cost is the same
  },
```

