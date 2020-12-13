## Element: time

**Element tag** `<time>`

**Description** An object describing an exact or approximate time. This type allows one and only one of exactTime, approximateTime, or unknownTime.


## Sub-Element: [timeDetails](timeDetails.md)

**Element tag** `<timeDetails>`

**Description** The time a notable event took place during the sighting

**Required**

**Non-repeatable**

**Data values:** [timeDetails](timeDetails.md)

### Tagging Examples:
```
<timeDetails>
    <exactTime>17:56:02+05</exactTime>
</timeDetails>
```

```
<timeDetails>
    <approximateTime>night</approximateTime>
</timeDetails>
```

```
<timeDetails>
    <unknownTime>true</unknownTime>
</timeDetails>
```

## Sub-Element: timeType

**Element tag** `<timeType>`

**Description** A description of the time noted, 

**Optional**

**Non-repeatable**

**Data values:** Possible values include "cryptid first seen", "cryptid submerged", or "cryptid no longer visible"

### Tagging Examples:

`<timeType>Cryptid photographed</timeType>`

`<timeType>Cryptid emerged from water</timeType>`

`<timeType>Cryptid bumped the boat</timeType>`