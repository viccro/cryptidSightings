# Element: account

**Element tag** `<cs:account>`

**Description** The consistent account of the encounter, given by a single observer or group of observers of the incident

## Sub-Element: observer
**Element tag:** `<cs:observer>`

**Description:** The name of one of the observers who stands by this account of the story.

**Attributes:** *type, groupMembership*

**Repeatable, Required**

**Data values:**  The names, appellations, or other identifiers assigned to an individual, group of people, firm or other corporate body, or other entity that observed the cryptid. Use of a Name Authority is recommended. The name should be in natural order, if possible.  If there is no known creator, make a reference to the presumed culture or nationality of the unknown creator (e.g., use “Unknown Spanish woman” or “Unknown man” before "Unknown")


**Recommended values for *type*:** The acceptable values are *individual* and *group*

**Recommended values for *groupMembership*:** If an individual is listed as part of a group, denote the name of the group with this attribute. For example, *Campus Life youth group*.

## Sub-Element: [cryptidSeen](cryptid.md)

**Element tag:** `<cs:cryptidSeen>`

**Description:** The cryptozoological creature being reported in this encounter

**Repeatable, Required**

**Data values:** [cryptid](cryptid.md)


## Sub-element: [sightingDate](date.md)
**Element tag:** `<cs:sightingDate>`

**Description:** The date on which a sighting occurred. If the same cryptid was seen over multiple days, multiple sighting objects should be used to describe these discrete sightings.

**Required** 

**Data values:** [sightingDate](sightingDate.md)


## Sub-element: [sightingTime](time.md)
**Element tag:** `<cs:sightingTime>`

**Description:** A time or set of times describing when a single sighting occurred. If the time of more than one event in the sighting is known, use multiple sightingTime blocks.

**Repeatable, Required** 

**Data values:** [sightingTime](sightingTime.md)


## Sub-element: [sightingLocation](location.md)
**Element tag:** `<cs:sightingLocation>`

**Description:** The place that the cryptid was seen. If the sighting took place in multiple known locations, use multiple sightingLocation blocks.

**Repeatable, Required** 

**Data values:** [sightingLocation](sightingLocation.md)


## Sub-Element: descriptionOfAccount

**Element tag:** `<cs:descriptionOfAccount>`

**Description:** A description of what happened, according to this consistent telling of the sighting, including any details that distinguish this account from others.

**Non-repeatable, Optional**

**Data values:** A description of what happened, according to this consistent telling of the sighting, including any details that distinguish this account from others. May include quotes or paraphrased description of the event. Do not use qualifier like "It appeared to" or "He claims that" unless the observers themselves used those words.


