# Cryptid Sightings Schema

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