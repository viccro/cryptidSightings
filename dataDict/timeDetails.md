## Element: timeDetails

**Element tag** <timeDetails>

**Description** An object describing an exact or approximate time. This type allows one and only one of exactTime, approximateTime, or unknownTime.

## Sub-Element: exactTime

**Element tag** `<exactTime>`

**Type** `xs:time`

**Description** Use if an exact time is known for the sighting.

**Optional**

**Data values:** A time of the sighting in xml standard, 24 hour time with as much precision as possible: hh:mm:ss.s. If time zone is known, use time offsets from UTC as in ISO 8601, eg 03:45:30+05

### Tagging Examples:
```
<exactTime>17:56:02Z</exactTime>
```
```
<exactTime>22:10-05</exactTime>
```

## Sub-Element: approximateTime

**Element tag** `<approximateTime>`

**Description** Use if a range of possible times are known. 

**Optional**

**Data values:** Possible entries include "morning", "after 10pm", and "between 3pm and 4:30pm". The term "day" refers to all light hours, dawn to dusk. The term "night" refers to all dark hours, dusk to dawn. Photographic and video evidence taken during the day or night can be used to determine these approximate times.

### Tagging Examples:
```
<approximateTime>dawn</approximateTime>
```

```
<approximateTime>between 8pm and 9:15pm</approximateTime>
```

## Sub-Element: unknownTime

**Element tag** `<unknownTime>`

**Type** `xs:boolean`

**Description** If no details at all are given about the time, set unknownTime to `true`. This is strongly discouraged, but preferred to leaving the time field empty.

**Optional**

**Data values:** Only use `true`. Rather than set this field to `false` for a known time, set one of the other two fields within `<timeDetails>` with more details.

### Tagging Example:
```
<unknownTime>true</unknownTime>
```