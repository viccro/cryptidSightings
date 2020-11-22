# Cryptid Media schema

Cryptid Media Schema (Version 0.4) was created as a draft for LIS 445: Metadata at Simmons 
University, in the School of Library and Information Science (SLIS). The schema was created by:
* Tish Albro
* Stephanie Bennett
* Vicki Crosson
* Alex Werbizky Ehrhardt

This version of the schema will be documented at www.github.com/viccro/cryptidSightings/tree/main/dataDict/

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