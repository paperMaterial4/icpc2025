# Applying Program-Comprehension Questions to Graphical Software Models
Repository with additional material for paper

- chess.cypher: Set of queries to create the entity-relations-attribute model used to test the executed queries. The model represents a C++ program implementing the game of Chess, it supports two human players playing against each other, or a single human player playing against a bot with multiple options of expertise level. The whole program has 2,372 lines of code. The model of extracted program entities, relations, attributes is built by the Cypher queries in this file, where each query adds one fact to the database model
- TestableQueries: Set of queries translating questions supported by the Chess model. The TestableQueries have been successfully tested by running them on the software model for the C++ Chess program mentioned above. Each query returned at least one instance of the pattern of interest in the analyzed model.
- UnTestedQueries: Set of queries translating questions that are not supported by the Chess model. These are a best attempt to rephrase the PC questions as Cypher queries. The queries require a software model that includes information, such as excetion handling, overidding relationships, and file inclusion, that cannot yet be extracted using our current extraction tools. But, we fully believe that the necessary information can be statically extracted from a software base, so we provide the queries with the disclaimer that they have not been validated.
- ResutsExamples: this folder provides the results (outputs) of running a small set of example queries:
  - Does this type have any siblings in the type hierarchy?
  - What are unused methods?
  - What is this type's type hierarchy?
  - Where is this field declared in the type hierarchy?

  These queries were executed on the software model of the C++ Chess Program mentioned above. The results are Neo4j graphical visualizations of query results, where entities are represented as graph nodes, relations are represented as edges. If the reviewers find these results useful, we will add to the repo the results of running every TestableQuery on the software model of the C++ Chess Program.
- ModelUnSupportedQuestions: the list of 299 PC questions that can NOT be answered from a software model and their respective categories. We provide this list for PC researchers interested in trying to support these additional developer questions.
