# Hadoop and Druid
By: Eric Tschetter - Druid Daddy

DEMO: Metamarkets wikipedia edit stream - Interactive dashboard based on druid

### What it was built to do 
* Ingestion ( take data fast)
* Slice through data drill in data
* Highly available

Druid was created after they tried nosql and rdbms solutions first but because
of various problems from initial processing to queries taking too long. They
switched to creating their own solution to the problem.


### Pieces of Druid (modeled after power rangers?)
Single point of failures could be zookeeper / data stream
* Data stream data flows into realtime nodes (Query API) 
* Every once in a awhile (config) they move their readonly data into historical nodes (Query API)
* Broker nodes handle requests because they know where all the data is and
  handle routing who needs to do what (query rewrite)   (Query API)


### Data
* Column oriented
* Take columns for the data
* They create ids for everything
* Then they store it as dictionary compression
* Create bitmap index on all the rows


### Availability
* Fault tolerant
* Rolling Deployments / Restarts
* Grow == Start processes
* Shrink == Kill Processes


### Their Cluster
* 80 machine on AWS
* ~3 trillion events
* 90% query latency < 1s

