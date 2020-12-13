# Element: location

**Element tag** `<location>`

**Description** An object describing a geographic location. 


## Sub-Element: continent

**Element tag** `<continent>`

**Description** The two letter code describing the continent of the location.

**Non-repeatable, Required**

**Data values:** One of the two letter codes: *AF, NA, OC, AN, AS, EU, SA* or *AU*. (codes stand for Africa, North America, Oceania, Antarctica, Asia, Europe, South America, Australia)

### Tagging Examples:
`<continent>NA</continent>`

`<continent>OC</continent>`

## Sub-element: [geoCoordinates](coordinates.md)

**Element tag** `<geoCoordinates>`

**Description** An object describing a geographic location using the Geographic coordinate system.

**Non-repeatable, Optional**

**Data values:** [coordinates](coordinates.md)

### Tagging Examples:
```
<geoCoordinates>
    <longitude>-71.100082</longitude>
    <latitude>42.339199</latitude>
</geoCoordinates>
```

## Sub-Element: [postalAddress](postalAddress.md)

**Element tag** `<postalAddress>`

**Description** The location as specified by mailing address components. Complete as many fields as possible, even if the location is not at a specified street address location.

**Non-repeatable, Optional**

**Data values:** [postalAddress](postalAddress.md)

### Tagging Examples:
```
<postalAddress>
    <addressCountry>US</addressCountry>
    <addressRegion>California</addressRegion>
</postalAddress>
```

```
<postalAddress>
    <addressCountry>US</addressCountry>
    <addressRegion>Illinois</addressRegion>
    <addressLocality>Chicago</addressLocality>
    <postalCode>60613</postalCode>
    <streetAddress>1060 West Addison</streetAddress>
</postalAddress>
```

## Sub-Element: unknownLocation

**Element tag** `<unknownLocation>`

**Type:** `xs:boolean`

**Description** Only use `true`. Rather than set this field to `false` for a known location, set the other location fields with more details.

**Non-repeatable, Optional**

### Tagging Example:
`<unknownLocation>true</unknownLocation>`

## Sub-Element: locationDescription

**Element tag** `<locationDescription>`

**Description** A free text description of the location, prioritizing any details not described in other schema fields. 

**Non-repeatable, Optional**

### Tagging Examples:
`<locationDescription>20 miles from the nearest road, just below a ridgeline in a desolate area just north of Mt. Shasta. In the Marble Mountains.</locationDescription>`

`<locationDescription>Loch Ness, Scotland, is a freshwater loch that is located in the Scottish Highlands.</locationDescription>`

`<locationDescription>The Norwegian Sea is a marginal sea within the Arctic Ocean.</locationDescription>`