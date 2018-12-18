# Research topics from version 1.0 of the DD-api
## Attribute standards
Attributes for different standards: for now the standard IMWA measurement format will be used. No other attributes that are needed from other standards are added.  A proposal has been made to add additional standards and attributes to the ObservationType.

__Biological Taxa are no longer defined in observation types. They are listed in the TWN standard, which is part of the Aquo-standard.__

__The DD_ECO-API specification already made a start for implementation of reference systems.__

## Multiple data types.
Support for multiple data types: future API versions will include more data types, such as forecasts, gridded and vector data.

__ Forecasts are part of the DD-OPER-API.__

Additional output formats: currently, the data is returned as an Aquo-compliant output. In a future version, multiple output types should be supported, for example WaterML 2.0.
__Aquo-compliancy is a responsibility of the source systems. The DD-API cannot convert non-compliant types to Aquo-compliant types. Because the Aquo-standard is also continuously changing, it would mean that the source systems will need to continuously change their data.__

## Calculations
Support basic calculations on time series data: create an endpoint that returns the mean or maximum of a measurement series.

__This is part of the aspects in the DD-OPER-API.__

## Smart references
Allow references to objects within the specifications. This has the potential to reduce the size of the resulting output. It makes parsing of the format harder though.

## Searching
Searching observation types based on specific standard fields must be implemented in the node that is implementing the specific standard. The nodes should handle these requests and use the “standard” filter in the request so the node knows which fields to use in the search process. The Digital Delta specification is not defining the implementation of this, but requires the functionality to be able to search with some important detailed fields of the standard (minimal: code, name, description, etc). If a standard is not implemented or the ‘standard’ field is not used in the requests, then the minimal response is provided with the observation type fields only.

__For searching, the filter-syntax of the DD-ECO-API can be implemented. The HHNK implementation used this technique to address the problem of locating locations in a GeoJSON multi-polygon.__
