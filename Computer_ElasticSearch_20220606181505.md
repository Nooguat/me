# How elasticsearch is working
Elasticsearch is a search engine extremely fast capable of full-text search

Some logical concepts must be known before understanding how it works

- Documents: Basic unit of information that can be indexed through Elasticsearch (in JSON). Not mandatory text, but any data structure that can be written in JSON
- Indices : Collection of documents that have the same characteristics. The highest level entity that you can query against in Elasticsearch. Same as a database inside a relationnal database. 
- Inverted Index : (Mechanism used by any search engine) Data structure that stores a mapping from content, such as words or numbers, to its locations in a documents/set of documents. 

Basically a hash-map structure that directs you from a word to a document. Does not store strings directly and instead spilts each documents to individuals search terms

The power of Elasticsearch is the divsion of work through nodes connected together (called a **cluster**) and shards (subdivisions of the index)
Node structure: 
- Master node : Controls the cluster and responsible of the cluster-wide operations like creating/deleting an index and adding/removing nodes.
- Data node : Stores data and executes data-related operations such as search and aggregations.
- Client node : Forwards cluster requests to the master node and data-related requests to data nodes.
[Sources]
