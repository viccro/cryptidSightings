# Element: postalAddress

**Element tag** `<postalAddress>`

**Description** An object describing a geographic location using postal code standards


## Sub-Element: addressCountry

**Element tag** `<addressCountry>`

**Description** The country component of the location.
 
**Optional**

**Data values:**  Use the two-letter ISO 3166-1 alpha-2 country code.
 

## Sub-Element: addressRegion

**Element tag** `<addressRegion>`

**Description** The region in which the locality is, and which is in the country. 

**Optional**

**Data values:**  *Massachusetts*, *Nova Scotia*, *Scotland*, or another appropriate first-level administrative division.

 
## Sub-Element: addressLocality
 
**Element tag** `<addressLocality>`
 
**Description** The locality in which the street address is, and which is in the region. 
 
**Optional**

**Data values:**  Boston, for example.


## Sub-Element: postalCode

**Element tag** `<postalCode>`

**Description** The postal code. 

**Optional**

**Data values:**  For example, 02115


## Sub-Element: streetAddress

**Element tag** `<streetAddress>`

**Description** The street address. 

**Optional**

**Data values:**  For example, 300 Fenway

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