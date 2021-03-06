# Element: date

**Element tag** `<date>`

**Description** An object describing an exact or approximate date. This type allows one and only one of exactDate, approximateDate, or unknownDate.

## Sub-Element: exactDate

**Sub-element tag** `<exactDate>`

**Type** `xs:date`

**Description** Use if an exact date is known for the sighting.

**Optional**

**Non-repeatable**

**Data values:** Uses xml date format, ie. YYYY-MM-DD

### Tagging Example:
`<exactDate>1989-10-14</exactDate>`

## Sub-Element: approximateDate

**Element tag** `<approximateDate>`

**Description** Use if a range of possible dates are known. 

**Optional**

**Non-repeatable**

**Data values:** Free text description. Possible entries include "2020-11", "2001-10-29 or 2001-10-30", "Summer 1982", "1850-1857", or "The 1600s".

### Tagging Examples:
`<approximateDate>Fall 2020</approximateDate>`

`<approximateDate>day</approximateDate>`

`<approximateDate>1934</approximateDate>`

## Sub-Element: unknownDate

**Element tag** `<unknownDate>`

**Type** `xs:boolean`

**Description** If no details at all are given about the date, set unknownDate to `true`. This is strongly discouraged, but preferred to leaving the date field empty. Omit this element if the date is available.

**Optional**

**Non-repeatable**

**Data values:** Only use `true`. Rather than set this field to `false` for a known date, set one of the other two fields within `<date>` with more details.

### Tagging Examples:
`<unknownDate>true</unknownDate>`