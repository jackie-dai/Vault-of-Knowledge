
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


### Json
JSON must be one object

Json datatypes: 
- **Object**: collection of key-value pairs. Keys must be strings. Values can be any JSON type (i.e., atomic, object, or array). Objects should not contain duplicate keys. Objects are denoted using “{“ and “}” in a JSON document.
    
- **Array**: an _ordered_ list of values. Values can be any JSON type (i.e. atomic, object, or array). Arrays are denoted using “[” and “]” in a JSON document.
    
- **Atomic**: one of a number (a 64-bit float), string, boolean or `null`.

XML and JSON representation of the same object
![[Pasted image 20250511233814.png]]