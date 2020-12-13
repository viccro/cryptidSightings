# Element: cryptidMedia

**Description:** Root element. A media object relating the account(s) of a cryptid sighting, such as those published in a newspaper article, book, or blog post

**Element tag:** `<mediaEvidence>`


## Sub-element: [mediaDetails](mediaDetails.md)

**Description:** Administrative and descriptive details about the media object that describes a cryptid sighting

**Non-repeatable, Required**

**Element tag:** `<mediaDetails>`

### Tagging Example:
```
<mediaDetails>
    <mediaIdentifier cs:type="URL">http://www.oddencounters.com/creatures/Marble-Mountain-Bigfoot-Video.html</mediaIdentifier>
    <mediaName cs:termSource="none" cs:termSourceID="none" supplied="false">Marble Mountain Bigfoot Video</mediaName>
    <mediaType cs:termSource="AAT" cs:termSourceID="300265431">Web sites</mediaType>
    <mediaAffiliation cs:termSource="none" cs:termSourceID="none">Odd Encounters</mediaAffiliation>
    <mediaPublicationDate>
        <approximateDate>2011-2015</approximateDate>
    </mediaPublicationDate>
    <mediaDimensions cs:type="word count" cs:unit="words">262</mediaDimensions>
    <mediaDescription>A blog post summarizing the Marble Mountain Bigfoot encounter and the Jim Mills video footage that stemmed from it.</mediaDescription>
    <mediaLanguage cs:termSource="ISO 639-2b" cs:type="current">eng</mediaLanguage>
</mediaDetails>
```

## Sub-element: [accountOfSighting](account.md)

**Description:** A consistent account of the sighting as described in this media source. Multiple observers may each disagree on details, resulting in multiple accounts per piece of media.

**Repeatable, Required**

**Element tag:** `<accountOfSighting>`

### Tagging Example:
```
<accountOfSighting>
    <observer cs:type="individual" cs:groupMembership="Campus Life youth group">Jim Mills</observer>
    <observer cs:type="group" cs:groupMembership="none">Campus Life youth group</observer>
    <cryptidSeen>
        <cryptidCanonicalName cs:termSource="LOC" cs:termSourceID="sh85117619">Sasquatch</cryptidCanonicalName>
        <cryptidAlternativeName>Bigfoot</cryptidAlternativeName>
        <cryptidDescription>"It does not look like a person. It's arms are way too big; it's hands. Look at its hands, its hands hang down to its knees at least."</cryptidDescription>
    </cryptidSeen>
    <sightingDate>
        <approximateDate>2001-06</approximateDate>
    </sightingDate>
    <sightingTime>
        <timeDetails>
            <approximateTime>day</approximateTime>
        </timeDetails>
        <timeType>video footage recorded</timeType>
    </sightingTime>
    <sightingLocation>
        <continent>NA</continent>
        <postalAddress>
            <addressCountry>US</addressCountry>
            <addressRegion>California</addressRegion>
        </postalAddress>
        <locationDescription>20 miles from the nearest road, just below a ridgeline in a desolate area just north of Mt. Shasta. In the Marble Mountains.</locationDescription>
    </sightingLocation>
    <descriptionOfAccount>Campus Life Youth Group, led by Jim Mills, found what appeared to be a shelter for something large. The shelter was described as being made of trees that were snapped by some massive force. Then, the group saw a strange figure walking along the ridgeline. Oddly proportioned, he stood taller than any man and was estimated to weight 700 pounds.</descriptionOfAccount>
</accountOfSighting>
```

## Sub-element: [mentionedEvidence](mentionedEvidence.md)

**Description:** Used to list evidence mentioned in the media source, from media recordings to plaster casts, body parts or costume pieces.

**Repeatable, Optional**

**Element tag:** `<mentionedEvidence>`
