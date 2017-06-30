
The ADW-Message-Bundle-1 bundle is used in ADW as a container to collect the ADW profiles listed below:- 

- ADW-WithdrawalNoticeAcceptResponse-Message-Header-1 [ADW-WithdrawalNoticeAcceptResponse-Message-Header-1]
- ADW-ReferralRequest-Cancelled-1 [ADW-ReferralRequest-Cancelled-1]
- CareConnect-ADW-Encounter-1 [CareConnect-ADW-Encounter-1]
- CareConnect-Patient-1 [CareConnect-Patient-1]
- CareConnect-ADW-Practitioner-1 [CareConnect-ADW-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]
- ADW-Condition-1 [ADW-Condition-1]

----------

[ADW-Message-WithdrawalNoticeAcceptResponse-1-Ex01]: ../Examples/Profile.ADW-WithdrawalNoticeAcceptResponse/ADW-Message-WithdrawalNoticeAcceptResponse-1-Ex01.xml

[ADW-Message-WithdrawalNoticeAcceptResponse-1-Ex02]: ../Examples/Profile.ADW-WithdrawalNoticeAcceptResponse/ADW-Message-WithdrawalNoticeAcceptResponse-1-Ex02.xml


###  ADW Data set Mapping for ADW Withdrawal Notice Accept Response message bundle. ###


----------

| REQUIRED DATA FIELD                      | FHIR PROFILE ELEMENT                              |
|------------------------------------------|---------------------------------------------------|
| **Withdrawal Notice Accept Response**    |                                                   |
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
| Organisation ODS Code                    | [Organization.identifier (ODS Organisation Code)]                                     |
| Local Authority Name                     | [Organization.name]                         |
| Social Services Team                     | [Organization.name] 
| **Local Authority Contact Name**         |                                                   |
| Family Name                              | [Practitioner.name.family]                                  |
| First Given Name                         | [Practitioner.name.given]                                  |
| **Local Authority Contact Details**      |                                                   |
| Local Authority Contact Email Address    | [Practitioner.telecom.value]                            |
| Local Authority Contact Telephone Number | [Practitioner.telecom.value]                    |


[ADW-WithdrawalNoticeAcceptResponse-Message-Header-1]: adw-withdrawal-notice-accept-response-message-header-1.html
[ADW-ReferralRequest-Cancelled-1]: adw-referral-request-cancelled-1.html
[CareConnect-Patient-1]: careconnect-patient-1.html
[CareConnect-ADW-Practitioner-1]: careconnect-adw-practitioner-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-ADW-Encounter-1]: careconnect-adw-encounter-1.html
[CareConnect-Location-1]: careconnect-location-1.html
[ADW-Condition-1]: adw-condition-1.html



[MessageHeader.timestamp (ADW Accept Response Message Sent Time)]: adw-withdrawal-notice-accept-response-message-header-1-dict.html#MessageHeader.ADW%20Accept%20Response%20Message%20Sent%20Time
[MessageHeader.event.code (Accept Response Type)]: adw-withdrawal-notice-accept-response-message-header-1-dict.html#MessageHeader.event.Accept%20Response%20Type
[MessageHeader.event.code]: adw-withdrawal-notice-accept-response-message-header-1-dict.html#MessageHeader.event.Accept%20Response%20Type
[MessageHeader.reason.text (Accept Reason)]: adw-withdrawal-notice-accept-response-message-header-1-dict.html#MessageHeader.reason.Accept%20Reason
[Patient.nhsNumber]: careconnect-patient-1-dict.html#Patient.nhsNumber
[Patient.localIdentifier]: careconnect-patient-1-dict.html#Patient.localIdentifier 
[Patient.name.family]: careconnect-patient-1-dict.html#Patient.name.family
[Patient.name.given]: careconnect-patient-1-dict.html#Patient.name.given
[Patient.birthDate]: careconnect-patient-1-dict.html#Patient.birthDate
[Patient.gender]: careconnect-patient-1-dict.html#Patient.gender
[Organization.identifier (Organisation Site Code)]: careconnect-organization-1-dict.html#Organization.ODS%20Site%20Code
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Location.name]: careconnect-location-1-dict.html#Location.name
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Practitioner.name.family]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Organization.identifier (ODS Organisation Code)]: careconnect-organization-1-dict.html#Organization.ODS%20Organisation%20Code
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Practitioner.name.family]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value


----------


### Referencing of profiles for ADW Withdrawal Notice Accept Response message bundle.###


The diagram shows the referencing for a typical Withdrawal Notice Accept Response message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for an Withdrawal Notice Accept Response](../Profile.ADW-WithdrawalNoticeAcceptResponse/MessageReferencing4.png)

----------


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on the [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html

