
What is a graph database?

A graph database is according to wiki, In computing, a graph database is a database that uses graph structures for semantic queries with nodes, edges, and properties to represent and store data. A key concept of the system is the graph.
Thats not super understandable, lets break it up and look some pictures
https://neo4j.com/blog/uncommon-use-cases-graph-databases/
This is a way of building a database that focuses on the relationships that might be more complicated than what a traditional database can. 
There are two main flavors of graph, and we will talk about them.

What problems does it solve?

Graph databases are great at solving complex relational data, like 
Social media
Contact tracing
Family trees
Biological/health sciences (this is what i do) 
In a traditional database, these relationships can be hard to model
Graph databases are also extremely flexible

What are some common implementations?
 
Neptune - AWS

Spark RDF

Gremlin - Apache

Neo4j - neo4j 
Cypher Graph Language 


Neo4j demo
1) download docker - https://www.docker.com/products/docker-desktop
2) pull neo4j image https://hub.docker.com/_/neo4j
3) run command to start
  ```
  docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$HOME/neo4j/data:/data \
    neo4j
 ```
 4) go to localhost:7474
 5) play!
