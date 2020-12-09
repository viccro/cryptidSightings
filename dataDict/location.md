# Element: location

**Required**

**Repeatable**

**Element tag** `<location>`

**Description** An object describing a geographic location. 


## Sub-Element: continent

**Element tag** `<continent>`

**Description** The two letter code describing the continent of the location.

**Required**

**Non-repeatable**

**Data values:** One of *AF, NA, OC, AN, AS, EU,* or *SA*.

### Tagging Examples:
`<continent>NA</continent>`

`<continent>OC</continent>`

## Sub-element: [geoCoordinates](coordinates.md)

**Element tag** `<geoCoordinates>`

**Description** An object describing a geographic location using the Geographic coordinate system.

**Optional**

**Non-repeatable**

**Data values:** [coordinates](coordinates.md)

## Sub-Element: [postalAddress](postalAddress.md)

**Element tag** `<postalAddress>`

**Description** The location as specified by mailing address components. Complete as many fields as possible, even if the location is not at a specified street address location.

**Optional**

**Non-repeatable**

**Data values:** [postalAddress](postalAddress.md)

## Sub-Element: unknownLocation

**Element tag** `<unknownLocation>`

**Type:** `xs:boolean`

**Description** Only use `True`. Rather than set this field to `False` for a known location, set the other location fields with more details.

**Optional**

**Non-repeatable**

## Sub-Element: locationDescription

**Element tag** `<locationDescription>`

**Description** A free text description of the location, prioritizing any details not described in other schema fields. 

**Optional**

**Non-repeatable**

### Tagging Examples:
`<locationDescription>20 miles from the nearest road, just below a ridgeline in a desolate area just north of Mt. Shasta. In the Marble Mountains.</locationDescription>`
