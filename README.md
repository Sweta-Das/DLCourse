# Knowledge Graph

- a data model that represents real-world entities and their relationships in a graph structure
- It is like a semantic network where information is organized as a network of interconnected "things" rather than isolated pieces of data.

## Key Components:
- **Nodes**: Represents the entities, such as a person, place, or object
- **Edges**: Represent the relationship between nodes; it gives the graph its meaning and context
- **Properties**: Key-value pairs that provide additional info about the nodes and relationships

# Neo4j

- a leading graph database i.e., specifically designed to store, manage, and query knowledge graphs
- It stores connections between data points natively, unlike traditional databases that store data in tables and require complex "joins" to find relationships
- Native connection between data points make the processing fast and efficient for tasks involving navigating interconnected data

## Key Features:
- **Native Graph Architecture**: Built from the ground up to handle graph data, with nodes containing direct pointers to connected nodes. Effective for relationship-heavy queries.
- **Cypher Query Language**: Neo4j uses a declarative query language called Cypher, which is optimized for working with graphs. It uses a simple, readable syntax that resembles ASCII art to describe patterns in the data.
- **Flexibility**: Schema-optional database, allowing for easy updates and additions of new data without a rigid, predefined structure.