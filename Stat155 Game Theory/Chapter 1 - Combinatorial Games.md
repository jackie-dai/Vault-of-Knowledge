## PBICB

A **combinatorial game (CG)** has
- two players
- set of positions X
- set of legal moves between positions 

**Progressively bounded (PB)** - for every starting position, there is a finite number of moves until the game terminates

**Impartial** (I) - the winning positions and number of available moves are the same for both players

**Partisan** - the opposite of impartial. The terminal nodes and moves available to each player is different

## Sprague-Grundy Function

**Minimal Excludant (MEX)** - the smallest non-negative value NOT in the set
 mex({1, 2, 3}) = 0
 mex({0, 1}) = 2

$$g(x) = mex[g(y) : y ∈ F(x)]$$



