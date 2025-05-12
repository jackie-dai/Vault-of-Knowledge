
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
Query different parts of the database in parallel
Pros:
- good for write-heavy operations because they only need to access one machine
Cons
- Ineffective for read-heavy operations because they need to access multiple parts of the database (i.e. joining)

### NoSQL Models

#### Key-value stores (KVS)
Only contains key-value pairs
- Pair(String/integer uuid, byte-array value)

Application must serialize and deserialize the byte array values

