

## Types of voting


Plurality Voting
The candidate with the most number of votes.


Borda Counting

## Definitions
- $\Gamma$ the set of candidates.
- $\succ_i$ voter \(i\)’s ranking of the candidates.
- $\pi=(\succ_1,\ldots,\succ_n)$: everyone’s rankings collected together, called a **preference profile**.
- $(f)$: the method used to choose the winner, such as plurality or Borda count.

	Voting Rule
- produces a single winner

Ranking Rule
- A > B B > C => A > B > C (transitive)
- Produces a social ranking

Independence of Irrelevant Alternatives (IIA)

## Properties for Voting and Ranking Rules
- Anonymity (symmetry): 
	- A voter should not hold more power than another
- Monotonicity
	- If a voter moves a candidate up without changing the other preferences, it should not move that candidate down
- Condorcet Winner Criterion
	- If a candidate beats all others in a pairwise contest, the candidate should be the winner
- IIA with Preference Strengths
- Cancellation of Ranking Cycles


###  Instant Runoff Voting (IRV)
In a round with m>2 candidates, the candidate with the fewest first place votes is eliminated, then a new round begins amongst the m-1 candidates. 

When m=2 candidates, a majority rule is applied to elect the winner.