
The ADW-Message-Bundle-1 bundle resource profile is used in the ADW interfaces as a container to collect the ADW profiles in the following combined order: 

- ADW-DischargeNoticeAcceptResponse-Message-Header-1 [ADW-DischargeNoticeAcceptResponse-Message-Header-1]
- ADW-ReferralRequest-Accepted-1 [ADW-ReferralRequest-Accepted-1]
- CareConnect-ADW-Encounter-1 [CareConnect-ADW-Encounter-1]
- Careconnect-Patient-1 [CareConnect-Patient-1]
- Careconnect-Practitioner-1 [CareConnect-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]

----------

Note: Only the ADW data set fields are supported by the National Adapter and therefore optional data will not be retained within transformed messages. 
Optional data in FHIR messages that are "passed through" the adapter will not be removed.

----------

[ADW-Message-DischargeNoticeAcceptResponse-1-Ex01]: ../Examples/Profile.ADW-DischargeNoticeAcceptResponse/ADW-Message-DischargeNoticeAcceptResponse-1-Ex01.xml

[ADW-Message-DischargeNoticeAcceptResponse-1-Ex02]: ../Examples/Profile.ADW-DischargeNoticeAcceptResponse/ADW-Message-DischargeNoticeAcceptResponse-1-Ex02.xml


###  ADW Data set Mapping for ADW Discharge Notice Accept Response message bundle. ###


----------



