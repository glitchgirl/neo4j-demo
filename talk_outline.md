:star2:
Hey everyone and welcome to an introduction to graph databases! I promise it isn't as scary as it seems.
Before we get started, I wanted to talk a little about me, a little about anything y'all will need if you want to follow along, and some rules.
:star2:
So first's things first:
ASK QUESTIONS!! Please raise your hand, ask questions. This stuff can get confusing and there are few questions I love more than "why why why why".
:star2:
Secondly, I will be using docker for this demo so you will need to have it installed if you want to follow along. Also, make sure you download the correct one, there are two chip versions. You don't need any coding knowledge, container knowledge, or database knowledge to follow along. 
I also have links and other info in this repo - I can slack this to y'all also. 
:star2:
A little about me, and why y'all should listen to me. My name is Morgan Smith, I have been at Phase2 for about 6 months, I am on the APS team. In my free time, I am on a roller derby team, I enjoy reading, and making art. I have been a software developer about 5 years, and I have hated SQL the entire time. It's just not my jam, its not how I think about data, especially relational data. 
:star2:
So lets talk about data and databases.
Whats data?
According to oxford it's 
`facts and statistics collected together for reference or analysis.`
or
`the quantities, characters, or symbols on which operations are performed by a computer, being stored and transmitted in the form of electrical signals and recorded on magnetic, optical, or mechanical recording media.`
Thats dense, but what we care about is the fact that data is just anything that we can store and is important. The idea that the data is important is critical to data science, and just generally making effective choices. For example if you are trying to make a choice about whether or not bring an umbrella out with you, you don't care about what phase the moon is in. The moon's phase isn't data, its just noise. The wind, and chance of rain are the data points that we care about. We can expand this idea to also think about bigger picture things, like what data is useful to show a person on their profile for example. 

What's a traditional database?

A quick note on no sql -

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
Biological/health sciences (this is what i used to do) 
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
