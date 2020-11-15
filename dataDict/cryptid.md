# Element: cryptid

**Description:** An object identifying and describing a cryptid.

**Repeatable, Required** 

## Sub-element: cryptidCanonicalName
**Element tag:** `<cs:cryptidCanonicalName>`

**Description:** The name of the cryptid as standardized by an external body, such as LOC or the Encyclopaedia of Cryptozoology online.

**Attributes:** *termSource, termSourceId*

**Non-Repeatable, Required**

**Data values:**  Controlled. Recommended: taken from the wikipedia List of Cryptids.

**Recommended values for *termSource*:** *AAT*, *wikiLC*

**Recommended values for *termSourceID*:** AAT number, Name listed in chart from wikipedia List of Cryptids

## Sub-element: cryptidAlternativeName
**Element tag:** `<cs:cryptidAlternativeName>`

**Description:** Any alternative name used to refer to the type of creature or individual creature observed

**Repeatable, Optional** 

## Sub-element: cryptidDescription
**Element tag:** `<cs:cryptidDescription>`

**Description:** A description of the cryptid, as reported in this account, as told by the listed observer(s). This may include dimensions, colors, mode of locomotion, and other biological details.

**Repeatable, Optional** 

**Data values:** May include quotes or paraphrased description, as consistent with the parent account of the sighting


## Tagging examples
```
<cryptidSeen>
    <cryptidCanonicalName cs:termSource="LOC" cs:termSourceID="sh85117619">Sasquatch</cryptidCanonicalName>
    <cryptidAlternativeName>Bigfoot</cryptidAlternativeName>
    <cryptidDescription>"It does not look like a person. It's arms are way too big; it's hands. Look at its hands, its hands hang down to its knees at least."</cryptidDescription>
    <cryptidDescription>"His arms obviously hang below his knees"</cryptidDescription>
</cryptidSeen>
```

```
<cryptidSeen>
    <cryptidCanonicalName termSource="wikiLLC" termSourceId="https://en.wikipedia.org/wiki/Loveland_frog">Loveland frog</cryptidCanonicalName>
    <cryptidAlternativeName>Loveland frog</cryptidAlternativeName>
    <cryptidAlternativeName>Loveland lizard</cryptidAlternativeName>
</cryptidSeen>        
```
