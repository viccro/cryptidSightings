# Element: mediaDetails

**Description:** Administrative and descriptive details about the media object. When the media object is a child of mentionedEvidence, the media object may or may not reference a cryptid sighting.
 
## Sub-element: mediaIdentifier

**Description:** A single URL, URI, ISBN, or other identifier for the media.

**Non-repeatable**

**Required**

**Element tag:** `<cs:mediaIdentifier>`

**Data values:**  Uncontrolled. Free text description. Recommended use of permalinks for URL/URI addresses.

**Attributes:** *type*

**Recommended data values for *type*:** The type of identifier listed: URI, URL, ISBN, etc. Getty AAT term preferred. 


## Sub-element: mediaName

**Description:** A name identifying the piece of media, such as a fixed title 

**Repeatable**

**Required**

**Element tag:** `<cs:mediaName>`

**Data values:**  Use a name that originally referred to the piece of media if possible, or a name that is commonly used to refer to the media. If none is known, use a unique phrase that identifies the cryptidMedia by type, contents, and/or creators. If more than one name is known, repeat the mediaName set.

**Attributes:** *supplied*, *termsSource*, *termSourceId*

**Fixed data values for *supplied*:** If the mediaName was created during the creation of the record, include the fixed attribute **supplied:"yes"**. If the title was fixed before the creation of the cryptidMedia record, omit this attribute. 

**Recommended values for *termSource*:** Reference the source of the name used, such as LOC for Library of Congress.

**Recommended values for *termSourceID*:** Reference the unique identifier of the term used, if present, such as the Library of Congress identifier number.


## Sub-element: mediaType

**Description:** Used to describe the type of content of the media: digital photograph, motion picture film, article, book, etc. 

**Repeatable**

**Required**

**Element tag:** `<cs:mediaType>`

**Attributes:** *termSource, termSourceId*

**Data values:** Use to describe the media format type: digital photograph, motion picture film, article, book, etc. If a media object contains more than one format type, mediaType may be repeated. Recommended data value term source from Getty AAT. If the type of media cannot be determined, enter the value "undefined". 

**Recommended values for *termSource*:** *AAT* 

**Recommended values for *termSourceID*:** AAT number

 
## Sub-element: mediaAffiliation

**Description:** If the media was published in association with a collection, newspaper, a media outlet, blog, social media platform, etc., list that affiliation here.

**Optional**

**Non-repeatable**

**Element tag:** `<cs:mediaAffiliation>`

**Data values:**  Use Library of Congress Name Authority File if possible. If an unlisted website, list the name of the site here, (e.g., Joe's Papers for an article listed at www.joespapers.com/article/listed/at/this/path).

**Attributes:** *termsSource*, *termSourceId*

**Recommended values for *termSource*:** Reference the source of the name used, such as LOC for Library of Congress.

**Recommended values for *termSourceID*:** Reference the unique identifier of the term used, if present, such as the Library of Congress identifier number. If not present in a CV, use a URL/URI if possible such as www.joespapers.com for an article listed on Joe's Papers.

 
## Sub-element: [mediaPublicationDate](date.md)

**Description:** The publication date of the media, such as the copyright date of a book, or the date a blog was posted 

**Optional**

**Non-repeatable**

**Element tag:** `<cs:mediaPublicationDate>`

**Element type:** [Date](date.md)

**Data values:** Refer to **Element: Date** for use description of exactDate, approximateDate, and unknownDate options
 
## Sub-element: mediaDimensions

**Description:** Dimensions related to the media: word count, page count, size of book, seconds or frames of video, file size in bytes or pixels, etc.

**Optional**

**Repeatable**

**Element tag:** `<cs:mediaDimensions>`

**Attributes:** *type, unit*

**Data values:**  Controlled. Recommended. CDWALite format where possible

**Data values for *unit*:** *cm, mm, m, g, kg, kb, Mb, Gb, px, word count, page count*, and others as recommended in CCO and CDWA. 

**Data values for *type*:** *height*, *duration*, and others as recommended in CCO and CDWA. 
 
## Sub-element: mediaDescription

**Description:** Used to describe the role and content of a piece of media.

**Required**

**Element tag:** `<cs:mediaDescription>`

**Data values:**  Uncontrolled. Free text description of the media, prioritizing information that is not otherwise described in the schema.
 
## Sub-element: mediaLanguage

**Description:** The main language of the piece of media

**Optional**

**Repeatable** 

**Element tag:** `<cs:mediaLanguage>`

**Attributes:** *type*, *lang*

**Data values:**  Controlled. Recommended. Language formulated according to rules in the CCO and CDWA (i.e., ISO 639-2b, RFC 3066 and other encoding schemes may be used, or another authoritative source may be used, such as Ethnologue: Languages of the World. 14th edition. Barbara F. Grimes, ed. Dallas, Texas: SIL International, 2000). If ISO or other codes are used, they must be translated into common English for end-users. 

**Recommended values for *lang*:** Language codes from Library of Congress language code for MARC. 

**Recommended values for *type*:** current, former, translated, local, and others as recommended in CCO and CDWA. 
