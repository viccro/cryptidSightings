# Cryptid Sighting schema

***
Cryptid Sightings Schema (Version 0.1) was created as a draft for LIS 445: Metadata at Simmons 
University, in the School of Library and Information Science (SLIS). The schema was created by:
* Tish Albro
* Stephanie Bennett
* Vicki Crosson
* Alex Werbizky Ehrhardt

This version of the schema will be documented at www.github.com/viccro/cryptidSightings/tree/main/dataDict/

The Cryptid Sightings Schema will be used to document any sighting of a cryptid (any animal whose 
existence is unsubstantiated). 

The schema makes use of ___???

Change log:
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
***

* [sighting](sighting.md)
    * [accountOfSighting](account.md)
        * [observer](account.md#sub-element-observer)
        * [cryptidSeen](account.md#sub-element-cryptidseen)
            * [cryptidCanonicalName](cryptid.md#sub-element-cryptidcanonicalname)
            * [cryptidAlternativeName](account.md#sub-element-cryptidalternativename)
            * ...
        * [descriptionOfAccount](account.md#sub-element-descriptionofaccount)
        * [mediaSource](account.md#sub-element-mediasource)
    * [sightingDate](date.md)
    * [sightingTime](time.md)
    * ...