| REQUIRED DATA FIELD                      | FHIR PROFILE ELEMENT                              |
|------------------------------------------|---------------------------------------------------|
| **Discharge Notice Accept Response**     |                                                   |
| Notice Receipt issued date               | [MessageHeader.timestamp (ADW Accept Response Message Sent Time)]                        |
| Notice Type                              | [MessageHeader.event.code (Accept Response Type)]                                     |
| Response Type                            | [MessageHeader.response.code]                                     |
| Response Details                         | [MessageHeader.reason.text (Accept Reason)]                                        |
| **Patient Identifiers**                  |                                                   |
| Patient NHS Number                       | [Patient.identifier (NHS Number)]                          |
| Hospital Patient Identifier              | [Patient.identifier (Hospital Patient Identifier)]            |
| **Patient Name**                         |                                                  |
| Family Name                              | [Patient.name.family (Family Name)]                                     |
| First Given Name                         | [Patient.name.given (First Given Name)]                                       |
| **Patient Birth Date**                   |                                                  |
| Patient Birth Date                       | [Patient.birthDate (Patient Birth Date)]                                      |
| **Person Stated Gender**                 |                                                  |
| Patient Stated Gender                    | [Patient.gender (Patient stated gender)]                                         |
| **Hospital**                             |                                                  |
| Organization Site Code                   | [Organization.identifier (Organization Site Code)]             |
| Hospital Name                            | [Organization.name (Hospital/Local Authority)]                                |
| Ward Name                                | [Location.name (Ward)]                                     |
| **Hospital Liaison Name**                |                                                  |
| Family Name                              | [Practitioner.name.family (Family Name - Hospital Liaison)]                                  |
| First Given Name                         | [Practitioner.name.given (First Given Name - Hospital Liaison)]                         |
| **Hospital Liaison Contact Details**     |                                                  |
| Hospital Liaison Email Address           | [Practitioner.telecom.value (Hospital Liaison Email)]               |
| Hospital Liaison Telephone Number        | [Practitioner.telecom.value (Hospital Liaison Telephone no.)]                            |
| **Local Authority**                      |                                                  |
| Organization Site Code                   | [Organization.identifier (Organization Site Code)]               |
| Local Authority Name                     | [Organization.name (Hospital/Local Authority)]                         |
| Social Services Team                     | [Organization.name (Social Services' team)] 
| **Local Authority Contact Name**         |                                                   |
| Family Name                              | [Practitioner.name.family (Local Authority Contact)]                                  |
| First Given Name                         | [Practitioner.name.given (Local Authority Contact)]                                  |
| **Local Authority Contact Details**      |                                                   |
| Local Authority Contact Email Address    | [Practitioner.telecom.value (Local Authority Contact Email)]                            |
| Local Authority Contact Telephone Number | [Practitioner.telecom.value (Local Authority Contact Telephone no.)]                    |


[ADW-DischargeNoticeAcceptResponse-Message-Header-1]: adw-discharge-notice-accept-response-message-header-1.html
[ADW-ReferralRequest-Accepted-1]: adw-referral-request-accepted-1.html
[careconnect-patient-1]: careconnect-patient-1.html
[careconnect-practitioner-1]: careconnect-practitioner-1.html
[CareConnect-Organization-1]: CareConnect-Organization-1.html
[CareConnect-ADW-Encounter-1]: adw-response-encounter-1.html
[CareConnect-Organization-1]: CareConnect-Organization-1.html
[careconnect-location-1]: careconnect-location-1.html


[MessageHeader.timestamp (ADW Accept Response Message Sent Time)]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.ADW%20Accept%20Response%20Message%20Sent%20Time
[MessageHeader.event.code (Accept Response Type)]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.event.Accept%20Response%20Type
[MessageHeader.response.code]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.response.Response%20Type
[MessageHeader.reason.text (Accept Reason)]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.reason.Accept%20Reason
[Patient.identifier (NHS Number)]: careconnect-patient-1-dict.html#Patient.NHS%20Number
[Patient.identifier.type (NHS Number Status Indicator)]: careconnect-patient-1-dict.html#Patient.identifier.NHS%20Number%20Status%20Indicator  
[Patient.identifier (Hospital Patient Identifier)]: careconnect-patient-1-dict.html#Patient.Hospital%20Patient%20Identifier 
[Patient.name.family (Family Name)]: careconnect-patient-1-dict.html#Patient.name.Family%20name
[Patient.name.given (First Given Name)]: careconnect-patient-1-dict.html#Patient.name.First%20given%20name
[Patient.birthDate (Patient Birth Date)]: careconnect-patient-1-dict.html#Patient.Patient%20Birth%20Date
[Patient.gender (Patient stated gender)]: careconnect-patient-1-dict.html#Patient.Patient%20stated%20gender
[Organization.identifier (Organization Site Code)]: CareConnect-Organization-1-dict.html#Organization.Organization%20Site%20Code
[Organization.name (Hospital/Local Authority)]: CareConnect-Organization-1-dict.html#Organization.Hospital%20or%20Local%20Authority%20Name
[Location.name (Ward)]: careconnect-location-1-dict.html#Location.Ward%20name
[identifier (Hospital - ODS Organisation Code)]: CareConnect-Organization-1-dict.html#Organization.ODS%20Organisation%20Code
[name (Hospital)]: CareConnect-Organization-1-dict.html#Organization.name
[name (Ward)]: CareConnect-Organization-1-dict.html#Organization.name
[Practitioner.name.family (Family Name - Hospital Liaison)]: careconnect-practitioner-1-dict.html#Practitioner.name.Family%20name
[Practitioner.name.given (First Given Name - Hospital Liaison)]: careconnect-practitioner-1-dict.html#Practitioner.name.First%20given%20name
[Practitioner.telecom.value (Hospital Liaison Email)]: careconnect-practitioner-1-dict.html#Practitioner.telecom.Practitioner%20Email%20address%20string
[Practitioner.telecom.value (Hospital Liaison Telephone no.)]: careconnect-practitioner-1-dict.html#Practitioner.telecom.Practitioner%20Telephone%20number%20string
[identifier (Local Authority - ODS Organisation Code)]: CareConnect-Organization-1-dict.html#Organization.ODS%20Organisation%20Code
[Organization.name (Hospital/Local Authority)]: CareConnect-Organization-1-dict.html#Organization.Hospital%20or%20Local%20Authority%20Name
[Organization.name (Social Services' team)]: CareConnect-Organization-1-dict.html#Organization.Social%20Services%20team
[Practitioner.name.family (Local Authority Contact)]: careconnect-practitioner-1-dict.html#Practitioner.name.Family%20name
[Practitioner.name.given (Local Authority Contact)]: careconnect-practitioner-1-dict.html#Practitioner.name.First%20given%20name
[Practitioner.telecom.value (Local Authority Contact Email)]: careconnect-practitioner-1-dict.html#Practitioner.telecom.Practitioner%20Email%20address%20string
[Practitioner.telecom.value (Local Authority Contact Telephone no.)]: careconnect-practitioner-1-dict.html#Practitioner.telecom.Practitioner%20Telephone%20number%20string

----------


### Referencing of profiles for ADW Discharge Notice Accept Response message bundle.###


The diagram shows the referencing for a typical Discharge Notice Accept Response message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for an Discharge Notice Accept Response](../Profile.ADW-DischargeNoticeAcceptResponse/MessageReferencing4.png)

----------


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/profiling.html
[FHIR website]: http://hl7.org/fhir/index.html
[Base Resource Definitions]: http://hl7.org/fhir/resource.html
