# Element: cryptid

**Description:** An object identifying and describing a cryptid.

## Sub-element: cryptidCanonicalName
**Element tag:** `<cryptidCanonicalName>`

**Description:** The name of the cryptid as standardized by an external body, such as [wikiLC](https://en.wikipedia.org/wiki/List_of_cryptids), LOC, or the Encyclopaedia of Cryptozoology online.

**Attributes:** *termSource, termSourceId*

**Non-Repeatable, Required**

**Data values:**  Controlled. Recommended: Library of Congress, the [wikipedia List of Cryptids](https://en.wikipedia.org/wiki/List_of_cryptids).

**Recommended values for *termSource*:** *LOC* *AAT*, *[wikiLC](https://en.wikipedia.org/wiki/List_of_cryptids)*. *[wikiLLC](https://en.wikipedia.org/wiki/Lists_of_legendary_creatures)*, *[fandomWikiLC](https://cryptidz.fandom.com/wiki/List_of_Cryptids)*. See reference index for full list.

**Recommended values for *termSourceID*:** LOC number, URL or URI found in the termsource

### Tagging Examples:
`<cryptidCanonicalName  cs:termSource="LOC" cs:termSourceID="sh 85077967">Loch Ness Monster</cryptidCanonicalName>`

`<cryptidCanonicalName cs:termSource="wikiLC" cs:termSourceID="https://en.wikipedia.org/wiki/Mongolian_death_worm">Mongolian Death Worm</cryptidCanonicalName>`

## Sub-element: cryptidAlternativeName

**Element tag:** `<cryptidAlternativeName>`

**Description:** Any alternative name used to refer to the type of creature or individual creature observed, especially one used by the observer

**Repeatable, Optional** 

### Tagging Examples:
```
<cryptidAlternativeName>Leed's Devil</cryptidAlternativeName>
<cryptidAlternativeName>Jabberwock</cryptidAlternativeName>
<cryptidAlternativeName>Wozzle Bug</cryptidAlternativeName>
```
```
<cryptidAlternativeName>Abominable Snowman</cryptidAlternativeName>
```

## Sub-element: cryptidDescription
**Element tag:** `<cryptidDescription>`

**Description:** A description of the cryptid, as reported in this account, as told by the listed observer(s). This may include dimensions, colors, mode of locomotion, and other biological details.

**Non-Repeatable, Optional** 

**Data values:** May include quotes or paraphrased description, as consistent with the parent account of the sighting

### Tagging Examples:
`<cryptidDescription>Hoofed creature, with "long thin legs and a long neck, with a dog-like head. It had wings and appeared to be stooping, as if about to jump." Observer could not identify "whether it had hair or feathers."</cryptidDescription>`

`<cryptidDescription>"It does not look like a person. It's arms are way too big; it's hands. Look at its hands, its hands hang down to its knees at least."</cryptidDescription>`