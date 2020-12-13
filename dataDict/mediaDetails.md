# Element: mediaDetails

**Description:** Administrative and descriptive details about the media object. When the media object is a child of mentionedEvidence, the media object may or may not reference a cryptid sighting.
 
## Sub-element: mediaIdentifier

**Description:** A single URL, URI, ISBN, or other identifier for the media.

**Non-repeatable, Required**

**Element tag:** `<mediaIdentifier>`

**Data values:**  Uncontrolled. Free text description. Recommended use of permalinks for URL/URI addresses.

**Attributes:** *type*

**Recommended data values for *type*:** The type of identifier listed: `URI`, `URL`, `ISBN`, etc. Getty AAT term preferred. 

### Tagging Examples:
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

### Tagging Examples:
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

### Tagging Examples:
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

### Tagging Examples:
`<mediaAffiliation  cs:termSource="LCNAF" cs:termSourceID="nr 89013909">Encyclopaedia Britannica</mediaAffiliation>`

`<mediaAffiliation cs:termSource="none" cs:termSourceID="none">Odd Encounters</mediaAffiliation>`

## Sub-element: [mediaPublicationDate](date.md)

**Description:** The publication date of the media, such as the copyright date of a book, or the date a blog was posted 

**Optional**

**Element tag:** `<mediaPublicationDate>`

**Element type:** [Date](date.md)

**Data values:** Refer to **Element: Date** for use description of exactDate, approximateDate, and unknownDate options
 
### Tagging Examples:
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

### Tagging Examples:
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
 
### Tagging Examples:
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
