# Digital Delta API Specification Version 2.0

Version 2.0 of the Digital Delta API builds on the foundation as specified in [version 1.0](https://github.com/DigitaleDeltaOrg/dd-api-spec/blob/master/README.md).

See the [Digital Delta project](http://www.digitaldelta.nu/en/phase-3-operational-phase/item340) for some back ground information.

The changes in version 2.0 compared to 1.0 can be summarized as:

* Renaming of some attributes, e.g. for consistency reasons, or to clarify the content of the attribute
* Adjusting some resource object types in the response in order to let them adhere better to standards. For instance, the Location objects now is a GeoJSON object) and the paging information has been re-arranged according the DSO API guidelines.
* Adding attributes to the Timeseries object that facilitate the definition of computation results and ensemble runs.
* Adding interval information to the values in a Timeseries
* Adding the concept of aspect sets, a mechanism to group related time series, e.g. the minimum, maximum and average of a measured quantity, or the direction and amplitude of wave field.

Due to the nature of the changes, version 2.0 is not backwards compatible with version 1.0.  

The status of this specification is **draft**.

## Naming
Some terms used in this document have a specific meaning:
- **must**: implementation is **required**.
- **may**: implementation is **optional**.
- **should**: implementation is **recommended** due to future changes.  

## The specification
Version 2.0 includes two specifications.
The generic [DD-API version 2.0](dd.v20.raml) of the specification is the 'general purpose' specification, with url's that facilitate both searching for and retrieving data. Hence it both for discovery and for getting data.

The [Operational extension "dd-oper"](dd-oper.v20.raml) is an extension developed for/by Rijkswaterstaat, designed to retrieve data using a fixed strict url-path. It only differs from the generic version in the url-syntax. The dd-oper-url does not support discovery.

The changes between version 1.0 and 2.0 are described [here](https://github.com/DigitaleDeltaOrg/dd-api-spec/blob/2.0/Documentation/Changes_between_1.0_and_2.0.md).

## Parties
The parties involved in drafting this specifications are, in alphabetical order:
<table>
    <tr>
        <td><b>Organisation</b></td>
        <td><b>Contact</b></td>
    </tr>
    <tr>
        <td>Deltares</td>
        <td>Stef Hummel</td>
    </tr>
    <tr>
        <td>EcoSys</td>
        <td>Geri Wolters</td>
    </tr>
    <tr>
        <td>Hydrologic</td>
        <td>Sander Loos</td>
    </tr>
    <tr>
        <td>IBM</td>
        <td>Jurgen Boerboom</td>
    </tr>
    <tr>
        <td>Nelen &amp; Schuurmans</td>
        <td>Jan-Maarten Verbree</td>
    </tr>
    <tr>
        <td>Rijkswaterstaat</td>
        <td>Flip Dirksen</td>
    </tr>
    <tr>
        <td>VORtech</td>
        <td>Jeroen Gerrits</td>
    </tr>
</table>

See [version 1.0](https://github.com/DigitaleDeltaOrg/dd-api-spec/blob/master/README.md) for the currently available implementations of the Digital Delta API.
