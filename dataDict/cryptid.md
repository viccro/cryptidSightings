# Element: cryptid

**Description:** An object identifying and describing a cryptid.

## Sub-element: cryptidCanonicalName
**Element tag:** `<cryptidCanonicalName>`

**Description:** The name of the cryptid as standardized by an external body, such as [wikiLC](https://en.wikipedia.org/wiki/List_of_cryptids), LOC, or the Encyclopaedia of Cryptozoology online.

**Attributes:** *termSource, termSourceId*

**Non-Repeatable, Required**

**Data values:**  Controlled. Recommended: taken from the [wikipedia List of Cryptids](https://en.wikipedia.org/wiki/List_of_cryptids).

**Recommended values for *termSource*:** *AAT*, *[wikiLC](https://en.wikipedia.org/wiki/List_of_cryptids)*. *[wikiLLC](https://en.wikipedia.org/wiki/Lists_of_legendary_creatures)*, *[fandomWikiLC](https://cryptidz.fandom.com/wiki/List_of_Cryptids)*. See reference index for full list.

**Recommended values for *termSourceID*:** URL or URI linking to the termsource

## Sub-element: cryptidAlternativeName

**Element tag:** `<cryptidAlternativeName>`

**Description:** Any alternative name used to refer to the type of creature or individual creature observed, especially one used by the observer

**Repeatable, Optional** 

## Sub-element: cryptidDescription
**Element tag:** `<cryptidDescription>`

**Description:** A description of the cryptid, as reported in this account, as told by the listed observer(s). This may include dimensions, colors, mode of locomotion, and other biological details.

**Repeatable, Optional** 

**Data values:** May include quotes or paraphrased description, as consistent with the parent account of the sighting


## Tagging examples
```
<cryptidSeen>
    <cryptidCanonicalName cs:termSource="LOC" cs:termSourceID="sh85117619">Sasquatch</cryptidCanonicalName>
    <cryptidAlternativeName>Bigfoot</cryptidAlternativeName>
    <cryptidDescription>"It does not look like a person. It's arms are way too big; it's hands. Look at its hands, its hands hang down to its knees at least."</cryptidDescription>
</cryptidSeen>
```

```
    <cryptidSeen>
        <cryptidCanonicalName cs:termSource="wikiLLC" cs:termSourceID="https://en.wikipedia.org/wiki/Loveland_frog">Loveland frog</cryptidCanonicalName>
        <cryptidAlternativeName>Loveland frogman</cryptidAlternativeName>
        <cryptidAlternativeName>Loveland lizardman</cryptidAlternativeName>
        <cryptidDescription>Bipedal, four-foot tall frog. Amphibious </cryptidDescription>
    </cs:cryptidSeen>      
```
