# Element: mentionedEvidence

**Description:** Wrap used to contain affirmative evidence and or negative evidence mentioned in the media source, from media recordings to plaster casts, body parts or costume pieces. If no additional evidence is present, this element may be omitted.

**Optional**

**Non-repeatable**

**Element tag:** `<mentionedEvidence>`

## Sub-element: [evidenceAffirmative](evidence.md)

**Description:** Evidence provided to prove the claims of the observers. If multiple distinct pieces of evidence are present, repeat this element.

**Optional**

**Repeatable**

**Element tag:** `<evidenceAffirmative>`

**Data values:** [evidenceAffirmative](evidence.md)

### Tagging example:
```
<evidenceAffirmative>
    <evidenceAgent>Jim Mills</evidenceAgent>
    <evidenceClassification>demonstrative</evidenceClassification>
    <evidenceType>Video of creature</evidenceType>
    <mediaEvidence>
        <mediaIdentifier cs:type="URL">https://youtu.be/eD8XSQbayXs</mediaIdentifier>
        <mediaName>Marble Mountain Bigfoot Video</mediaName>
        <mediaType cs:termSource="AAT" cs:termSourceID="300312050">Digital moving image formats</mediaType>
        <mediaPublicationDate>
            <exactDate>2011-07-06</exactDate>
        </mediaPublicationDate>
        <mediaDimensions cs:type="duration" cs:unit="s">417</mediaDimensions>
        <mediaDescription>A video taken by John Mills during the Campus Life youth retreat. The video starts by exploring the lair of "some kinda creature", with a structured shelter of branches and debris "snapped by mighty mighty strength", with claw marks on surrounding trees. As the group explores the area, someone shouts out "He's walking down. Bigfoot's walking down right now," referring to a ridge in the distance. The camera zooms in to the figure on the ridge, watching him descend to a cluster of trees. When he gets to the trees, the figure begins pacing back and forth, before continuing his descent.</mediaDescription>
        <mediaLanguage cs:type="current">eng</mediaLanguage>
    </mediaEvidence>
</evidenceAffirmative>
```


## Sub-element: [evidenceNegative](evidence.md)

**Description:** Evidence provided to discredit the claims of the observers. If multiple distinct pieces of evidence are present, repeat this element.

**Optional**

**Repeatable**

**Element tag:** `<evidenceNegative>`

**Data values:** [evidenceNegative](evidence.md)

### Tagging Example:

```
<evidenceNegative>
    <evidenceAgent>Philip Morris</evidenceAgent>
    <evidenceClassification>demonstrative</evidenceClassification>
    <evidenceType>Rubber Ape Suit</evidenceType>
</evidenceNegative>
```