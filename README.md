# Shortest Path
In this lab we were required to implement shortest path algorithms.

## Dijkstra and Bellman-Ford
In the first part I implemented Dijkstra algorithm and Bellman-Ford algorithm for shortest path
- I used Dijkstra for positive edges problems since it is more efficient
- For negative edges problems I used Bellman Ford

I then compared my results to those given by nx.

My intention was to compare the problems for each pair of vertices but the time complexity makes it unfeasible, so I opted to just test for a small subset of pairs.

I got the same results from my algorithm and from nx's. I saved the results in `problems` folder

## A* algorithm
I then implemented a A* variant for the problem in which I used the euclidean distance from pairs of points as the heuristic function.

As coordinates I used those provided by `map` in create_problem.

Also for the sake of time, I just tested one pair for problem instance.

Since A* is a special instance of Dijkstra, it didn't make sense to test it on negative edge problems, so I just tested positive edge problems.

You can find the results in `astar` folder.

