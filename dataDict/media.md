# Element: mediaType
**Element tag**<cs:mediaType>
**Description** Use to describe the type of content of the media: digital photograph, motion picture film, article, book, etc.
**Attributes:** *termSource, termSourceId*
**Non-Repeatable, Optional**
[IS mediaType CONTROLLED?]
## Sub-Element: mediaName
**Element tag**<cs:mediaName>
**Description**A name identifying the piece of media. If none is known, use a unique phrase that identifies it by type, contents, and/or creators
**Non-Repeatable, Required**
## Sub-Element: mediaIdentifier
**Element tag**<cs:mediaIdentifier>
**Description**A single URL, ISBN, or other identifier for the media
**Attributes** *type*
**Non-Repeatable, Optional**
## Sub-Element: mediaAffiliation
**Element tag**<cs:mediaAffiliation>
**Description**If the media was published in a collection, newspaper, etc, list that affiliation here.
**Non-Repeatable, Optional**
## Sub-Element: mediaPublicationDate
**Element tag**<cs:mediaPublicationDate>
**Description**The publication date of the media, such as the copyright date of a book, or the date a blog was posted
**Non-Repeatable, Optional**
**Data Values** Date formatted as YYYY-MM-DD
## Sub-Element: mediaDimensions
**Element tag**<cs:mediaDimensions>
**Description**Dimensions related to the media: page count, size of book, seconds or frames of video, file size in bytes or pixels, etc
**Attributes** *unit, type*
**Non-Repeatable, Optional**
**Data Values** Controlled.  Recommended: Taken from CDWA/CCO.
## Sub-Element: mediaDescription
**Element tag**<cs:mediaDescription>
**Description** [WHAT ARE WE GOING FOR WITH THIS ONE?  I CAN GUESS, BUT I’M NOT GOING TO.]
**Non-Repeatable, Required**
## Sub-Element: mediaLanguage
**Element tag**<cs:mediaLanguage>
**Description** The main language of the piece of media.
**Attributes** *type*
**Repeatable, Optional**
**Recommended values for *type* ** Include ‘translated’ and ‘original.’
