##Element: time
**Element tag** <cs:time>
**Description** An object describing an exact or approximate time or range of times

**Optional //I think//**

##Sub-Element: exactTime
**Element tag** <cs:exactTime>
**Type** type=xs:time
**Description** Use if an exact time is known for the sighting

**Required, Non-Repeatable**


##Sub-Element: approximateTime

**Element tag** <cs:approximateTime>

**Type** type=xs:string

**Description** Use if a range of times are known, or with the value 'unknown' if there is no way to narrow it down

**Required, Non-repeatable**


