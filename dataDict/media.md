# Element: media
**Description:** Used to identify media evidence, like a video recording or photograph. All sub-elements of the <media> wrapper may be entered within <mediaEvidence>
**Repeatable, Optional**
**Element tag:** < cs:mediaEvidence >
 
## Sub-element: mediaType
**Description:** Use to describe the type of content of the media: digital photograph, motion picture film, article, book, etc. 
**Repeatable, Optional**
**Element tag:** < cs:mediaType >
**Attributes:** *termSource, termSourceId*
**Data values:**  Controlled. Recommended: Getty Art and Architecture Thesaurus 
**Recommended values for *termSource*:** *AAT* 
**Recommended values for *termSourceID*:** AAT number
 
## Sub-element: mediaName
**Description:** A name identifying the piece of media. If none is known, use a unique phrase that identifies it by type, contents, and/or creators. 
**Repeatable, Optional**
**Element tag:** < cs:mediaName >
**Attributes:** *evidenceSource, termSource, termSourceId, type, unit *
**Data values:**  Controlled. Recommended. Library of Congress Name Authority File if possible.
**Recommended values for *termSource*:** *LOC* 
**Recommended values for *termSourceID*:** LOC control number
 
## Sub-element: mediaIdentifier
**Description:** A single URL, ISBN, or other identifier for the media
**Repeatable, Optional**
**Element tag:** < cs:mediaIdentifier >
**Attributes:** *type*
**Data values:**  Uncontrolled. Free text description. Recommended use of permalinks for uri/url addresses.
**Recommended data values for *type*:** AAT term
 
## Sub-element: mediaAffiliation
**Description:** If the media was published in a collection, newspaper, etc, list that affiliation here.
**Repeatable, Optional**
**Element tag:** < cs:mediaAffiliation >
**Attributes:** * evidenceSource, termSource, termSourceId, type, unit *
**Data values:**  Controlled. Recommended. Library of Congress Name Authority File
**Recommended data values for *type*:** AAT term
**Recommended values for *termSource*:** *LOC* 
**Recommended values for *termSourceID*:** LOC control number
 
## Sub-element: mediaPublicationDate
**Description:** The publication date of the media, such as the copyright date of a book, or the date a blog was posted
**Repeatable, Optional**
**Element tag:** < cs:mediaPublicationDate >
**Element type:** Date 
		QUESTION: Do not know how to represent the exact vs. approximate date subelements.
**Data values:**  Controlled. Recommended. YYYY-MM-DD
 
## Sub-element: mediaDimensions
**Description:** Dimensions related to the media: page count, size of book, seconds or frames of video, file size in bytes or pixels, etc.
**Repeatable, Optional**
**Element tag:** < cs:mediaDimensions>
**Attributes:** *type, unit *
**Data values:**  Controlled. Recommended. CDWALite format where possible
**Data values for *unit*:** cm, mm, m, g, kg, kb, Mb, Gb, pixels, and others as recommended in CCO and CDWA. 

 
## Sub-element: mediaDescription
**Description:** Used to describe the role and content of a piece of media.
**Repeatable, Optional**
**Element tag:** < cs:mediaDescription >
**Attributes:** * evidenceSource, termSource, termSourceId, type, unit *
**Data values:**  Uncontrolled. Free text description
 
## Sub-element: mediaLanguage
**Description:** The main language of the piece of media
**Repeatable, Optional**
**Element tag:** < cs:mediaLanguage>
**Attributes:** *type*
**Data values:**  Controlled. Recommended. Language formulated according to rules in the CCO and CDWA (i.e., ISO 639-2b, RFC 3066 and other encoding schemes may be used, or another authoritative source may be used, such as Ethnologue: Languages of the World. 14th edition. Barbara F. Grimes, ed. Dallas, Texas: SIL International, 2000). If ISO or other codes are used, they must be translated into common English for end-users. 
**Recommended values for *type*:** current, former, translated, local, and others as recommended in CCO and CDWA. 

