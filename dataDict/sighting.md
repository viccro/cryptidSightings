# Cryptid Sightings Schema

***
Cryptid Sightings Schema (Version 0.1) was created as a draft for LIS 445: Metadata at Simmons 
University, in the School of Library and Information Science (SLIS). The schema was created by:
* Tish Albro
* Stephanie Bennett
* Vicki Crosson
* Alex Werbizky Ehrhardt

This version of the schema will be documented at www.github.com/viccro/cryptidSightings/tree/main/dataDict/main.md

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
***

## Element: sighting
Documentation surrounding a singular sighting of a cryptid

### Sub-element: [accountOfSighting](account.md)
**Element tag:** `<cs:accountOfSighting>`
**Description:** A consistent account of the sighting. An observer may give multiple conflicting accounts over time, and multiple observers may each disagree on details, resulting in multiple accounts per sighting.
**Repeatable, Required** 

### Sub-element: [sightingDate](date.md)
**Element tag:** `<cs:sightingDate>`
**Description:** The date on which a sighting occurred. If the same cryptid was seen over multiple days, multiple sighting objects should be used to describe these discrete sightings.
**Non-Repeatable, Optional** 

### Sub-element: [sightingTime](time.md)
**Element tag:** `<cs:sightingTime>`
**Description:** The time or range of times on which a single sighting occurred.
**Non-Repeatable, Optional** 

### Sub-element: [sightingLocation](location.md)
**Element tag:** `<cs:sightingLocation>`
**Description:** The place that the cryptid was seen.
**Repeatable, Optional** 

### Sub-element: [evidenceAffirmative](evidence.md)
**Element tag:** `<cs:evidenceAffirmative>`
**Description:** Evidence provided to prove the claims of the observers.
**Repeatable, Optional** 

### Sub-element: [evidenceNegative](evidence.md)
**Element tag:** `<cs:evidenceNegative>`
**Description:** Evidence provided to disprove the claims of the observers.
**Repeatable, Optional** 