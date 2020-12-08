# Element: coordinates

**Element tag** `<coordinates>`

**Description** An object describing a geographic location using the Geographic coordinate system


## Sub-Element: longitude

**Element tag** `<longitude>`

**Type** `xs:decimal`

**Description** The longitude of a location. 

**Required**	

**Data values:**  Use decimal format, e.g. -122.08585



## Sub-Element: latitude

**Element tag** `<latitude>`

**Type** `xs:decimal`

**Description** The latitude of a location. 

**Required**

**Data values:**  Use decimal format, e.g. 37.42242

### Tagging Examples:
```
<geoCoordinates>
    <longitude>-71.100082</longitude>
    <latitude>42.339199</latitude>
</geoCoordinates>
```