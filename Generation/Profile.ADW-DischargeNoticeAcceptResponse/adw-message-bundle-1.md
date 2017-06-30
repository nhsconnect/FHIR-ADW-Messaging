
The ADW-Message-Bundle-1 bundle is used in ADW as a container to collect the ADW profiles listed below:- 

- ADW-DischargeNoticeAcceptResponse-Message-Header-1 [ADW-DischargeNoticeAcceptResponse-Message-Header-1]
- ADW-ReferralRequest-Accepted-1 [ADW-ReferralRequest-Accepted-1]
- CareConnect-ADW-Encounter-1 [CareConnect-ADW-Encounter-1]
- CareConnect-Patient-1 [CareConnect-Patient-1]
- CareConnect-ADW-Practitioner-1 [CareConnect-ADW-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]
- ADW-Condition-1 [ADW-Condition-1]

----------

An instance of a DocumentReference and a Binary resource have been added to the end of the [Discharge Accept Response xml bundle example] to illustrate how a supporting document, in this case a pdf, could be attached to the message.

[Discharge Accept Response xml bundle example]: ../Examples/Profile.ADW-DischargeNoticeAcceptResponse/ADW-Message-Discharge-Notice-Accept-Response-Bundle-1-Example-1.xml

[ADW-Message-DischargeNoticeAcceptResponse-1-Ex01]: ../Examples/Profile.ADW-DischargeNoticeAcceptResponse/ADW-Message-DischargeNoticeAcceptResponse-1-Ex01.xml

[ADW-Message-DischargeNoticeAcceptResponse-1-Ex02]: ../Examples/Profile.ADW-DischargeNoticeAcceptResponse/ADW-Message-DischargeNoticeAcceptResponse-1-Ex02.xml


###  ADW Data set Mapping for ADW Discharge Notice Accept Response message bundle. ###


----------

Note that for sliced elements and extensions within CareConnect profiles, it is not possible to link to the exact sliced element in this mapping table.


| REQUIRED DATA FIELD                      | FHIR PROFILE ELEMENT                              |
|------------------------------------------|---------------------------------------------------|
| **Discharge Notice Accept Response**     |                                                   |
| Notice Receipt issued date               | [MessageHeader.timestamp (ADW Accept Response Message Sent Time)]                        |
| Notice Type                              | [MessageHeader.event.code (Accept Response Type)]                                     |
| Response Type                            | [MessageHeader.event.code]                                    |
| Response Details                         | [MessageHeader.reason.text (Accept Reason)]                                        |
| **Patient Identifiers**                  |                                                   |
| Patient NHS Number                       | [Patient.nhsNumber]                          |
| Hospital Patient Identifier              | [Patient.localIdentifier]            |
| **Patient Name**                         |                                                  |
| Family Name                              | [Patient.name.family]                                     |
| First Given Name                         | [Patient.name.given]                                       |
| **Patient Birth Date**                   |                                                  |
| Patient Birth Date                       | [Patient.birthDate]                                      |
| **Person Stated Gender**                 |                                                  |
| Patient Stated Gender                    | [Patient.gender]                                         |
| **Hospital**                             |                                                  |
| Organisation Site Code                   | [Organization.identifier (Organisation Site Code)]             |
| Hospital Name                            | [Organization.name]                                |
| Ward Name                                | [Location.name]                                     |
| **Hospital Liaison Name**                |                                                  |
| Family Name                              | [Practitioner.name.family]                                  |
| First Given Name                         | [Practitioner.name.given]                         |
| **Hospital Liaison Contact Details**     |                                                  |
| Hospital Liaison Email Address           | [Practitioner.telecom.value]               |
| Hospital Liaison Telephone Number        | [Practitioner.telecom.value]                            |
| **Local Authority**                      |                                                  |
| Organization ODS Code                    | [Organization.identifier (ODS Organisation Code)]               |
| Local Authority Name                     | [Organization.name]                         |
| Social Services Team                     | [Organization.name] 
| **Local Authority Contact Name**         |                                                   |
| Family Name                              | [Practitioner.name.family]                                  |
| First Given Name                         | [Practitioner.name.given]                                  |
| **Local Authority Contact Details**      |                                                   |
| Local Authority Contact Email Address    | [Practitioner.telecom.value]                            |
| Local Authority Contact Telephone Number | [Practitioner.telecom.value]                    |


[ADW-DischargeNoticeAcceptResponse-Message-Header-1]: adw-discharge-notice-accept-response-message-header-1.html
[ADW-ReferralRequest-Accepted-1]: adw-referral-request-accepted-1.html
[CareConnect-Patient-1]: careconnect-patient-1.html
[CareConnect-ADW-Practitioner-1]: careconnect-adw-practitioner-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-ADW-Encounter-1]: careconnect-adw-encounter-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-Location-1]: careconnect-location-1.html
[ADW-Condition-1]: adw-condition-1.html


[MessageHeader.timestamp (ADW Accept Response Message Sent Time)]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.ADW%20Accept%20Response%20Message%20Sent%20Time
[MessageHeader.event.code (Accept Response Type)]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.event.Accept%20Response%20Type
[MessageHeader.event.code]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.event.Accept%20Response%20Type
[MessageHeader.reason.text (Accept Reason)]: adw-discharge-notice-accept-response-message-header-1-dict.html#MessageHeader.reason.Accept%20Reason
[Patient.nhsNumber]: careconnect-patient-1-dict.html#Patient.nhsNumber
[Patient.localIdentifier]: careconnect-patient-1-dict.html#Patient.localIdentifier
[Patient.name.family]: careconnect-patient-1-dict.html#Patient.name.family
[Patient.name.given]: careconnect-patient-1-dict.html#Patient.name.given
[Patient.birthDate]: careconnect-patient-1-dict.html#Patient.birthDate
[Patient.gender]: careconnect-patient-1-dict.html#Patient.gender
[Organization.identifier (Organisation Site Code)]: careconnect-organization-1-dict.html#Organization.ODS%20Site%20Code
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Location.name]: careconnect-location-1-dict.html#Location.name
[Organization.identifier (ODS Organisation Code)]: careconnect-organization-1-dict.html#Organization.ODS%20Organisation%20Code
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Practitioner.name.family]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Practitioner.name.family]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value

----------


### Referencing of profiles for ADW Discharge Notice Accept Response message bundle.###


The diagram shows the referencing for a typical Discharge Notice Accept Response message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for an Discharge Notice Accept Response](../Profile.ADW-DischargeNoticeAcceptResponse/MessageReferencing4.png)

----------


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on the [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html
