# Time Complexity
b = branching factor
d = depth of shallowest goal

## BFS
- Only found goal when popped off agenda
- Popped off when children are being generated.
- O(b^(d+1)) - Worse case
- O(b^d) - Best case

## DFS
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

# Least Cost
- Cheapest comes off agenda - priority queue.
## Time + Space
- Worst case O(b^m) 
- Best case O(b^d)