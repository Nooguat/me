## Recalls on blockchain
- Way of representing data, divided in blocks; signed one from another.
- Generally used for transactions as the data is virtually uneditable 
- Blocks are validated by proofs either *work* or *stake* (stake is less power-needing) that generate signatures based on content (if modified ; signature become invalid)
### Differences between blockchains and databases
The two are manners of storing data. Differences are all fields ; from data integrity to structure
- The blockchain is decentralized ; data integrity is virtually unattackable 
- The database can do **CRUD** operations (Updates and Delete; not possible with blockchain); queries are fasters than the blockchain
### Combining the two
(*This use MongoDB Atlas; TODO check for others systems*)
- The main issue with blockchain is the **scalability** : as the most of the nodes needs to validate a new one; the more blocks the longer
Blockchain database is a blockchain with blocks stored inside a database; which permits queries and adding new blocks to the chain 

