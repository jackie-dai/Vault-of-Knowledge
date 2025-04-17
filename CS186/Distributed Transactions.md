  
When do we commit a xact that is processed by multiple machines

2PC
Coordinator and particpant

Phases
1. Voting
2. Results

**Must be a unanimous decision**
## Phases
### Voting
1. Coord broadcasts a "Prepare message"
2. Participants send back "yes" or "no"

## Results
3. Coord processes responses
	1. if all yes -> commit, otherwise -> abort



### Optimization
- All or nothing
