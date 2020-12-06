# Element: mediaDetails

**Description:** Administrative and descriptive details about the media object. When the media object is a child of mentionedEvidence, the media object may or may not reference a cryptid sighting.
 
## Sub-element: mediaIdentifier

**Description:** A single URL, URI, ISBN, or other identifier for the media.

**Non-repeatable**

**Required**

**Element tag:** `<cs:mediaIdentifier>`

**Data values:**  Uncontrolled. Free text description. Recommended use of permalinks for URL/URI addresses.

**Attributes:** *type*

**Recommended data values for *type*:** The type of identifier listed: URI, URL, ISBN, etc. AAT term preferred. 

## Sub-element: mediaName

**Description:** A name identifying the piece of media, such as a fixed title 

**Required**

**Element tag:** `<cs:mediaName>`

**Data values:**  Use a name that originally referred to the piece of media if possible, or a name that is commonly used to refer to the media. If none is known, use a unique phrase that identifies it by type, contents, and/or creators. 

## Sub-element: mediaType

**Description:** Used to describe the type of content of the media: digital photograph, motion picture film, article, book, etc. 

**Optional**

**Element tag:** `<cs:mediaType>`

**Attributes:** *termSource, termSourceId*

**Data values:**  Controlled. Recommended: Getty Art and Architecture Thesaurus 

**Recommended values for *termSource*:** *AAT* 

**Recommended values for *termSourceID*:** AAT number
 
## Sub-element: mediaAffiliation

**Description:** If the media was published in a collection, newspaper, etc, list that affiliation here.

**Optional**

**Element tag:** `<cs:mediaAffiliation>`

**Data values:**  Use Library of Congress Name Authority File if possible. If an unlisted website, list the name of the site here, (e.g., Joe's Papers for an article listed at www.joespapers.com/article/listed/at/this/path).
 
## Sub-element: [mediaPublicationDate](date.md)

**Description:** The publication date of the media, such as the copyright date of a book, or the date a blog was posted

**Optional**

**Element tag:** `<cs:mediaPublicationDate>`

**Element type:** [Date](date.md)
 
## Sub-element: mediaDimensions

**Description:** Dimensions related to the media: page count, size of book, seconds or frames of video, file size in bytes or pixels, etc.

**Repeatable, Optional**

**Element tag:** `<cs:mediaDimensions>`

**Attributes:** *type, unit*

**Data values:**  Controlled. Recommended. CDWALite format where possible

**Data values for *unit*:** *cm, mm, m, g, kg, kb, Mb, Gb, px*, and others as recommended in CCO and CDWA. 

**Data values for *type*:** *height*, *duration*, and others as recommended in CCO and CDWA. 
 
## Sub-element: mediaDescription

**Description:** Used to describe the role and content of a piece of media.

**Required**

**Element tag:** `<cs:mediaDescription>`

**Data values:**  Uncontrolled. Free text description of the media, prioritizing information that is not otherwise described in the schema.
 
## Sub-element: mediaLanguage

**Description:** The main language of the piece of media

**Repeatable, Optional**

**Element tag:** `<cs:mediaLanguage>`

**Attributes:** *type*

**Data values:**  Controlled. Recommended. Language formulated according to rules in the CCO and CDWA (i.e., ISO 639-2b, RFC 3066 and other encoding schemes may be used, or another authoritative source may be used, such as Ethnologue: Languages of the World. 14th edition. Barbara F. Grimes, ed. Dallas, Texas: SIL International, 2000). If ISO or other codes are used, they must be translated into common English for end-users. 

**Recommended values for *type*:** current, former, translated, local, and others as recommended in CCO and CDWA. 
