##Element: location
**Element tag** <cs:location>
**Description** An object describing a geographic location
**Non-repeatable, required**
//Not quite sure if this is correct//

##Sub-Element: geoCoordinates
**Element tag** <cs:geoCoordinates>
**Type** type=xs:coordinates
**Description** An object describing a geographic location using the Geographic coordinate system
**Optional**

##Sub-Element: continent
**Element tag** <cs:continent>
**Description** An object describing the continent
**Optional**

##Sub-Element: postalAddress
**Element tag** <cs:postalAddress>
**Type** type=xs:postalAddress
**Description** An object describing a geographic location using postal code standards
**Optional**

##Sub-Element: locationDescription
**Element tag** <cs:locationDescription>
**Description** //Unknown?//
**Optional**

##Element: coordinates
**Element tag** <cs:coordinates>
**Description** An object describing a geographic location using the Geographic coordinate system

**Optional**


##Sub-Element: longitude

**Element tag** <cs:longitude>

**Type** type=xs:decimal

**Description** The longitude of a location. For example -122.08585

**Optional – but if one, then the other**	


##Sub-Element: latitude

**Element tag** <cs:latitude>

**Type** type=xs:decimal

**Description** The latitude of a location. For example 37.42242

**Optional – but if one, then the other**


##Element: postalAddress

**Element tag** <cs:postalAddress>

**Description** An object describing a geographic location using postal code standards

**Optional**


##Sub-Element: addressCountry
**Element tag** <cs:addressCountry>
**Description** The country, using the two-letter ISO 3166-1 alpha-2 country code
 
**Optional**
 
 
##Sub-Element: addressLocality
 
**Element tag** <cs:addressLocality>
 
**Description** The locality in which the street address is, and which is in the region. For example, Boston
 
**Optional**


##Sub-Element: addressRegion
**Element tag** <cs:addressRegion>
**Description** The region in which the locality is, and which is in the country. For example, Massachusetts or another appropriate first-level Administrative division

**Optional**

##Sub-Element: postalCode
**Element tag** <cs:postalCode>
**Description** The postal code. For example, 02115
**Optional**

##Sub-Element: streetAddress
**Element tag** <cs:streetAddress>
**Description** The street address. For example, 300 Fenway
**Optional**

