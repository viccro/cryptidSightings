# Element: cryptidMedia

**Description:** Root element. A media object relating the account(s) of a cryptid sighting, such as those published in a newspaper article, book, or blog post

**Element tag:** `<mediaEvidence>`


## Sub-element: [mediaDetails](mediaDetails.md)

**Description:** Administrative and descriptive details about the media object that describes a cryptid sighting

**Non-repeatable, Required**

**Element tag:** `<mediaDetails>`

## Sub-element: [accountOfSighting](account.md)

**Description:** A consistent account of the sighting as described in this media source. Multiple observers may each disagree on details, resulting in multiple accounts per piece of media.

**Repeatable, Required**

**Element tag:** `<accountOfSighting>`

## Sub-element: [mentionedEvidence](mentionedEvidence.md)

**Description:** Used to list evidence mentioned in the media source, from media recordings to plaster casts, body parts or costume pieces.

**Repeatable, Optional**

**Element tag:** `<mentionedEvidence>`
