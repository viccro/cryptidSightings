# Cryptid Media schema

Cryptid Media Schema (Version 1.0) was created as a final project for LIS 445: Metadata at Simmons 
University, in the School of Library and Information Science (SLIS). The schema was created by:
* Tish Albro
* Stephanie Bennett
* Vicki Crosson
* Alex Werbizky Ehrhardt

This version of the schema will be documented at www.github.com/viccro/cryptidSightings/tree/main/dataDict/
The latest version of the schema may be downloaded [at this link](https://raw.githubusercontent.com/viccro/cryptidSightings/main/cryptid-media-1.0.xsd).

The Cryptid Sightings Schema will be used to document any sighting of a cryptid (any animal whose 
existence is unsubstantiated). 

The schema makes use of a lot of structures found in CDWAlite, especially with regards to attributes.

## Schema Structure

* [cryptidMedia](cryptidMedia.md)
    * [mediaDetails](mediaDetails.md)
        * [mediaIdentifier](cryptidMedia.md#sub-element-mediaIdentifier)
        * [mediaName](cryptidMedia.md#sub-element-medianame)
        * [mediaType](cryptidMedia.md#sub-element-mediatype)
        * [mediaAffiliation](cryptidMedia.md#sub-element-mediaaffiliation)
        * [mediaPublicationDate](date.md)
        * [mediaDimensions](cryptidMedia.md#sub-element-mediaDimensions)
        * [mediaDescription](cryptidMedia.md#sub-element-mediadescription)

    * [accountOfSighting](account.md)
        * [observer](account.md#sub-element-observer)
        * [cryptidSeen](account.md#sub-element-cryptidseen)
            * [cryptidCanonicalName](cryptid.md#sub-element-cryptidcanonicalname)
            * [cryptidAlternativeName](account.md#sub-element-cryptidalternativename)
            * [cryptidDescription](account.md#sub-element-cryptiddescription)
        * [sightingDate](date.md)
            * [exactDate](date.md#sub-element-exactdate)
            * [approximateDate](date.md#sub-element-approximatedate)
            * [unknownDate](date.md#sub-element-unknowndate)
        * [sightingTime](time.md)
            * [timeDetails](timeDetails.md)
                * [exactTime](timeDetails.md#sub-element-exacttime)
                * [approximateTime](timeDetails.md#sub-element-approximatetime)
                * [unknownTime](time.md#sub-element-unknowntime)
            * [timeType](time.md#sub-element-timetype)
        * [sightingLocation](location.md)
            * [continent](location.md#sub-element-continent)
            * [geoCoordinates](location.md#sub-element-geocoordinates)
                * [longitude](coordinates.md#sub-element-longitude)
                * [latitude](coordinates.md#sub-element-latitude)
            * [postalAddress](postalAddress.md)
                * [addressCountry](postalAddress.md#sub-element-addresscountry)
                * [addressRegion](postalAddress.md#sub-element-addressregion)
                * [addressLocality](postalAddress.md#sub-element-addresslocality)
                * [postalCode](postalAddress.md#sub-element-postalCode)
                * [streetAddress](postalAddress.md#sub-element-streetaddress)
            * [unknownLocation](location.md#sub-element-unknownlocation)
            * [locationDescription](location.md#sub-element-locationdescription)
        * [descriptionOfAccount](account.md#sub-element-descriptionofaccount)

    * [mentionedEvidence](cryptidMedia.md#sub-element-mentionedevidence)
        * [evidenceAffirmative](evidence.md)
            * [evidenceAgent](evidence.md#sub-element-evidenceagent)
            * [evidenceType](evidence.md#sub-element-evidencetype)
            * [mediaEvidence](mediaDetails.md)
            * [mediaIdentifier](cryptidMedia.md#sub-element-mediaIdentifier)
                * [mediaName](cryptidMedia.md#sub-element-medianame)
                * [mediaType](cryptidMedia.md#sub-element-mediatype)
                * [mediaAffiliation](cryptidMedia.md#sub-element-mediaaffiliation)
                * [mediaPublicationDate](cryptidMedia.md#sub-element-mediapublicationdate)
                * [mediaDimensions](cryptidMedia.md#sub-element-mediaDimensions)
                * [mediaDescription](cryptidMedia.md#sub-element-mediadescription)
            * [evidenceDescription](evidence.md#sub-element-evidenceAgent)
        * [evidenceNegative](evidence.md)
            * [evidenceAgent](evidence.md#sub-element-evidenceagent)
            * [evidenceType](evidence.md#sub-element-evidencetype)
            * [mediaEvidence](mediaDetails.md)
            * [mediaIdentifier](cryptidMedia.md#sub-element-mediaIdentifier)
                * [mediaName](cryptidMedia.md#sub-element-medianame)
                * [mediaType](cryptidMedia.md#sub-element-mediatype)
                * [mediaAffiliation](cryptidMedia.md#sub-element-mediaaffiliation)
                * [mediaPublicationDate](cryptidMedia.md#sub-element-mediapublicationdate)
                * [mediaDimensions](cryptidMedia.md#sub-element-mediaDimensions)
                * [mediaDescription](cryptidMedia.md#sub-element-mediadescription)
            * [evidenceDescription](evidence.md#sub-element-evidenceAgent)

## Change log:
* v0.2: 
    * cryptid contains xs:choice, not xs:all
    * moved mediaSource (prev media) inside of accountOfSighting (prev reportOfSighting)
    * canonicalName termsource and termsourceID moved to attributes
    * offer exact and approx times, and type of time to qualify ranges
        * require mediaName
    * fleshed out docstrings for each field

* v0.3: Corrections made after filling out Category A corpus
    * descriptionOfReport renamed to descriptionOfAccount
    * personWhoSaysThis renamed to evidenceAgent
    * mediaLanguage added with type attribute
    * attributes added to mediaDimensions
    * person fields have type attribute to identify "individual" or "group"
    * choices and alls have been changed to sequences where applicable
    
* v0.4: Changed from cryptid-sightings schema to cryptid-media schema
    * root element is now mediaSource
    * exactTime>date corrected to exactTime>time
    * rearranged objects to be in the order that they're used
    * restructured time to allow for description of what the timestamp is describing
    
* v0.5 - v0.7: Changes reflect global copy edits from checking against the reality of the .xsd functions in practice, reflect decisions from discussions, and Stephanie's edit notes on her practice v0.4 xml records.
    * Created a googleDoc table of resources we reference in the data dictionary
    * Created the global attribute "lang" and assigned a CV of LOC
    * Updates to to the following sections:
       * cryptid.md
         * update cryptidCannonicalName description, values for termSource, and termSourceID
       * cryptidMedia.md
         * described cryptedMedia as the root element
       * date.md
         * updated unknownDate description for clarity
       * evidence.md
         * updated sub-elements to "non-repeatable" as they are coded in the .xsd. The evidenceAffirmative and evidenceNegative wrappers are repeatable, but the evidence sub-elements within those wrappers are non-repeatable. 
       * location.md
       * mediaDetails
         * updated descriptions
         * updated descriptions as necessary
         * updated mediaLanguage with a link to the new arrtibute "lang" 
         * added attribute "supplied" fixed value "yes" to mediaName element ONLY
         * mediaName is now required and repeatable
         * mediaName now has limited attributes		
         * mediaType is now required and repeatable
         * mediaType now has limited attributes		
         * mediaAffiliation now has limited attributes
         * prohibited attributes in mediaDescription
         * mediaDimensions calls out "word count" and "page count" as a recommended terms
       * mentionedEvidence
         * updated annotation descriptions
         * added element evidenceClassification with restricted attribute values. created use description
         * prohibited attributes in evidenceDescription
       * timeDetails
         * defined terms "day" and "night"
    
* v1.0 Minor edits made to align xsd with data dictionary
    * Prefer 'None' to domain or empty for uncontrolled mediaAffiliations
    * Remove lang attribute from mediaLanguage
    * Add termSource attribute to mediaLanguage, to specify CV used
    * Removed lang attribute from cryptidDescription
    * Made continent an enum
    * Attributes now required
    * evidenceType repeated
    * mediaIdentifier required
    * set supplied attribute to true and false, rather than yes/no
    * cryptidDescription optional
    * mediaEvidence optional

# Element: cryptidMedia

**Description:** Root element. A media object relating the account(s) of a cryptid sighting, such as those published in a newspaper article, book, or blog post

**Element tag:** `<mediaEvidence>`


## Sub-element: [mediaDetails](mediaDetails.md)

**Description:** Administrative and descriptive details about the media object that describes a cryptid sighting

**Non-repeatable, Required**

**Element tag:** `<mediaDetails>`

**Tagging Example**
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

**Tagging Example**
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

**Tagging Example**
```
<mentionedEvidence>
<evidenceAffirmative>
    <evidenceAgent  cs:termSource="none" cs:termSourceID="none">Robert Kenneth Wilson</evidenceAgent>
    <evidenceClassification>physical</evidenceClassification>
    <evidenceType  cs:termSource="AAT" cs:termSourceID="300046300">photograph</evidenceType>
    <mediaEvidence>
        <mediaIdentifier  cs:type="URL">https://www.britannica.com/topic/Loch-Ness-monster-legendary-creature</mediaIdentifier>
        <mediaName  cs:termSource="none" cs:termSourceID="none">Loch Ness monster: legendary creature</mediaName>
        <mediaType  cs:termSource="AAT" cs:termSourceID="300046300">photograph</mediaType>
        <mediaAffiliation  cs:termSource="none" cs:termSourceID="none">Britannica</mediaAffiliation>
        <mediaPublicationDate>
            <exactDate>2020-05-04</exactDate>
        </mediaPublicationDate>
        <mediaDimensions  cs:unit="pixels" cs:type="height">450</mediaDimensions>
        <mediaDimensions  cs:unit="pixels" cs:type="width">662</mediaDimensions>
        <mediaDescription>The digitized version of the photograph orignally taken in 1934 by Robert Kenneth Wilson</mediaDescription>
        <mediaLanguage  cs:termSource="ISO 639-2b" cs:type="current">eng</mediaLanguage>
    </mediaEvidence>
    <evidenceDescription>The Surgeon's Photograph of what Robert Kenneth Wilson saw in 1934</evidenceDescription>
</evidenceAffirmative>
<evidenceNegative>
    <evidenceAgent  cs:termSource="none" cs:termSourceID="none">Marmaduke Wetherell</evidenceAgent>
    <evidenceClassification>testimonial</evidenceClassification>
    <evidenceType  cs:termSource="AAT" cs:termSourceID="300026392">interview</evidenceType>
    <mediaEvidence>
        <mediaIdentifier  cs:type="URL">https://www.britannica.com/topic/Loch-Ness-monster-legendary-creature</mediaIdentifier>
        <mediaName  cs:termSource="none" cs:termSourceID="none">Loch Ness monster: legendary creature</mediaName>
        <mediaType  cs:termSource="AAT" cs:termSourceID="300048715">article</mediaType>
        <mediaAffiliation  cs:termSource="LCNAF" cs:termSourceID="nr 89013909">Encyclopaedia Britannica</mediaAffiliation>
        <mediaPublicationDate>
            <exactDate>2020-05-04</exactDate>
        </mediaPublicationDate>
        <mediaDimensions  cs:unit="word count" cs:type="words">512</mediaDimensions>
        <mediaDescription></mediaDescription>
        <mediaLanguage  cs:termSource="ISO 639-2b" cs:type="current">eng</mediaLanguage>
    </mediaEvidence>
    <evidenceDescription>The creature captured in the photograph is a creation by Marmaduke Wetherell, created by combining different children's toys.</evidenceDescription>
</evidenceNegative>
</mentionedEvidence>
```        

# Element: mediaDetails

**Description:** Administrative and descriptive details about the media object. When the media object is a child of mentionedEvidence, the media object may or may not reference a cryptid sighting.
 
## Sub-element: mediaIdentifier

**Description:** A single URL, URI, ISBN, or other identifier for the media.

**Non-repeatable, Required**

**Element tag:** `<mediaIdentifier>`

**Data values:**  Uncontrolled. Free text description. Recommended use of permalinks for URL/URI addresses.

**Attributes:** *type*

**Recommended data values for *type*:** The type of identifier listed: `URI`, `URL`, `ISBN`, etc. Getty AAT term preferred. 

**Tagging Examples**
`<mediaIdentifier cs:type="URL">http://www.oddencounters.com/creatures/Marble-Mountain-Bigfoot-Video.html</mediaIdentifier>`

`<mediaIdentifier  cs:type="URL">https://www.britannica.com/topic/Loch-Ness-monster-legendary-creature</mediaIdentifier>`

## Sub-element: mediaName

**Description:** A name identifying the piece of media, such as a fixed title 

**Repeatable, Required**

**Element tag:** `<mediaName>`

**Data values:**  Use a name that originally referred to the piece of media if possible, or a name that is commonly used to refer to the media. If none is known, use a unique phrase that identifies the cryptidMedia by type, contents, and/or creators. If more than one name is known, repeat the mediaName set.

**Attributes:** *supplied*, *termsSource*, *termSourceId*

**Fixed data values for *supplied*:** If the mediaName was created during the creation of the record, set this attribute to `true`. If the title was fixed before the creation of the cryptidMedia record, set it to `false`.

**Recommended values for *termSource*:** Reference the source of the name used, such as LOC for Library of Congress. If no control was use, enter `none`.

**Recommended values for *termSourceID*:** Reference the unique identifier of the term used, if present, such as the Library of Congress identifier number. If no control was use, enter `none`.

**Tagging Examples**
`<mediaName cs:termSource="none" cs:termSourceID="none">Loch Ness monster: legendary creature</mediaName>`

`<mediaName cs:termSource="none" cs:termSourceID="none" supplied="false">Marble Mountain Bigfoot Video</mediaName>`

## Sub-element: mediaType

**Description:** Used to describe the type of content of the media: `digital photograph`, `digital moving image formats`, `article`, `book`, etc. 

**Repeatable, Required**

**Element tag:** `<mediaType>`

**Attributes:** *termSource, termSourceId*

**Data values:** Use to describe the media format type: digital photograph, motion picture film, article, book, etc. If a media object contains more than one format type, mediaType may be repeated. Recommended data value term source from Getty AAT. If the type of media cannot be determined, enter the value "undefined". 

**Recommended values for *termSource*:** `AAT`, `none` 

**Recommended values for *termSourceID*:** AAT number, `none`

**Tagging Examples**
`<mediaType cs:termSource="AAT" cs:termSourceID="300312050">Digital moving image formats</mediaType>`

`<mediaType  cs:termSource="AAT" cs:termSourceID="300048715">article</mediaType>`
 
## Sub-element: mediaAffiliation

**Description:** If the media was published in association with a collection, newspaper, a media outlet, blog, social media platform, etc., list that affiliation here.

**Optional**

**Element tag:** `<mediaAffiliation>`

**Data values:**  Use Library of Congress Name Authority File if possible. If an unlisted website, list the name of the site here, (e.g., `Joe's Papers` for an article listed at www.joespapers.com/article/listed/at/this/path).

**Attributes:** *termsSource*, *termSourceId*

**Recommended values for *termSource*:** Reference the source of the name used, such as `LCNAF` for Library of Congress Name Authority. If no controlled source was used, enter `none`.

**Recommended values for *termSourceID*:** Reference the unique identifier of the term used, if present, such as the Library of Congress identifier number. If no controlled source was used, enter `none`.

**Tagging Examples**
`<mediaAffiliation  cs:termSource="LCNAF" cs:termSourceID="nr 89013909">Encyclopaedia Britannica</mediaAffiliation>`

`<mediaAffiliation cs:termSource="none" cs:termSourceID="none">Odd Encounters</mediaAffiliation>`

## Sub-element: [mediaPublicationDate](date.md)

**Description:** The publication date of the media, such as the copyright date of a book, or the date a blog was posted 

**Optional**

**Element tag:** `<mediaPublicationDate>`

**Element type:** [Date](date.md)

**Data values:** Refer to **Element: Date** for use description of exactDate, approximateDate, and unknownDate options
 
**Tagging Examples**
```
<mediaPublicationDate>
    <approximateDate>2011-2015</approximateDate>
</mediaPublicationDate>
```

```
<mediaPublicationDate>
    <exactDate>2020-05-04</exactDate>
</mediaPublicationDate>
```

## Sub-element: mediaDimensions

**Description:** Dimensions related to the media: word count, page count, size of book, seconds or frames of video, file size in bytes or pixels, etc. Do not include more than one dimension in each element; repeat mediaDimensions to add both height and width, for example.

**Repeatable, Optional**

**Element tag:** `<mediaDimensions>`

**Attributes:** *type, unit*

**Data values:**  Controlled. Recommended. CDWALite format where possible

**Data values for *unit*:** `cm`, `mm`, `m`, `g`, `kg`, `kb`, `Mb`, `Gb`, `px`, `words`, `pages`, and others as recommended in CCO and CDWA. 

**Data values for *type*:** `height`, `duration`, `length`, `word count` and others as recommended in CCO and CDWA. 

**Tagging Examples**
```
<mediaDimensions  cs:unit="pixels" cs:type="height">450</mediaDimensions>
<mediaDimensions  cs:unit="pixels" cs:type="width">662</mediaDimensions>
```

`<mediaDimensions cs:unit="s" cs:type="duration">417</mediaDimensions>`

## Sub-element: mediaDescription

**Description:** Used to describe the role and content of a piece of media.

**Required**

**Element tag:** `<mediaDescription>`

**Data values:**  Uncontrolled. Free text description of the media, prioritizing information that is not otherwise described in the schema.
 
**Tagging Examples**
`<mediaDescription>A video taken by John Mills during the Campus Life youth retreat. The video starts by exploring the lair of "some kinda creature", with a structured shelter of branches and debris "snapped by mighty mighty strength", with claw marks on surrounding trees. As the group explores the area, someone shouts out "He's walking down. Bigfoot's walking down right now," referring to a ridge in the distance. The camera zooms in to the figure on the ridge, watching him descend to a cluster of trees. When he gets to the trees, the figure begins pacing back and forth, before continuing his descent.</mediaDescription>`

`<mediaDescription>The digitized version of the photograph orignally taken in 1934 by Robert Kenneth Wilson</mediaDescription>`

`<mediaDescription>A history of sightings of the Loch Ness monster, including photographs, details of accounts, as well as debunking information.</mediaDescription>`

## Sub-element: mediaLanguage

**Description:** The main language of the piece of media

**Repeatable, Optional** 

**Element tag:** `<mediaLanguage>`

**Attributes:** *type*, *termSource*

**Data values:**  Controlled. Recommended. Language formulated according to rules in the CCO and CDWA (i.e., ISO 639-2b, RFC 3066, Language codes from Library of Congress language code for MARC, and other encoding schemes may be used, or another authoritative source may be used, such as Ethnologue: Languages of the World. 14th edition. Barbara F. Grimes, ed. Dallas, Texas: SIL International, 2000). If ISO or other codes are used, they must be translated into common English for end-users. 

**Recommended values for *type*:** `current`, `former`, `translated`, `local`, and others as recommended in CCO and CDWA. 

**Recommended values for *termSource*:** Identify the controlled vocabulary used to populate the language data value. For example: `ISO 639-2b` or `RFC 3066`.

## Tagging Examples:
`<mediaLanguage  cs:termSource="ISO 639-2b" cs:type="current">eng</mediaLanguage>`

```
<mediaLanguage  cs:termSource="ISO 639-2b" cs:type="former">jpn</mediaLanguage>
<mediaLanguage  cs:termSource="ISO 639-2b" cs:type="translated">tlh</mediaLanguage>
```

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

**Tagging Examples**
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

**Tagging Example**
```
<cryptidSeen>
    <cryptidCanonicalName cs:termSource="LOC" cs:termSourceID="sh85117619">Sasquatch</cryptidCanonicalName>
    <cryptidAlternativeName>Bigfoot</cryptidAlternativeName>
    <cryptidDescription>"It does not look like a person. It's arms are way too big; it's hands. Look at its hands, its hands hang down to its knees at least."</cryptidDescription>
</cryptidSeen>
```

## Sub-element: [sightingDate](date.md)
**Element tag:** `<sightingDate>`

**Description:** The date on which a sighting occurred. If the same cryptid was seen over multiple days, multiple sighting objects should be used to describe these discrete sightings.

**Required** 

**Data values:** [sightingDate](sightingDate.md)

**Tagging Examples**
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

**Description:** A time or set of times describing when a single sighting occurred. If the time of more than one event in the sighting is known, use multiple sightingTime blocks.

**Repeatable, Required** 

**Data values:** [time](time.md)

**Tagging Examples**
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

**Tagging Examples**
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

**Tagging Examples**
```
<descriptionOfAccount>Campus Life Youth Group, led by Jim Mills, found what appeared to be a shelter for something large. The shelter was described as being made of trees that were snapped by some massive force. Then, the group saw a strange figure walking along the ridgeline. Oddly proportioned, he stood taller than any man and was estimated to weight 700 pounds.</descriptionOfAccount>
```

```
<descriptionOfAccount>Robert Kenneth Wilson went to Loch Ness, Scotland in 1934 determined to gather evidence that the Loch Ness Monster existed. He saw a creature with a long neck and round head and managed to capture a photograph. This photograph is the most well-known and is known as the Surgeon's Photograph.</descriptionOfAccount>
```

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

**Tagging Examples**
`<cryptidCanonicalName  cs:termSource="LOC" cs:termSourceID="sh 85077967">Loch Ness Monster</cryptidCanonicalName>`

`<cryptidCanonicalName cs:termSource="wikiLC" cs:termSourceID="https://en.wikipedia.org/wiki/Mongolian_death_worm">Mongolian Death Worm</cryptidCanonicalName>`

## Sub-element: cryptidAlternativeName

**Element tag:** `<cryptidAlternativeName>`

**Description:** Any alternative name used to refer to the type of creature or individual creature observed, especially one used by the observer

**Repeatable, Optional** 

**Tagging Examples**
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

**Tagging Examples**
`<cryptidDescription>Hoofed creature, with "long thin legs and a long neck, with a dog-like head. It had wings and appeared to be stooping, as if about to jump." Observer could not identify "whether it had hair or feathers."</cryptidDescription>`

`<cryptidDescription>"It does not look like a person. It's arms are way too big; it's hands. Look at its hands, its hands hang down to its knees at least."</cryptidDescription>`

## Element: date

**Element tag** `<date>`

**Description** An object describing an exact or approximate date. This type allows one and only one of exactDate, approximateDate, or unknownDate.

## Sub-Element: exactDate

**Sub-element tag** `<exactDate>`

**Type** `xs:date`

**Description** Use if an exact date is known for the sighting.

**Optional**

**Non-repeatable**

**Data values:** Uses xml date format, ie. YYYY-MM-DD

**Tagging Example**
`<exactDate>1989-10-14</exactDate>`

## Sub-Element: approximateDate

**Element tag** `<approximateDate>`

**Description** Use if a range of possible dates are known. 

**Optional**

**Non-repeatable**

**Data values:** Free text description. Possible entries include "2020-11", "2001-10-29 or 2001-10-30", "Summer 1982", "1850-1857", or "The 1600s".

**Tagging Examples**
`<approximateDate>Fall 2020</approximateDate>`

`<approximateDate>day</approximateDate>`

`<approximateDate>1934</approximateDate>`

## Sub-Element: unknownDate

**Element tag** `<unknownDate>`

**Type** `xs:boolean`

**Description** If no details at all are given about the date, set unknownDate to `true`. This is strongly discouraged, but preferred to leaving the date field empty. Omit this element if the date is available.

**Optional**

**Non-repeatable**

**Data values:** Only use `true`. Rather than set this field to `false` for a known date, set one of the other two fields within `<date>` with more details.

**Tagging Examples**
`<unknownDate>true</unknownDate>`

## Element: time

**Element tag** `<time>`

**Description** An object describing an exact or approximate time. This type allows one and only one of exactTime, approximateTime, or unknownTime.


## Sub-Element: [timeDetails](timeDetails.md)

**Element tag** `<timeDetails>`

**Description** The time a notable event took place during the sighting

**Required**

**Non-repeatable**

**Data values:** [timeDetails](timeDetails.md)

**Tagging Examples**
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

**Tagging Examples**

`<timeType>Cryptid photographed</timeType>`

`<timeType>Cryptid emerged from water</timeType>`

`<timeType>Cryptid bumped the boat</timeType>`

## Element: timeDetails

**Element tag** <timeDetails>

**Description** An object describing an exact or approximate time. This type allows one and only one of exactTime, approximateTime, or unknownTime.

## Sub-Element: exactTime

**Element tag** `<exactTime>`

**Type** `xs:time`

**Description** Use if an exact time is known for the sighting.

**Optional**

**Data values:** A time of the sighting in xml standard, 24 hour time with as much precision as possible: hh:mm:ss.s. If time zone is known, use time offsets from UTC as in ISO 8601, eg 03:45:30+05

**Tagging Examples**
`<exactTime>17:56:02Z</exactTime>`

`<exactTime>22:10-05</exactTime>`

## Sub-Element: approximateTime

**Element tag** `<approximateTime>`

**Description** Use if a range of possible times are known. 

**Optional**

**Data values:** Possible entries include "morning", "after 10pm", and "between 3pm and 4:30pm". The term "day" refers to all light hours, dawn to dusk. The term "night" refers to all dark hours, dusk to dawn. Photographic and video evidence taken during the day or night can be used to determine these approximate times.

**Tagging Examples**
`<approximateTime>dawn</approximateTime>`

`<approximateTime>between 8pm and 9:15pm</approximateTime>`

## Sub-Element: unknownTime

**Element tag** `<unknownTime>`

**Type** `xs:boolean`

**Description** If no details at all are given about the time, set unknownTime to `true`. This is strongly discouraged, but preferred to leaving the time field empty.

**Optional**

**Data values:** Only use `true`. Rather than set this field to `false` for a known time, set one of the other two fields within `<timeDetails>` with more details.

**Tagging Example**
`<unknownTime>true</unknownTime>`

# Element: location

**Element tag** `<location>`

**Description** An object describing a geographic location. 


## Sub-Element: continent

**Element tag** `<continent>`

**Description** The two letter code describing the continent of the location.

**Non-repeatable, Required**

**Data values:** One of the two letter codes: *AF, NA, OC, AN, AS, EU, SA* or *AU*. (codes stand for Africa, North America, Oceania, Antarctica, Asia, Europe, South America, Australia)

**Tagging Examples**
`<continent>NA</continent>`

`<continent>OC</continent>`

## Sub-element: [geoCoordinates](coordinates.md)

**Element tag** `<geoCoordinates>`

**Description** An object describing a geographic location using the Geographic coordinate system.

**Non-repeatable, Optional**

**Data values:** [coordinates](coordinates.md)

**Tagging Examples**
```
<geoCoordinates>
    <longitude>-71.100082</longitude>
    <latitude>42.339199</latitude>
</geoCoordinates>
```

## Sub-Element: [postalAddress](postalAddress.md)

**Element tag** `<postalAddress>`

**Description** The location as specified by mailing address components. Complete as many fields as possible, even if the location is not at a specified street address location.

**Non-repeatable, Optional**

**Data values:** [postalAddress](postalAddress.md)

**Tagging Examples**
```
<postalAddress>
    <addressCountry>US</addressCountry>
    <addressRegion>California</addressRegion>
</postalAddress>
```

```
<postalAddress>
    <addressCountry>US</addressCountry>
    <addressRegion>Illinois</addressRegion>
    <addressLocality>Chicago</addressLocality>
    <postalCode>60613</postalCode>
    <streetAddress>1060 West Addison</streetAddress>
</postalAddress>
```

## Sub-Element: unknownLocation

**Element tag** `<unknownLocation>`

**Type:** `xs:boolean`

**Description** Only use `true`. Rather than set this field to `false` for a known location, set the other location fields with more details.

**Non-repeatable, Optional**

**Tagging Example**
`<unknownLocation>true</unknownLocation>`

## Sub-Element: locationDescription

**Element tag** `<locationDescription>`

**Description** A free text description of the location, prioritizing any details not described in other schema fields. 

**Non-repeatable, Optional**

**Tagging Examples**
`<locationDescription>20 miles from the nearest road, just below a ridgeline in a desolate area just north of Mt. Shasta. In the Marble Mountains.</locationDescription>`

`<locationDescription>Loch Ness, Scotland, is a freshwater loch that is located in the Scottish Highlands.</locationDescription>`

`<locationDescription>The Norwegian Sea is a marginal sea within the Arctic Ocean.</locationDescription>`

# Element: coordinates

**Element tag** `<coordinates>`

**Description** An object describing a geographic location using the Geographic coordinate system


## Sub-Element: longitude

**Element tag** `<longitude>`

**Type** `xs:decimal`

**Description** The longitude of a location. 

**Required**	

**Data values:**  Use decimal format, e.g. -122.08585

### Tagging Exapmle:
`<longitude>-71.100082</longitude>`


## Sub-Element: latitude

**Element tag** `<latitude>`

**Type** `xs:decimal`

**Description** The latitude of a location. 

**Required**

**Data values:**  Use decimal format, e.g. 37.42242

**Tagging Examples**
`<latitude>42.339199</latitude>`

# Element: postalAddress

**Element tag** `<postalAddress>`

**Description** An object describing a geographic location using postal code standards


## Sub-Element: addressCountry

**Element tag** `<addressCountry>`

**Description** The country component of the location.
 
**Optional**

**Data values:**  Use the two-letter ISO 3166-1 alpha-2 country code.

**Tagging Examples**
`<addressCountry>US</addressCountry>`

`<addressCountry>GB</addressCountry>`

`<addressCountry>NP</addressCountry>`

## Sub-Element: addressRegion

**Element tag** `<addressRegion>`

**Description** The region in which the locality is, and which is in the country. 

**Optional**

**Data values:**  *Massachusetts*, *Nova Scotia*, *Scotland*, or another appropriate first-level administrative division.

**Tagging Examples**
`<addressRegion>Scotland</addressRegion>`

`<addressRegion>The Himalaya Mountains</addressRegion>`
 
## Sub-Element: addressLocality
 
**Element tag** `<addressLocality>`
 
**Description** The locality in which the street address is, and which is in the region. 
 
**Optional**

**Data values:**  Boston, for example.

**Tagging Examples**
`<addressLocality>Inverness</addressLocality>`

`<addressLocality>Menlunq Tsu Glacier</addressLocality>`

## Sub-Element: postalCode

**Element tag** `<postalCode>`

**Description** The postal code. 

**Optional**

**Data values:**  For example, 02115

**Tagging Examples**
`<postalCode>101000</postalCode>`

`<postalCode>78213</postalCode>`

`<postalCode>R3C 0V8</postalCode>`

## Sub-Element: streetAddress

**Element tag** `<streetAddress>`

**Description** The street address. 

**Optional**

**Data values:**  For example, 300 Fenway

**Tagging Examples**
`<streetAddress>улица Крымский Вал, 9</streetAddress>`

`<streetAddress>1600 Pennsylvania Avenue</streetAddress>`

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

**Tagging Example**

```
<evidenceNegative>
    <evidenceAgent>Philip Morris</evidenceAgent>
    <evidenceClassification>demonstrative</evidenceClassification>
    <evidenceType>Rubber Ape Suit</evidenceType>
</evidenceNegative>
```

# Element: evidence

**Description:** An object describing a piece of evidence, for or against, related to the claim of the sighting
 
## Sub-element: evidenceAgent

**Element tag:** `<evidenceAgent>`

**Description:** The names, appellations, or other identifiers assigned to an individual, group of people, firm or other corporate body, or other entity that provided the piece of evidence. Use of a Name Authority is recommended. The name should be in natural order, if possible.  If there is no known creator, make a reference to the presumed culture or nationality of the unknown creator (e.g., use “Unknown Spanish woman” or “Unknown man” before "Unknown")

**Repeatable, Optional**

**Data values:**  Controlled. Recommended: Library of Congress Name Authority File

**Attributes:** *termSource*, *termSourceID*

**Recommended values for *termSource*:** A controlled vocabulary such as the Library of Congress Name Authority File. If not present in a CV, enter the type of source, such as "URL".

**Recommended values for *termSourceID*:** A controlled vocabulary identification number such as the Library of Congress Name Authority File. If not present in a CV, enter a unique identifier such as a URL address if available, or "none".

**Tagging Examples**

**Example: Blogger name "Matt K." from Blogger.com appears as such:** 
`<cs:evidenceAgent cs:termSource="Blogger" cs:termSourceID="https://www.blogger.com/profile/16529901596756078984">Matt K.</cs:evidenceAgent>`

**Example: The recorder of a sighting testimony name "Batchelor, John, 1854-1944" from LCNAF appears as such:**
`<cs:evidenceAgent cs:termSource="LCNAF" cs:termSourceId="85253806">Batchelor, John, 1854-1944</cs:evidenceAgent>`


## Sub-element: evidenceClassification

**Element tag:** `<evidenceClassification>`

**Description:** The legal category corresponding to the evidenceType presented. Limited to physical, testimonial, demonstrative, and documentary

**Non-repeatable, Optional**

**Data values:** Optional. Repeat the attribute value for display text.

**Attributes:** Controlled. Limited to physical, testimonial, demonstrative, and documentary

**Tagging Examples**
`<evidenceClassification>demonstrative</evidenceClassification>`

`<evidenceClassification>physical</evidenceClassification>`

## Sub-element: evidenceType

**Element tag:** `<evidenceType>`

**Description:** The type of thing that comprises the evidence, taken from the Stadardized local supplement list to the WFS report terms, the standard terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports controlled vocabularies, the Library of Congress Subject Headings, and/or Getty AAT as described in the Data Dictionary Evidence element appendix. Repeat `<evidenceType>` as many times as needed.

**Repeatable, Optional**

**Data values:**  Controlled. See appendix. Recommended: Local Evidence Dictionary Appendix or terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports Terms: ANSI/ASB Standard 019, Wildlife Forensics General Standards, First Edition, 2019 [http://www.asbstandardsboard.org/wp-content/uploads/2019/05/019_Std_e1.pdf]; ANSI/ASB Standard 028, Wildlife Forensics Morphology Standards, First Edition, 2019 [http://www.asbstandardsboard.org/wp-content/uploads/2019/05/028_Std_e1.pdf]; ANSI/ASB Standard 048, Wildlife Forensic DNA Standard Procedures, First Edition, 2019 [http://www.asbstandardsboard.org/wp-content/uploads/2019/05/048_Std_e1.pdf].

**Attributes:** *termSource*, *termSourceID*

**Recommended values for *termSource*:** See list of local acronyms. Recommended are: WFSGeneral, WFSMorphology, and WFSDNA. Use the term "local" if supplied by the record creator or localED if pulled from the local evidence dictionary appendix.

**Recommended values for *termSourceID*:** Use URI, URL, or other unique identifier where supplied by term source. If using local or localED term, use term value here, in addition to using it as value of element.

**Tagging Examples**
`<evidenceType cs:termSource="AAT" cs:termSourceID="300028682">Video recordings (physical artifacts)</evidenceType>`
`<evidenceType cs:termSource="localED" cs:termSourceID="Animal (whole)">Animal (whole)</evidenceType>`
 
## Sub-element: [mediaEvidence](mediaDetails.md)

**Element tag:** `<mediaEvidence>`

**Description:** Details about a media object that serves as evidence for or against a cryptid sighting. If the media itself gives details about a cryptid sighting, a whole cryptidMedia object should be created, and only the mediaIdentifier of that object should be included. If the object is an image or footage, which doesn't contain enough information to create a full cryptidMedia entry, fill out this details block in full.

**Optional**

**Data values:** [mediaDetails](mediaDetails.md)

### Tagging example:
```
<mediaEvidence>
    <mediaIdentifier cs:type="URL">https://youtu.be/eD8XSQbayXs</mediaIdentifier>
    <mediaName cs:termSource="none" cs:termSourceID="none">Marble Mountain Bigfoot Video</mediaName>
    <mediaType cs:termSource="AAT" cs:termSourceID="300312050">Digital moving image formats</mediaType>
    <mediaPublicationDate>
        <exactDate>2011-07-06</exactDate>
    </mediaPublicationDate>
    <mediaDimensions cs:type="duration" cs:unit="s">417</mediaDimensions>
    <mediaDescription>A video taken by John Mills during the Campus Life youth retreat. The video starts by exploring the lair of "some kinda creature", with a structured shelter of branches and debris "snapped by mighty mighty strength", with claw marks on surrounding trees. As the group explores the area, someone shouts out "He's walking down. Bigfoot's walking down right now," referring to a ridge in the distance. The camera zooms in to the figure on the ridge, watching him descend to a cluster of trees. When he gets to the trees, the figure begins pacing back and forth, before continuing his descent.</mediaDescription>
    <mediaLanguage  cs:termSource="ISO 639-2b" cs:type="current">eng</mediaLanguage>
</mediaEvidence>
```

## Sub-element: evidenceDescription

**Description:** Used to describe the role and content of a piece of evidence.

**Non-repeatable, Optional**

**Element tag:** `<evidenceDescription>`

**Data values:**  Uncontrolled. Free text description.

**Tagging Examples**
`<evidenceDescription>The creature captured in the photograph is a creation by Marmaduke Wetherell, created by combining different children's toys.</evidenceDescription>`

`<evidenceDescription>Eric Shipton's photograph of an alleged Yeti footprint, 13 inches in length, shows five toes, with an apparent 'big toe.'</evidenceDescription>`


# APPENDIX: Local Evidence Dictionary for Cryptid Sightings
description: Examples and supplementary type and term lists to the terms defined in the Wildlife Forensic Subcommittee Reports


## Evidence Classification
###	Physical
Objects that can be touched, like animal parts.

#### Recommended testimonial evidence terms: use the WFS reports, Stadardized local supplement list, and/or the Library of Congress Subject Headings for terms related to physical evidence.

#### Stadardized local supplement list to the WFS report terms: 
* Animal (whole)
* Animal (part)
* Fur
* Muscular
* Skin
* Skeletal
* Other
* Track (Single)
* Track (Trail)

#### Examples WFS report terms:
* Anthropogenic
* Casework samples
* Interspecific	
* Individual matching
* Taphonomy

#### Examples Library of Congress terms:
* Ear
* Blood
* Animal tracks
* Footprints, fossil
* Organs

###	Testimonial
Statements provided by either a layperson or expert witness.

#### Recommended testimonial evidence terms: use the Getty AAT and/or WFS reports for terms related to testimonial evidence.

#### Examples AAT terms:
* Interviews
* Discussions (events)
* Speeches (compositions)
* Testimonies

###	Demonstrative
Visual aids like photographs, video recordings, maps, diagrams, and casts of physical evidence.

#### Recommended demonstrative evidence terms: use the Getty AAT and/or WFS reports for terms related to demonstrative evidence.

### Examples AAT terms:
* Casts (sculpture)
* Forensic photographs
* Photographs
* Maps (documents)
* Historical maps
* Video recordings (physical artifacts)

### Examples WFS report terms:
* Anthropogenic
* Casework reference samples
* Reference materials
* Voucher specimen
* Curated collection


###	Documentary
a piece of written, printed, or electronic matter that provides information that serves as an official record. such as veterinary records, correspondence, and police logs.
#### Recommended documentary evidence terms: use the Getty AAT and/or WFS reports for terms related to documentary evidence. 

### Example AAT terms: 
* books
* correspondence
* damage reports
* diaries
* speeches (documents)

### Example WFS report terms:
* Taxonomic identification
* Chain of custody
* Technical review