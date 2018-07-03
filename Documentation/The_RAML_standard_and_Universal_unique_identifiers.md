The <a href="http://raml.org">RAML specification</a> currently doesn't know the type uuid (Universal unique identifiers). To have a structure in the definition to allow working with uuids, the Digital Delta specification uses a strong with a specific regular expression pattern.   
The base pattern is&colon; [0-9a-f]{8}-([0-9a-f]{4}-){3}[0-9a-f]{12}.</i>
