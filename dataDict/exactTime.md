##Element: exactTime
**Element tag** <cs:exactTime>
**Description** An object describing a media accounting of the sighting, as in a newspaper article or book

**Required**

##Sub-Element: date
**Element tag** <cs:date>
**Type** type=xs:time
**Description** A time of the sighting in xml standard, 24 hour time with as much precision as possible: hh:mm:ss.s. If time zone is known, use time offsets from UTC as in ISO 8601, eg 03:45:30+05

**Optional //I think?//**

##Sub-Element: qualifier
**Element tag** <cs:qualifier>
**Type** type=xs:string
**Description** A qualifier on the time: for example "disputed by critics"

**Optional**

##Sub-Element: typeOfTime
**Element tag** <cs:typeOfTime>
**Description** Possible values include "Start" and "End"

**Optional**

