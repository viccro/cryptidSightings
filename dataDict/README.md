# Cryptid Media schema

Cryptid Media Schema (Version 1.0) was created as a final project for LIS 445: Metadata at Simmons 
University, in the School of Library and Information Science (SLIS). The schema was created by:
* Tish Albro
* Stephanie Bennett
* Vicki Crosson
* Alex Werbizky Ehrhardt

This version of the schema will be documented at www.github.com/viccro/cryptidSightings/tree/main/dataDict/
The latest version of the schema may be downloaded [at this link](https://raw.githubusercontent.com/viccro/cryptidSightings/main/cryptid-media-1.0.xsd).

The Cryptid Sightings Schema will be used to document any sighting of a cryptid (any animal whose 
existence is unsubstantiated). 

The schema makes use of a lot of structures found in CDWAlite, especially with regards to attributes.

## Schema Structure

* [cryptidMedia](cryptidMedia.md)
    * [mediaDetails](mediaDetails.md)
        * [mediaIdentifier](cryptidMedia.md#sub-element-mediaIdentifier)
        * [mediaName](cryptidMedia.md#sub-element-medianame)
        * [mediaType](cryptidMedia.md#sub-element-mediatype)
        * [mediaAffiliation](cryptidMedia.md#sub-element-mediaaffiliation)
        * [mediaPublicationDate](date.md)
        * [mediaDimensions](cryptidMedia.md#sub-element-mediaDimensions)
        * [mediaDescription](cryptidMedia.md#sub-element-mediadescription)

    * [accountOfSighting](account.md)
        * [observer](account.md#sub-element-observer)
        * [cryptidSeen](account.md#sub-element-cryptidseen)
            * [cryptidCanonicalName](cryptid.md#sub-element-cryptidcanonicalname)
            * [cryptidAlternativeName](account.md#sub-element-cryptidalternativename)
            * [cryptidDescription](account.md#sub-element-cryptiddescription)
        * [sightingDate](date.md)
            * [exactDate](date.md#sub-element-exactdate)
            * [approximateDate](date.md#sub-element-approximatedate)
            * [unknownDate](date.md#sub-element-unknowndate)
        * [sightingTime](time.md)
            * [timeDetails](timeDetails.md)
                * [exactTime](timeDetails.md#sub-element-exacttime)
                * [approximateTime](timeDetails.md#sub-element-approximatetime)
                * [unknownTime](time.md#sub-element-unknowntime)
            * [timeType](time.md#sub-element-timetype)
        * [sightingLocation](location.md)
            * [continent](location.md#sub-element-continent)
            * [geoCoordinates](location.md#sub-element-geocoordinates)
                * [longitude](coordinates.md#sub-element-longitude)
                * [latitude](coordinates.md#sub-element-latitude)
            * [postalAddress](postalAddress.md)
                * [addressCountry](postalAddress.md#sub-element-addresscountry)
                * [addressRegion](postalAddress.md#sub-element-addressregion)
                * [addressLocality](postalAddress.md#sub-element-addresslocality)
                * [postalCode](postalAddress.md#sub-element-postalCode)
                * [streetAddress](postalAddress.md#sub-element-streetaddress)
            * [unknownLocation](location.md#sub-element-unknownlocation)
            * [locationDescription](location.md#sub-element-locationdescription)
        * [descriptionOfAccount](account.md#sub-element-descriptionofaccount)

    * [mentionedEvidence](cryptidMedia.md#sub-element-mentionedevidence)
        * [evidenceAffirmative](evidence.md)
            * [evidenceAgent](evidence.md#sub-element-evidenceagent)
            * [evidenceType](evidence.md#sub-element-evidencetype)
            * [mediaEvidence](mediaDetails.md)
            * [mediaIdentifier](cryptidMedia.md#sub-element-mediaIdentifier)
                * [mediaName](cryptidMedia.md#sub-element-medianame)
                * [mediaType](cryptidMedia.md#sub-element-mediatype)
                * [mediaAffiliation](cryptidMedia.md#sub-element-mediaaffiliation)
                * [mediaPublicationDate](cryptidMedia.md#sub-element-mediapublicationdate)
                * [mediaDimensions](cryptidMedia.md#sub-element-mediaDimensions)
                * [mediaDescription](cryptidMedia.md#sub-element-mediadescription)
            * [evidenceDescription](evidence.md#sub-element-evidenceAgent)
        * [evidenceNegative](evidence.md)
            * [evidenceAgent](evidence.md#sub-element-evidenceagent)
            * [evidenceType](evidence.md#sub-element-evidencetype)
            * [mediaEvidence](mediaDetails.md)
            * [mediaIdentifier](cryptidMedia.md#sub-element-mediaIdentifier)
                * [mediaName](cryptidMedia.md#sub-element-medianame)
                * [mediaType](cryptidMedia.md#sub-element-mediatype)
                * [mediaAffiliation](cryptidMedia.md#sub-element-mediaaffiliation)
                * [mediaPublicationDate](cryptidMedia.md#sub-element-mediapublicationdate)
                * [mediaDimensions](cryptidMedia.md#sub-element-mediaDimensions)
                * [mediaDescription](cryptidMedia.md#sub-element-mediadescription)
            * [evidenceDescription](evidence.md#sub-element-evidenceAgent)

## Change log:
* v0.2: 
    * cryptid contains xs:choice, not xs:all
    * moved mediaSource (prev media) inside of accountOfSighting (prev reportOfSighting)
    * canonicalName termsource and termsourceID moved to attributes
    * offer exact and approx times, and type of time to qualify ranges
        * require mediaName
    * fleshed out docstrings for each field

* v0.3: Corrections made after filling out Category A corpus
    * descriptionOfReport renamed to descriptionOfAccount
    * personWhoSaysThis renamed to evidenceAgent
    * mediaLanguage added with type attribute
    * attributes added to mediaDimensions
    * person fields have type attribute to identify "individual" or "group"
    * choices and alls have been changed to sequences where applicable
    
* v0.4: Changed from cryptid-sightings schema to cryptid-media schema
    * root element is now mediaSource
    * exactTime>date corrected to exactTime>time
    * rearranged objects to be in the order that they're used
    * restructured time to allow for description of what the timestamp is describing
    
* v0.5 - v0.7: Changes reflect global copy edits from checking against the reality of the .xsd functions in practice, reflect decisions from discussions, and Stephanie's edit notes on her practice v0.4 xml records.
    * Created a googleDoc table of resources we reference in the data dictionary
    * Created the global attribute "lang" and assigned a CV of LOC
    * Updates to to the following sections:
       * cryptid.md
         * update cryptidCannonicalName description, values for termSource, and termSourceID
       * cryptidMedia.md
         * described cryptedMedia as the root element
       * date.md
         * updated unknownDate description for clarity
       * evidence.md
         * updated sub-elements to "non-repeatable" as they are coded in the .xsd. The evidenceAffirmative and evidenceNegative wrappers are repeatable, but the evidence sub-elements within those wrappers are non-repeatable. 
       * location.md
       * mediaDetails
         * updated descriptions
         * updated descriptions as necessary
         * updated mediaLanguage with a link to the new arrtibute "lang" 
         * added attribute "supplied" fixed value "yes" to mediaName element ONLY
         * mediaName is now required and repeatable
         * mediaName now has limited attributes		
         * mediaType is now required and repeatable
         * mediaType now has limited attributes		
         * mediaAffiliation now has limited attributes
         * prohibited attributes in mediaDescription
         * mediaDimensions calls out "word count" and "page count" as a recommended terms
       * mentionedEvidence
         * updated annotation descriptions
         * added element evidenceClassification with restricted attribute values. created use description
         * prohibited attributes in evidenceDescription
       * timeDetails
         * defined terms "day" and "night"
    
* v1.0 Minor edits made to align xsd with data dictionary
    * Prefer 'None' to domain or empty for uncontrolled mediaAffiliations
    * Remove lang attribute from mediaLanguage
    * Add termSource attribute to mediaLanguage, to specify CV used
    * Removed lang attribute from cryptidDescription
    * Made continent an enum
    * Attributes now required
    * evidenceType repeated
    * mediaIdentifier required
    * set supplied attribute to true and false, rather than yes/no
    * cryptidDescription optional
    * mediaEvidence optional