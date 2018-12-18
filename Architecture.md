# Introduction
The Digital Delta is a distributed system consisting of different data services that communicate using a common interface.

## Nodes
The data services consists of one or more nodes, being a data source that *may* be restricted in access.
Nodes can be either free (for public information), or require authentication secured by OpenID Connect (see [OpenidConnect document](OpenIDConnectDocument)).  

## Resource objects
The Digital Delta specification uses Resource objects.
A resource objects consist of entities, each with a set of attributes. An attribute has a type and *can* have restrictions. The RAML definition specifies these.
In version 2.0.1 of the API specification, the requirement of an ID needing to be a universally unique identifiers has been dropped. The ID is now a string. This is less restrictive for the data sources.

In this chapter all object are written down in tables. The implementation of these resources into a data model is up to the data node; the Digital Delta does not specify how data nodes store data in their persistence layer; the object tables represent the way information should be returned. The Digital Delta uses uuids (universally unique identifier, version 4) for identification of resource objects. The use of uuids guarantees a unique identifier for an instance over all nodes in the Digital Delta without the need for individual nodes to have a knowledge about data in other nodes. There is a code attribute as well that can be used by suppliers for their internal identifiers.
