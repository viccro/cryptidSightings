# Element: evidence
**Description:** An object describing a piece of evidence to either uphold in the affirmative (<evidenceAffirmative>) or reject in the negative (<evicendeNegative>) the claim of the cryptid sighting.
**Repeatable, Optional**
 
## Sub-element: evidenceAgent
**Description:** A person or organization who stands behind the piece of evidence
**Repeatable, Optional**
**Element tag:** <cs:evidenceAgent>
**Attributes:** *evidenceSource, termSource, termSourceId, type, unit*
**Data values:**  Controlled. Recommended: Library of Congress Name Authority File
**Recommended values for *termSource*:** *LOC* 
**Recommended values for *termSourceID*:** Library of Congress Name Authority File control number
 
## Sub-element: evidenceType
**Description:** The type of thing that comprises the evidence, taken from the Local Evidence Dictionary or standard terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports controlled vocabulary
**Repeatable, Optional**
**Element tag:** <cs:evidenceType >
**Attributes:** *evidenceSource, termSource, termSourceId, type, unit*
**Data values:**  Controlled. Recommended: Local Evidence Dictionary or terminology from the National Institute of Standard and Technology U.S. Department of Commerce Wildlife Forensics Subcommittee Reports Terms: ANSI/ASB Standard 019, Wildlife Forensics General Standards, First Edition, 2019 , ANSI/ASB Standard 028, Wildlife Forensics Morphology Standards, First Edition, 2019 , ANSI/ASB Standard 048, Wildlife Forensic DNA Standard Procedures, First Edition, 2019 .
**Recommended values for *termSource*:** *WFS * 
**Recommended values for *termSourceID*:** Relative source indicator of “local”, “Morphology” , “General” , “DNA”
**Recommended values for *type*:** See Local Evidence Dictionary Appendix. *physical* , *testimonial* , *demonstrative*, *documentary*
 
## Sub-element: mediaEvidence
**Description:** Used to identify media evidence, like a video recording or photograph. All sub-elements of the <media> wrapper may be entered within <mediaEvidence>
**Repeatable, Optional**
**Element tag:** < cs:mediaEvidence >

## Sub-element: evidenceDescription
**Description:** Used to describe the role and content of a piece of evidence.
**Repeatable, Optional**
**Element tag:** < cs:evidenceDescription >
**Attributes:** * evidenceSource, termSource, termSourceId, type, unit *
**Data values:**  Uncontrolled. Free text description

