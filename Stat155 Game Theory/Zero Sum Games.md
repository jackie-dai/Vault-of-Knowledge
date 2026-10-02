
Example: pick a hand. The hider holds up either 1 or 2 fingers. The chooser picks one hand and gains the amount of points on that hand (0, 1, or 2)
$$
\begin{array}{cc|cc}
 & & {\text{Hider}} \\
 & & L1 & R2 \\ \hline
\text{Chooser} & L & 1 & 0 \\
 & R & 0 & 2
\end{array}
$$

## Expected gain/loss
If hider chooses L1 with probability y1, and R2 with probability y2 = (1-y1)
The expected loss given chooser chooses L is E[y1 | x=l] = 1(y1) + 0(1-y1) = y1
The expected loss given chooser chooses R is E[y1 | x=R] = 0(y1) + 1(1-y1) = 1-y1


## Definitions

Payoff matrix 
$$
\begin{array}{cc|cc}
 & & {\text{Hider}} \\
 & & L1 & R2 \\ \hline
\text{Chooser} & L & 1 & 0 \\
 & R & 0 & 2
\end{array}
$$
Player 1's worst case is min $a_{ij}$, so their goal is to maximize the min $a_{ij}$
Player 2's worst case is max $a_{ij}$, so their goal is to minimize the max $a_{ij}$


Mixed strategy - a player plays each with move with some probability
Pure strategy - a player plays one move with probability 1

### Saddle Points

### Domination 