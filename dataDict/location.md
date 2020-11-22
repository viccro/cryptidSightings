##Element: location

**Element tag** `<cs:location>`

**Description** An object describing a geographic location. 

##Sub-element: coordinates

**Element tag** `<cs:coordinates>`

**Description** An object describing a geographic location using the Geographic coordinate system

**Optional**

**Data values:** [geoCoordinates](geoCoordinates.md)


##Sub-Element: continent

**Element tag** <cs:continent>

**Description** The two letter code describing the continent of the location.

**Required**

**Data values:** One of *AF, NA, OC, AN, AS, EU,* or *SA*.


##Sub-Element: [geoCoordinates](coordinates.md)

**Element tag** `<cs:geoCoordinates>`

**Description** The geospatial coordinates of the location

**Optional**

**Data values:** [geoCoordinates](coordinates.md)

##Sub-Element: [postalAddress](postalAddress.md)

**Element tag** `<cs:postalAddress>`

**Description** The location as specified by mailing address components. Complete as many fields as possible, even if the location is not at a specified street address location.

**Optional**

**Data values:** [postalAddress](postalAddress.md)

##Sub-Element: unknownLocation

**Element tag** `<cs:unknownLocation>`

**Type:** `xs:boolean`

**Description** Only use `True`. Rather than set this field to `False` for a known location, set the other location fields with more details.

**Optional**


##Sub-Element: locationDescription

**Element tag** `<cs:locationDescription>`

**Description** A free text description of the location, prioritizing any details not described in other schema fields. 

**Optional**

