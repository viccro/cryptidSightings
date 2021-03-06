# Element: account

**Required**

**Repeatable**

**Element tag** `<account>`

**Attributes:** No associated attributes

**Description** The consistent account of the encounter, given by a single observer or group of observers of the incident

## Sub-Element: observer
**Element tag:** `<observer>`

**Description:** The name of an individual observer or group of observers who stands by this account of the story.

**Attributes:** *type, groupMembership*

**Repeatable, Required**

**Data values:**  The names, appellations, or other identifiers assigned to an individual, group of people, firm or other corporate body, or other entity that observed the cryptid. Use of a Name Authority is recommended. The name should be in natural order, if possible.  If there is no known creator, make a reference to the presumed culture or nationality of the unknown creator (e.g., use “Unknown Spanish woman” or “Unknown man” before "Unknown")


**Recommended values for *type*:** The acceptable values are *individual* and *group*

**Recommended values for *groupMembership*:** If an individual is listed as part of a group, denote the name of the group with this attribute. For example, `Campus Life youth group`. If no group is listed, enter `none`.

### Tagging Examples:
```
<observer cs:type="individual" cs:groupMembership="Campus Life youth group">Jim Mills</observer>
<observer cs:type="group" cs:groupMembership="none">Campus Life youth group</observer>
```
```
<observer  cs:type="individual" cs:groupMembership="none">Robert Kenneth Wilson</observer>
```

## Sub-Element: [cryptidSeen](cryptid.md)

**Element tag:** `<cryptidSeen>`

**Description:** The cryptozoological creature being reported in this encounter

**Repeatable, Required**

**Data values:** [cryptid](cryptid.md)

### Tagging Example:
```
<cryptidSeen>
    <cryptidCanonicalName cs:termSource="LOC" cs:termSourceID="sh85117619">Sasquatch</cryptidCanonicalName>
    <cryptidAlternativeName>Bigfoot</cryptidAlternativeName>
    <cryptidDescription>"It does not look like a person. It's arms are way too big; it's hands. Look at its hands, its hands hang down to its knees at least."</cryptidDescription>
</cryptidSeen>
```

## Sub-element: [sightingDate](date.md)
**Element tag:** `<sightingDate>`

**Description:** The date on which a sighting occurred. If the same cryptid was seen over multiple days, multiple sightingDate objects should be used to describe these discrete sightings.

**Required** 

**Data values:** [sightingDate](sightingDate.md)

### Tagging Examples:
```
<sightingDate>
    <exactDate>1989-10-14</exactDate>
</sightingDate>
```

```
<sightingDate>
    <approximateDate>2001-06</approximateDate>
</sightingDate>
```

```
<sightingDate>
    <unknownDate>true</unknownDate>
</sightingDate>
```

## Sub-element: [sightingTime](time.md)
**Element tag:** `<sightingTime>`

**Description:** A time or set of times describing when a single sighting occurred. If the time of more than one event in the sighting is known, or if multiple sightings are described in the media, use multiple sightingTime objects. 

**Repeatable, Required** 

**Data values:** [time](time.md)

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

## Sub-element: [sightingLocation](location.md)
**Element tag:** `<sightingLocation>`

**Description:** The place that the cryptid was seen. If the sighting took place in multiple known locations, use multiple sightingLocation blocks.

**Repeatable, Required** 

**Data values:** [sightingLocation](sightingLocation.md)

### Tagging Examples:
```
<sightingLocation>
    <continent>AS</continent>
    <postalAddress>
        <addressCountry>NP</addressCountry>
        <addressLocality>Menlunq Tsu Glacier</addressLocality>
        <addressRegion>The Himalaya Mountains</addressRegion>
    </postalAddress>
    <locationDescription>Menlung Tsu Glacier, Menlung Basin, Gauri Sanka Range, Nepal, en route to Mount Everest.</locationDescription>
</sightingLocation>
```

## Sub-Element: descriptionOfAccount

**Element tag:** `<descriptionOfAccount>`

**Description:** A description of what happened, according to this consistent telling of the sighting, including any details that distinguish this account from others.

**Non-repeatable, Optional**

**Data values:** A description of what happened, according to this consistent telling of the sighting, including any details that distinguish this account from others. May include quotes or paraphrased description of the event. Do not use qualifier like "It appeared to" or "He claims that" unless the observers themselves used those words.

### Tagging Examples:
```
<descriptionOfAccount>Campus Life Youth Group, led by Jim Mills, found what appeared to be a shelter for something large. The shelter was described as being made of trees that were snapped by some massive force. Then, the group saw a strange figure walking along the ridgeline. Oddly proportioned, he stood taller than any man and was estimated to weight 700 pounds.</descriptionOfAccount>
```

```
<descriptionOfAccount>Robert Kenneth Wilson went to Loch Ness, Scotland in 1934 determined to gather evidence that the Loch Ness Monster existed. He saw a creature with a long neck and round head and managed to capture a photograph. This photograph is the most well-known and is known as the Surgeon's Photograph.</descriptionOfAccount>
```