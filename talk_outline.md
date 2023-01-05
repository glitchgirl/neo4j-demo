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
Thats dense, but what we care about is the fact that data is just anything that we can store and is important. The idea that the data is important is critical to data science, and just generally making effective choices. For example if you are trying to make a choice about whether or not bring an umbrella out with you, you don't care about what phase the moon is in. The moon's phase isn't data, its just noise. The wind, and chance of rain are the data points that we care about. We can expand this idea to also think about bigger picture things, like what data is useful to show a person on their profile. 
:star2:
As humans, we have a limit to how much data we can remember and use, so we use databases to store data.
What's a traditional database?
`a structured set of data held in a computer, especially one that is accessible in various ways.` What this means, its a standard way of organizing data, with rules about how to get the data. These are really useful for structured data, like geo-location data, credit card infomation, or stock prices. 
This is typically done with a sql database, in any of it's flavors (mysql, oracle, postgre). However, these kind of structure doesn't apply to all data, and these types of databases can really struggle with data where the relationships can change over time. One way we can deal with these changelles is nosql.
NoSQL databases can include things like key-value structures, document storage. Common examples include things like mongo. The benefits of these systems include things like partition tolerance and availability. For example, let's say we had a SQL database for e-commerce system. It has, customers, items, and orders. Let's say then, due to some privacy laws, we had to delete old customers, however for taxes we need to keep the order history. In a traditional SQL database, this could cause lots of issues with null refrences. NoSQL would handle this example by keeping the data in the order, but not the refrence. 
:star2:

This is was a small example, and in our data landscape today, data and relationships between the data can change frequently, and sometimes we care more about the relationships, than the data. 
This is where graph comes in. So graphs are mathematical structures used to model pairwise relations between objects. Oof. Also dense. Let's look at pictures.  
Awesome, we know what a graph is, and we know what database is. 
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

Alright! So we have talked about what data is, what a database is, why traditional databases might not always be the best solution for data managament, espically when it comes to things like rapidly changing data. Lets take a look at Neo4j! 
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

Next steps:
If you are interested in this, I recommend playing with this. I also recomend setting up insomnia for API testing, since postman doesn't super behave well with graphQL apis. They have been saying they have fixed it, so it might work beter now. 
I also recommend learning a little bit of discrete math to understand how these structures work. And I know that sounds scary, but its math with pictures!! So its not bad.
I do also recommend taking some data science classes.
Any questions?

Thanks! 
