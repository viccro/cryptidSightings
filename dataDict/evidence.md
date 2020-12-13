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

### Tagging Examples:

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

### Tagging Examples:
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

### Tagging Examples:
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

### Tagging Examples:
`<evidenceDescription>The creature captured in the photograph is a creation by Marmaduke Wetherell, created by combining different children's toys.</evidenceDescription>`

`<evidenceDescription>Eric Shipton's photograph of an alleged Yeti footprint, 13 inches in length, shows five toes, with an apparent 'big toe.'</evidenceDescription>`