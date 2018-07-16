# Changes between version 1.0 and 2.0

## Introduction
This document describes the changes between versions 1.0 of the specification and version 2.0.

## Type changes
(Almost) all types have changed in version 2.0, but may not require many changes.

### Generic to all types
#### UUIDs replaced by IDs
The requirement that every object requires a fixed UUID, will be changed. Every object will now require an identifying id, which is a string. If providers want to keep using a UUID, they just need to change the name of the property to ID.

### New types
#### AspectSet
Defines an aspect set.

#### AspectSetsListResponse
Defines a list response of aspect sets.

#### Provider
Defines the provider resource type for specifying provider-specific responses.

#### ProblemResponse
Defines error information.

### Generic to all list responses
All list-responses **must** provide a links resource object.
The links resource object **must** contain the following properties:
- totalObjectCount: contains the number of records that satisfy the query requirements.
- prev: has an href property that contains the url for the previous page, if available, else null.
- next: has an href property that contains the url for the next page, if available, else null.     
- maxPageSize: maximum page size as defined by the provider.
- minPageSize: minimum page size as defined by the provider.

The links resource object **may** contain the following properties:
- self: has an href property to the current request.

### Generic to all responses
All responses **may** provide a provider resource object. For the dd-oper specification, the provider resource object is required.
The provider resource object contains the following properties:
- name: name of the provider (required)
- supportURL: URL of the provider used for support questions. (required)

The provider resource object **may** contain the following properties:
- apiVersion: the version of the API used to provide the response. (optional, may be required in a future version)
- responseType: the exact type of the response. (optional, may be required in a future version)

apiVersion plus responseType can be used to parse the response.

When a request encounters an error, a problem resource object **must** be returned.

The problem resource object **must** have the following properties:
- status: HTTP status code of the error

The problem resource object **may** have the following properties:
- type: url specific for the error type.
- title: title of the error
- detail: details of the error
- instance: internal reference to the provider system (log?)

### Specific end-points
#### /datasources
The /datasources end-point will be renamed to /resources

#### /locations
- name will become locationName
- code will become locationCode
- node will become nodeId

#### /timeSeries (generic)
Changes to the filter options:
- start will become startTime
- end will become endTime
- observationType will become observationTypeId

New filter options:
- realization: optional, required for ensembles (future)
- aspectSet: optional, specifies the aspectSet

Discussion: the following, or filter syntax?
- includeMetaData: default true. if false, only data is returned, not the references.
-  quantity: optional, filters by quantity without needing to specify observationTypeId.
-  parameterCode: optional, filters by parameterCode without needing to specify the observationTypeId.
-  locationName: optional, filters on location name, instead of locationCode.
-  sourceName: optional, allows filtering on source.

#### /aspects
The aspects is a new, but required end-point, also for systems not having aspects. Non-supporting systems **must** return an empty array.

This end-points implements aspects ??? description needed ???
