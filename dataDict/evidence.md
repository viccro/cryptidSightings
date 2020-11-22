# Element: evidence

**Description:** An object describing a piece of evidence, for or against, related to the claim of the sighting
 
## Sub-element: evidenceAgent

**Element tag:** `<cs:evidenceAgent>`

**Description:** A person or organization who stands behind the piece of evidence

**Repeatable, Optional**

**Data values:**  Controlled. Recommended: Library of Congress Name Authority File
 

## Sub-element: evidenceType

**Element tag:** `<cs:evidenceType>`

**Description:** The type of thing that comprises the evidence, taken from the Local Evidence Dictionary or standard terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports controlled vocabulary

**Repeatable, Optional**

**Data values:**  Controlled. Recommended: Local Evidence Dictionary or terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports Terms: ANSI/ASB Standard 019, Wildlife Forensics General Standards, First Edition, 2019 , ANSI/ASB Standard 028, Wildlife Forensics Morphology Standards, First Edition, 2019 , ANSI/ASB Standard 048, Wildlife Forensic DNA Standard Procedures, First Edition, 2019.

 
## Sub-element: mediaEvidence

**Element tag:** `<cs:mediaEvidence>`

**Description:** Details about a media object that serves as evidence for or against a cryptid sighting. If the media itself gives details about a cryptid sighting, a whole cryptidMedia object should be created, and only the mediaIdentifier of that object should be included. If the object is an image or footage, which doesn't contain enough information to create a full cryptidMedia entry, fill out this details block in full.

**Optional**

**Data values:** [mediaDetails](mediaDetails.md)


## Sub-element: evidenceDescription

**Description:** Used to describe the role and content of a piece of evidence.

**Repeatable, Optional**

**Element tag:** `<cs:evidenceDescription>`

**Data values:**  Uncontrolled. Free text description.

