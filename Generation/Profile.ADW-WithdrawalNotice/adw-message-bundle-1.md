
The ADW-Message-Bundle-1 bundle resource profile is used in the ADW interfaces as a container to collect the ADW profiles listed below:- 

- ADW-WithdrawalNotice-Message-Header-1 [ADW-WithdrawalNotice-Message-Header-1]
- ADW-ReferralRequest-Cancelled-1 [ADW-ReferralRequest-Cancelled-1]
- CareConnect-ADW-Encounter-1 [CareConnect-ADW-Encounter-1]
- CareConnect-Patient-1 [CareConnect-Patient-1]
- CareConnect-ADW-Practitioner-1 [CareConnect-ADW-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]

----------

[ADW-Message-WithdrawalNotice-1-Ex02]: ../Examples/Profile.ADW-WithdrawalNotice/ADW-Message-WithdrawalNotice-1-Ex02.xml


###  ADW Data set Mapping for ADW Withdrawal Notice message bundle. ###


----------

Note that for some sliced elements and extensions within CareConnect profiles, it is not possible to link to the exact sliced element in this mapping table.


| REQUIRED DATA FIELD                  | FHIR PROFILE ELEMENT                             |
|--------------------------------------|--------------------------------------------------|
| **Withdrawal Notice**                |                                                  |
| Withdrawal Notice Issued Date        | [MessageHeader.timestamp (ADW Message Sent Time)]              |
| **Patient Identifiers**              |                                                  |
| Patient NHS Number                   | [Patient.identifier.value (NHS Number)]                          |
| NHS Number Status Indicator          | [Patient.identifier.nhsNumberVerificationStatus]                            |
| Hospital Patient Identifier          | [Patient.identifier (Local Identifier)]            |
| **Patient Name**                     |                                                  |
| Family Name                          | [Patient.name.family]                                     |
| First Given Name                     | [Patient.name.given]                                       |
| **Patient Birth Date**               |                                                  |
| Patient Birth Date                   | [Patient.birthDate]                                      |
| **Person Stated Gender**             |                                                  |
| Patient Stated Gender                | [Patient.gender]                                         |
| **Patient Address**                  |                                                  |
| Address Line 1                       | [Patient.address.line]                                   |
| Address Line 2                       | [Patient.address.line]                                   |
| Address Line 3                       | [Patient.address.line]                                   |
| Address Line 4                       | [Patient.address.city]                                   |
| Address Line 5                       | [Patient.address.district]                                   |
| Postcode                             | [Patient.address.postalCode]                             |
| **Hospital**                         |                                                  |
| Organization Site Code               | [Organization.identifier.value (ODS Site Code)]             |
| Hospital Name                        | [Organization.name]                                |
| Ward Name                            | [Location.name]                                     |
| **Withdrawal Type**                  |                                                  |
| Withdrawal type                      | [MessageHeader.event.code(Withdrawal Notice Type)]                  |
| **Reason for Withdrawal**            |                                                  |
| Reason for Withdrawal                | [MessageHeader.reason.coding.display]                          |
| **Reason For Withdrawal - Other**    |                                                  |
| Reason For Withdrawal - Other        | [MessageHeader.reason.text (Other Reason for Withdrawal)]                           |
| **Lead Clinician Name**              |                                                  |
| Family Name                          | [Practitioner.name.family]                   |
| First Given Name                     | [Practitioner.name.given]                    |
| **Hospital Liaison Name**            |                                                  |
| Family Name                          | [Practitioner.name.family]                              |
| First Given Name                     | [Practitioner.name.given]                              |
| **Hospital Liaison Contact Details** |                                                  |
| Hospital Liaison Email Address       | [Practitioner.telecom.value]               |
| Hospital Liaison Telephone Number    | [Practitioner.telecom.value]                                  |
| **Local Authority**                  |                                                  |
| Organization Site Code               | [Organization.identifier.value (ODS Organisation Code)]               |
| Local Authority Name                 | [Organization.name]                         |
| Social Services Team                 | [Organization.name] 


[ADW-WithdrawalNotice-Message-Header-1]: adw-withdrawal-notice-message-header-1.html
[ADW-ReferralRequest-Cancelled-1]: adw-referral-request-cancelled-1.html
[CareConnect-Patient-1]: careconnect-patient-1.html
[CareConnect-ADW-Practitioner-1]: careconnect-adw-practitioner-1.html
[ADW-Lead-Clinician-Practitioner-1]: careconnect-adw-practitioner-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-ADW-Encounter-1]: careconnect-adw-encounter-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-Location-1]: careconnect-location-1.html


[MessageHeader.timestamp (ADW Message Sent Time)]: adw-withdrawal-notice-message-header-1-dict.html#MessageHeader.ADW%20Message%20Sent%20Time
[Patient.identifier.value (NHS Number)]: careconnect-patient-1-dict.html#Patient.identifier.value
[Patient.identifier.nhsNumberVerificationStatus]: extension-careconnect-nhsnumberverificationstatus-1-dict.html#Extension.valueCodeableConcept
[Patient.identifier (Local Identifier)]: careconnect-patient-1-dict.html#Patient.identifier.value
[Patient.name.family]: careconnect-patient-1-dict.html#Patient.name.family
[Patient.name.given]: careconnect-patient-1-dict.html#Patient.name.given
[Patient.birthDate]: careconnect-patient-1-dict.html#Patient.birthDate
[Patient.gender]: careconnect-patient-1-dict.html#Patient.gender
[Patient.address.line]: careconnect-patient-1-dict.html#Patient.address.line
[Patient.address.city]: careconnect-patient-1-dict.html#Patient.address.city
[Patient.address.district]: careconnect-patient-1-dict.html#Patient.address.district
[Patient.address.postalCode]: careconnect-patient-1-dict.html#Patient.address.postalCode
[Organization.identifier.value (ODS Site Code)]: careconnect-organization-1-dict.html#Organization.identifier.value
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Location.name]: careconnect-location-1-dict.html#Location.name
[MessageHeader.event.code(Withdrawal Notice Type)]: adw-withdrawal-notice-message-header-1-dict.html#MessageHeader.event.Withdrawal%20Notice%20Type
[MessageHeader.reason.coding.display]: adw-withdrawal-notice-message-header-1-dict.html#MessageHeader.reason.coding.display
[MessageHeader.reason.text (Other Reason for Withdrawal)]: adw-withdrawal-notice-message-header-1-dict.html#MessageHeader.reason.Other%20Reason%20for%20Withdrawal
[Practitioner.name.family]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.family 
[Practitioner.name.given]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.name.family]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-adw-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-adw-practitioner-1-dict.html#Practitioner.telecom.value
[Organization.identifier.value (ODS Organisation Code)]: careconnect-organization-1-dict.html#Organization.identifier.value
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Organization.name]: careconnect-organization-1-dict.html#Organization.name




----------


### Referencing of profiles for an ADW Withdrawal Notice message bundle.###


The diagram shows the referencing for a typical Withdrawal Notice message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for an Withdrawal Notice](../Profile.ADW-WithdrawalNotice/MessageReferencing4.png)

----------


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html