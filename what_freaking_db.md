# Which freaking database should I use
By: Andrew C. Oliver

###  RDBMS
* Great at consistency 
* Not great at scaling

### Single process model (Usually RDBMS type model, acidy and such)
* Usually have lots of servers with many connections to few servers

### Multiprocess model (The hole fault tolerance and scalability win win)
* Usually have a lot of servers with distributed connections

### Historical Scalability
It was shit, hardware made a great 


### Mathematical model
* RDBMS is based on relational algebra based on set theory 
* Not every problem is a set problem "direct Path" or "which thing contains other
thing which has this other thing" (FOAF)
* Sometimes relationships are as important as the data
* Sometimes data is simpler than the relational model but needs higher levels of
availability
* One size never really did fit all


### Datarrhea
* The cheapness of storing data has yielded more demand
* * Economics predicted this
* Moore's law ended while yous slept
* Massive parallelization is the most feasible way to get at it (counter
  trended with an explosion in disk speeds)


### ..but
* if
* * your data is tabular
* * fits cleanly in a relational model
* * Don't have scale issues
* * Don't have a large dataset
Then use this RDBMS model


### Operation vs Analytical
* One db type is unlikely to be well suited for all your problems
* The system doing "Short and sweet" "Lightweight" transactions is your
  operational system
* The system doing long running reports is analytical and the system doing the
  light weight queries is operations
* There is also search or so he says, assume this


### Key value stores
* Constant time O(1) lookup by key
* good enough for :right now stock quotes
* Usually combined with an index for search 
* generally works well with mac reduce
* scales very well


### Column Family big table
* Mang key-value store
* Keys and values become composite
* Damnit he moves so fast


### Document databases
* JSON documents
* Couchbase, CouchDB, MongoDB
* Key value store that understands the values
* Not as map-reduce friendly, larger data set require indexes
* operational store


###  Graph databases
* Based on graph theory
* Less about bolume of data more about ocmplexity
* Many are transactionl
* * Often the transactions are "more correct" than those offered by a relational
  database
* FOAF, direct path operations are easy
* * Very complicated / inefficient in RDBMS
* Usually paired with an index for search


### Where does hadoop fit
* NOSql
* Software frameworks
* * Pig
* *  ETC
* * ETC
* excellent chouce for data processing and data analytics
* MapReduce

he moves so fast wtf...
Convergence of filesystems and database
hadoop HDFS


### Other Derivations --shit
* Triplestores
* * Apache Jenna
* OODBMS/ORDMS
* * Cache


### Things to consider
* Persistence
* * Async / Sync
* Replication
* Availability
* Transactions / Consistency
* "locality" detecting the best node to go to in a multiple instance setup
* Language

Solr Lucene
* Merge index, most similar to a document database

### Conclustions
* RDBMS may not scale to your needs, Obviously
* Your data may not map to tables
* Key value store data by, key fast, scalable cant handle complex data
* Column  family fast, scalable denormalized, map reduce, good for series


The real important thing to take away is that there is no one silver bullet.
You might store data in one method and then load it into another to perform
analytics on the data.  For example in analysing emails you might store data in
a filesystem or document store and then load metadata into a graph search to
find certain relationships between data and what has you.  


