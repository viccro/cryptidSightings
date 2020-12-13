# Element: postalAddress

**Element tag** `<postalAddress>`

**Description** An object describing a geographic location using postal code standards


## Sub-Element: addressCountry

**Element tag** `<addressCountry>`

**Description** The country component of the location.
 
**Optional**

**Data values:**  Use the two-letter ISO 3166-1 alpha-2 country code.

### Tagging Examples:
`<addressCountry>US</addressCountry>`

`<addressCountry>GB</addressCountry>`

`<addressCountry>NP</addressCountry>`

## Sub-Element: addressRegion

**Element tag** `<addressRegion>`

**Description** The region in which the locality is, and which is in the country. 

**Optional**

**Data values:**  *Massachusetts*, *Nova Scotia*, *Scotland*, or another appropriate first-level administrative division.

### Tagging Examples:
`<addressRegion>Scotland</addressRegion>`

`<addressRegion>The Himalaya Mountains</addressRegion>`
 
## Sub-Element: addressLocality
 
**Element tag** `<addressLocality>`
 
**Description** The locality in which the street address is, and which is in the region. 
 
**Optional**

**Data values:**  Boston, for example.

### Tagging Examples:
`<addressLocality>Inverness</addressLocality>`

`<addressLocality>Menlunq Tsu Glacier</addressLocality>`

## Sub-Element: postalCode

**Element tag** `<postalCode>`

**Description** The postal code. 

**Optional**

**Data values:**  For example, 02115

### Tagging Examples:
`<postalCode>101000</postalCode>`

`<postalCode>78213</postalCode>`

`<postalCode>R3C 0V8</postalCode>`

## Sub-Element: streetAddress

**Element tag** `<streetAddress>`

**Description** The street address. 

**Optional**

**Data values:**  For example, 300 Fenway

### Tagging Examples:
`<streetAddress>улица Крымский Вал, 9</streetAddress>`

`<streetAddress>1600 Pennsylvania Avenue</streetAddress>`