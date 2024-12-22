# Applying Program-Comprehension Questions to Graphical Software Models
Repository with additional material for paper

- chess.cypher: Set of queries to create the entity-relations-attribute model used to test the executed queries. The model represents a C++ program implementing the game of Chess, it supports two human players playing against each other, or a single human player playing against a bot with multiple options of expertise level. The whole program has 2,372 lines of code. The model of extracted program entities, relations, attributes is built by the Cypher queries in this file, where each query adds one fact to the database model
- TestableQueries: Set of queries translating questions supported by the Chess model. The TestableQueries have been successfully tested by running them on the software model for the C++ Chess program mentioned above. Each query returned at least one instance of the pattern of interest in the analyzed model.

- nonExecutedQueries: set of queries translating questions that are not supported by the chess model.
- ResutsExamples: folder including fours examples of query output. Each subfolder has the executed query and the graph visualization returned after executing it on a Neo4j database. 
