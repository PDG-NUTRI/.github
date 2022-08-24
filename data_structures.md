# Data structures
This document defines the data structures used in our database. Each subsection represent a data structure composed of one or more datafields.
Data fields in **bold** are mendatory.
## Dietitian
- **id** : Integer
- **firstName** : Text string
- **lastName** : Text string
- **clientList** : Array Integer
- **password** : Text string
- **birthDate** : Date and time
- **avs** : Integer
## Client
- **firstName** : Text string
- **lastName** : Text string
- **birthDate** : Date and time
- **phoneNumber** : Integer
- **insurance** : Integer
- familySituation : Text string
- healthStatus : Text string
- medication : Text string
- history : Text string
- profession : Text string
- sport : Text string
- hobby : Text string
- foodBehavior : Text string
## Aftercare
- **bmi** : Integer
- **weight** : Float
- **diagnostic** : Text string
- comments : Text string
- **motivations** : Text string
- **foodObjectives** : Text string
- **startDate** : Date and time
- **endDate** : Date and time
- **documents** : Array Reference
## Meal
- **startTime** : Date and time
- **endTime** : Date and time
- **hunger** : Integer (0-5)
- **photos** : Reference
- satiety : Integer (0-4)
- setting : Text string
- comments : Text string