# Digital Delta web service API specification version 2.0
Version 2.0 of the Digital Delta API builds on the foundation as specified in [version 1.0](https://github.com/DigitaleDeltaOrg/dd-api-spec/blob/master/README.md).
The main new feature of version 2.0 is the addition of Aspects sets to allow expectations and predictions to be retrieved.

Due to the nature of the changes, version 2.0 is not backwards compatible with version 1.0.
The status of this specification is **draft**.


## The specification
The [Generic version 2.0](dd.v20.raml) of the specification is the 'general purpose' specification.
The main changes compared to version 1.0 are:
- Aspects have been added for aspect-oriented measurements and expectations.
- Locations results are converted to GeoJSON.
- uuid (UUID type) will be replaced with id (string), to make the definitions less rigid.
- Source object added. Replaces DataSource and TimeSeriesType.
- problem-block added to allow for more specific error reporting.
- /datasources is replaced by /sources.
- paging-related parameters are now moved to the links-block. count has been renamed to totalObjectCount.
- optional provider-block has been added. Contains provider-specific information, including response-version, response-type, etc.
- optional inclusion of the query syntax as defined in the Digital Delta Eco API.
- Required /aspectsset endpoint added. Systems not supporting Aspect sets must return an empty list.

The [Operations version 2.0](dd-oper.v20.raml) extends the is a specific version developed for Rijkswaterstaat, designed to retrieve data using fixed, strict paths, with the purpose to be able to cache request/responses.

For a more complete list of changes between version 1.0 and 2.0, please see [here](changes_between_1.0_and_2.0.md).

The parties involved in drafting this specifications (alphabetically) are:

| Organisation | Contact |
| --- | --- |
| Deltares |  |
| EcoSys |  |
| Hydrologic | |
| Nelen &amp; Schuurmans | |
| Rijkswaterstaat |  |
| Vortech |  |  |


The current implementations of this specifications and their status are:

| Organisation | Product | Status |
| --- | --- | --- |
| Deltares |  |  |
| EcoSys |  |  |
| Hydrologic | |  |
| Nelen &amp; Schuurmans | |  |
| Rijkswaterstaat |  |  |
| Vortech |  |  |   |
