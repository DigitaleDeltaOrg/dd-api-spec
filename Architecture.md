# Introduction
The Digital Delta is a distributed system consisting of different data services that communicate using a common interface.

## Nodes
The data services consists of one or more nodes, being a data source that *may* be restricted in access.
Nodes can be either free (for public information), or require authentication secured by OpenID Connect (see [OpenidConnect document](OpenIDConnectDocument)).  

## Resource objects
The Digital Delta specification uses Resource objects.
A resource objects consist of entities, each with a set of attributes. An attribute has a type and *can* have restrictions. The RAML definition specifies these.
In version 2.0.1 of the API specification, the requirement of an ID needing to be a universally unique identifiers has been dropped. The ID is now a string. This is less restrictive for the data sources.
