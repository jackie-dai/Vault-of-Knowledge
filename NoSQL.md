
### Two classes of relational databases

#### Online Transaction Processing (OLTP)
High number of transactions and updates
- Many updates
#### Online Analytical Processing (OAP)
high number of joins and queries
- No updates


### Background


### Three-tier Architecture
![[Pasted image 20250511211117.png]]
- App servers are replicates that only keep track of which clients they are connected to
- The server holds the common state and communicates with the app servers

### Methods for Scaling Databases

#### Partitioning
Pros

Cons
- Ineffective for 