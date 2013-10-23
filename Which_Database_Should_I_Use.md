
Which Database Should I Use
===========================

by: Andrew Oliver; @aoliver

Founded POI hosted at Apache

## Why not use RDBMS? ##

CAP Theorem:

 * Consistency - transactions
 * Availability - redundancy
 * Partition Tolerance - scale

RDMBS great at consistency and availablability, not at paritioning (scaling)

In a single process model, thousands of connections to single database system

Disk speeds didn't historically scale with CPU

ANSI2002, extended queries?

RDBMS based on relational algebray or set theory

Not all problems have direct path

Some database needs higher availability; one size doesn't fit all

Storage is cheaper, so there's more demand for storing more

Operational vs Analytical
 * one db type can't solve all designs
 * operationsl systems == lightweight transations
 * analytical systems == long running reports, charting

## Other types of DB ##
### Key value Stores ###
 * Cassandra
 * Couchbase

 * Constant Time Lookup by Key Combined
   with index for searches 
 * great for map  Reduce 

 * List item

Very Scalable


### Column Family/Big Table
### Document databases
 * Couchebase, CouhDB, MongoDB
 * nativly speak json
 * key-value store understands values
 * large datasets require indexes
 * operational store

###Graph Databases
 * Graph Theory (didn't know this existed....)
 * transactional
 * index required for searching (paired)
 * rows are tables
 * Neo4j is an example db

###Hadoop
 * (why is this guy called out so differently)
 * not a database, software framework
 * excellent for data processing and/or analysis

### Others
 * Triplestores: Apache Jenna
 * OODBMS/ORDMS (ousted! they apparently have too many shortfalls): Caché

## Considerations
 * persisteance
 * replication
 * availability
 * trnsaction consistency
 * locality
 * language

## Conclusions
* RDBMS may not scale per needs
* data may not map efficiently in tables
* Kay Value store can't handle complexe data
* Colum Family/Big Table are fast and scalable, not great for huge data

RDBMS for most correct transactions, need to ANSI something
structure of the data is important

@acoliver

If you're on the endge of choice:
* Analyze what you goals maybe in the future

Solr is a Merge Index based on Lucene


