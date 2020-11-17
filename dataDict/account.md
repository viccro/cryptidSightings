# Element: account

**Element tag** `<cs:account>`

**Description** The consistent account of the encounter, given by a single observer or group of observers of the incident

## Sub-Element: observer
**Element tag:** `<cs:observer>`

**Description:** The name of one of the observers who stands by this account of the story.

**Attributes:** *type*

**Repeatable, Required**

**Data values:**  The names, appellations, or other identifiers assigned to an individual, group of people, firm or other corporate body, or other entity that observed the cryptid. Use of a Name Authority is recommended. The name should be in natural order, if possible. For unknown observers, use the value *unknown*

**Recommended values for *type*:** The acceptable values are *individual* and *group*

## Sub-Element: cryptidSeen

**Element tag:** `<cs:cryptidSeen>`

**Description:** The cryptozoological creature being reported in this encounter

**Repeatable, Required**

**Data values:** [cryptid object](cryptid.md)


## Sub-Element: descriptionOfAccount

**Element tag:** `<cs:descriptionOfAccount>`

**Description:** A description of what happened, according to this consistent telling of the sighting, including any details that distinguish this account from others.

**Non-repeatable, Optional**

**Data values:** May include quotes or paraphrased description, as consistent with the parent account of the sighting

## Sub-Element: mediaSource

**Element tag:** `<cs:mediaSource>`

**Description:** An object describing a media accounting of the sighting, as in a newspaper article or book.

**Repeatable, Optional**

**Data values:** [media object](media.md)


