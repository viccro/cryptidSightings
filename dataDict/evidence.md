# Element: evidence

**Description:** An object describing a piece of evidence, for or against, related to the claim of the sighting
 
## Sub-element: evidenceAgent

**Element tag:** `<evidenceAgent>`

**Description:** The names, appellations, or other identifiers assigned to an individual, group of people, firm or other corporate body, or other entity that provided the piece of evidence. Use of a Name Authority is recommended. The name should be in natural order, if possible.  If there is no known creator, make a reference to the presumed culture or nationality of the unknown creator (e.g., use “Unknown Spanish woman” or “Unknown man” before "Unknown")

**Repeatable, Optional**

**Data values:**  Controlled. Recommended: Library of Congress Name Authority File

**Attributes:** *termSource*, *termSourceID*

**Recommended values for *termSource*:** A controlled vocabulary such as the Library of Congress Name Authority File. If not present in a CV, enter the type of source, such as "URL".

**Recommended values for *termSourceID*:** A controlled vocabulary identification number such as the Library of Congress Name Authority File. If not present in a CV, enter a unique identifier such as a URL address.
 
## Sub-element: evidenceClassification

**Element tag:** `<evidenceClassification>`

**Description:** The legal category corresponding to the evidenceType presented. Limited to physical, testimonial, demonstrative, and documentary

**Optional**

**Data values:** Optional. Repeat the attribute value for display text.

**Attributes:** Controlled. Limited to physical, testimonial, demonstrative, and documentary


## Sub-element: evidenceType

**Element tag:** `<evidenceType>`

**Description:** The type of thing that comprises the evidence, taken from the Local Evidence Dictionary or standard terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports controlled vocabulary

**Optional**

**Data values:**  Controlled. Recommended: Local Evidence Dictionary or terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports Terms: ANSI/ASB Standard 019, Wildlife Forensics General Standards, First Edition, 2019 [http://www.asbstandardsboard.org/wp-content/uploads/2019/05/019_Std_e1.pdf]; ANSI/ASB Standard 028, Wildlife Forensics Morphology Standards, First Edition, 2019 [http://www.asbstandardsboard.org/wp-content/uploads/2019/05/028_Std_e1.pdf]; ANSI/ASB Standard 048, Wildlife Forensic DNA Standard Procedures, First Edition, 2019 [http://www.asbstandardsboard.org/wp-content/uploads/2019/05/048_Std_e1.pdf].

**Attributes:** *termSource*, *termSourceID*

**Recommended values for *termSource*:** See list of local acronyms. Recommended are: WFSGeneral, WFSMorphology, and WFSDNA.

 
## Sub-element: [mediaEvidence](mediaDetails.md)

**Element tag:** `<mediaEvidence>`

**Description:** Details about a media object that serves as evidence for or against a cryptid sighting. If the media itself gives details about a cryptid sighting, a whole cryptidMedia object should be created, and only the mediaIdentifier of that object should be included. If the object is an image or footage, which doesn't contain enough information to create a full cryptidMedia entry, fill out this details block in full.

**Optional**

**Data values:** [mediaDetails](mediaDetails.md)


## Sub-element: evidenceDescription

**Description:** Used to describe the role and content of a piece of evidence.

**Optional**

**Element tag:** `<evidenceDescription>`

**Data values:**  Uncontrolled. Free text description.

