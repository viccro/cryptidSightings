## Element: time

**Element tag** `<time>`

**Description** An object describing an exact or approximate time. This type allows one and only one of exactTime, approximateTime, or unknownTime.

## Sub-Element: [timeDetails](timeDetails.md)

**Element tag** `<timeDetails>`

**Description** The time a notable event took place during the sighting

**Required**

**Data values:** [timeDetails](timeDetails.md)


## Sub-Element: timeType

**Element tag** `<timeType>`

**Description** A description of the time noted, 

**Optional**

**Data values:** Possible values include "cryptid first seen", "cryptid submerged", or "cryptid no longer visible"

### Tagging Examples:
```
<sightingTime>
    <timeDetails>
        <exactTime>19:07:33+05</exactTime>
    </timeDetails>
    <timeType>cell phone video begins</timeType>
</sightingTime>
```

```
<sightingTime>
    <timeDetails>
        <approximateTime>day</approximateTime>
    </timeDetails>
    <timeType>cryptid walked along ridge</timeType>
</sightingTime>
```

```
<sightingTime>
    <timeDetails>
        <unknownTime>true</unknownTime>
    </timeDetails>
    <timeType>cryptid rocked the boat</timeType>
</sightingTime>
```