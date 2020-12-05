##Element: timeDetails

**Element tag** <cs:timeDetails>

**Description** An object describing an exact or approximate time. This type allows one and only one of exactTime, approximateTime, or unknownTime.

##Sub-Element: exactTime

**Element tag** `<cs:exactTime>`

**Type** `xs:time`

**Description** Use if an exact time is known for the sighting.

**Optional**

**Data values:** A time of the sighting in xml standard, 24 hour time with as much precision as possible: hh:mm:ss.s. If time zone is known, use time offsets from UTC as in ISO 8601, eg 03:45:30+05


##Sub-Element: approximateTime

**Element tag** `<cs:approximateTime>`

**Description** Use if a range of possible times are known. 

**Optional**

**Data values:** Possible entries include "morning", "after 10pm", and "between 3pm and 4:30pm".


##Sub-Element: unknownTime

**Element tag** `<cs:unknownTime>`

**Type** `xs:boolean`

**Description** If no details at all are given about the time, set unknownTime to True. This is strongly discouraged, but preferred to leaving the time field empty.

**Optional**

**Data values:** Only use `True`. Rather than set this field to `False` for a known time, set one of the other two fields within `<cs:timeDetails>` with more details.