# Completeness
- Will guarantee a solution
- DFS is not.
- BFS is - infinite loops will not be visited.

# Optimality
- Does it guarantee to find shortest path.
- BFS goes level by level, worse case is b^d+1, will be optimal. YES.
- DFS is not.

# Admissability
# State Space algo
- Remove from agenda
- Insert successors into agenda
- State space = all states available from the search tree.
- Visits in state space = search tree.
- Re-exploration - can visit states more than one
	- Avoid any succ that is curr nodes parent: doesnt solved if not parent loop
		- Doesnt solve reexp
	- Avoid same node in curr path: doesnt solve reexp in all probs
	- Avoid previously visitied nodes: expensive space complexity.
- Cycles: May have a cycle if keep going depth first.

# Time Complexity
b = branching factor
d = depth of shallowest goal

## BFS
- Queue agenda.
- Only found goal when popped off agenda
- Popped off when children are being generated.
- O(b^(d+1)) - Worse case
- O(b^d) - Best case

## DFS
- Stack
m = length of the longest path
- Suceptipal to cycles so m has to assume there is no cycles :/
- Will go down until depth m for each path.
- O(b^m) -  Worse case - Worse, not optimal. Not complete due to cycles.
- O(bd) - Best case - much better.

# Space Complexity
## BFS
- Same as Time.
## DFS
- Remove states without successors - reclaim space.
- Remove states that are confirmed not to have goal.
- Use space that was just reclaimed - space needed for each layer can be reused when branching factor is constant.
- O(bm) - (+1) - Worst case.
- O(bd) - Best case

# Least Cost, Greedy, A*
- Cheapest comes off agenda - priority queue.
## Time + Space
- Worst case O(b^m) 
- Best case O(b^d)

# Least Cost
- Priority Ordered Que, In order of path cost full path.
- Not complete - Path may look cheaper, extend it infinitely.
- Complete if action costs are positive.
- Optimal - Always extend cheapest path

# Informed
## Greedy
- Not complete - heuristic doesnt accumulate.
- Optimal - if heuristic is misleading, no
## A*
- Most promising code according to heuristic is always expanded. Like Least cost except uses heur. If heuristic is admissable, it will always under-estimate and never over estimate.
- How much it will cost to get here + heuristic.
- Yes complete,
- Is optimal if heuristic is admissable, due to heuristic never overestimating.

# Comparing heuristics
- Find if one is admissable.
- Difference between estimates and actual costs.