# Element: cryptidMedia

**Description:** Root element. An object describing a media accounting of the sighting, such as those published in a newspaper article, book, or blog post.

**Element tag:** `<cs:mediaEvidence>`


## Sub-element: [mediaDetails](mediaDetails.md)

**Description:** Details about this media object that describes a cryptid sighting

**Non-repeatable, Required**

**Element tag:** `<cs:mediaDetails>`

## Sub-element: [accountOfSighting](account.md)

**Description:** A consistent account of the sighting as described in this media source. Multiple observers may each disagree on details, resulting in multiple accounts per piece of media.

**Repeatable, Required**

**Element tag:** `<cs:accountOfSighting>`

## Sub-element: [mentionedEvidence](mentionedEvidence.md)

**Description:** Used to list evidence mentioned in the media source, from media recordings to plaster casts, body parts or costume pieces.

**Repeatable, Optional**

**Element tag:** `<cs:mentionedEvidence>`
