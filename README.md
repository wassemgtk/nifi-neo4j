#### A NiFi Connection Pool Service and Cypher Processors for Neo4j 3.0

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/53c3e4e2e4334133a1790c4b46ea8800)](https://www.codacy.com/app/Qordoba/nifi-neo4j?utm_source=github.com&utm_medium=referral&utm_content=wassemgtk/nifi-neo4j&utm_campaign=badger)

A collection of tools for accessing Neo4j graph databases from Apache NiFi.

**_This is alpha quality software and is not currently actively maintained. It is not intended for use in a production environment._**


Requires:
* Nifi version 1.0.0
* Neo4j version 3.0

Features:
* Uses the Bolt binary protocol Java driver released with [Neo4j 3.0](http://neo4j.com/blog/neo4j-3-0-massive-scale-developer-productivity/)
* Configurable NiFi connection pool service
* PutCypher processor for updating Neo4j
* Supports parameterised cypher queries for primitive property types (float, string, boolean and integer) - see processor usage documentation details.
* _(coming soon)_ GetCypher processor for fetching data, with support for streaming arbitrarily large query results 

Limitations:
* Only executes single queries - no support for multiple queries in a transaction
* No tests included yet

#### Setup & Usage

1. Either build from source or download the latest release
2. Put the .nar files in the nifi lib directory and remove any old versions
3. Start (or restart) NiFi
4. Create, configure and start a Neo4j Bolt Session Pool service
5. Create and configure a cypher processor in your flow

