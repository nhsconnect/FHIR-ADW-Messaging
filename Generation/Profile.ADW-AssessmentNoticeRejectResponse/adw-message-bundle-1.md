
The ADW-Message-Bundle-1 bundle resource profile is used in the ADW interfaces as a container to collect the ADW profiles in the following combined order: 

- ADW-AssessmentNoticeRejectResponse-Message-Header-1 [ADW-AssessmentNoticeRejectResponse-Message-Header-1]
- ADW-ReferralRequest-Rejected-1 [ADW-ReferralRequest-Rejected-1]
- Careconnect-Patient-1 [CareConnect-Patient-1]
- Careconnect-Practitioner-1 [CareConnect-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]

----------


###  ADW Data set Mapping for ADW Assessment Notice Reject Response message bundle. ###


----------

Note that for sliced elements and extensions within CareConnect profiles, it is not possible to link to the exact sliced element in this mapping table.


| REQUIRED DATA FIELD                      | FHIR PROFILE ELEMENT                              |
|------------------------------------------|---------------------------------------------------|
| **Assessment Notice Reject Response**    |                                                   |
| Notice Receipt issued date               | [MessageHeader.timestamp (ADW Reject Response Message Sent Time)]                        |
| Notice Type                              | [MessageHeader.event.code (Reject Response Type)]                 |
| Response Type                            | [ReferralRequest.status]                                     |
| Response Details                         | [MessageHeader.reason.text (Reject Reason)]                                       |
| **Patient Identifiers**                  |                                                   |
| Patient NHS Number                       | [Patient.identifier.value (NHS Number)]                          |
| Hospital Patient Identifier              | [Patient.identifier (Local Identifier)]            |
| **Patient Name**                         |                                                  |
| Family Name                              | [Patient.name.family]                                     |
| First Given Name                         | [Patient.name.given]                                       |
| **Patient Birth Date**                   |                                                  |
| Patient Birth Date                       | [Patient.birthDate]                                      |
| **Person Stated Gender**                 |                                                  |
| Patient Stated Gender                    | [Patient.gender]                                         |
| **Hospital**                             |                                                  |
| Organization Site Code                   | [Organization.identifier.value (ODS Site Code)]             |
| Hospital Name                            | [Organization.name]                                |
| Ward Name                                | [Location.name]                                     |
| **Hospital Liaison Name**                |                                                  |
| Family Name                              | [Practitioner.name.family]                                  |
| First Given Name                         | [Practitioner.name.given]                         |
| **Hospital Liaison Contact Details**     |                                                  |
| Hospital Liaison Email Address           | [Practitioner.telecom.value]               |
| Hospital Liaison Telephone Number        | [Practitioner.telecom.value]                            |
| **Local Authority**                      |                                                  |
| Organisation ODS Code                    | [Organization.identifier.value (ODS Organisation Code)]                                     |
| Local Authority Name                     | [Organization.name]                         |
| Social Services Team                     | [Organization.name] 
| **Local Authority Contact Name**         |                                                   |
| Family Name                              | [Practitioner.name.family]                                  |
| First Given Name                         | [Practitioner.name.given]                                  |
| **Local Authority Contact Details**      |                                                   |
| Local Authority Contact Email Address    | [Practitioner.telecom.value]                            |
| Local Authority Contact Telephone Number | [Practitioner.telecom.value]                    |



[ADW-AssessmentNoticeRejectResponse-Message-Header-1]: adw-assessment-notice-reject-response-message-header-1.html
[ADW-ReferralRequest-Rejected-1]: adw-referral-request-rejected-1.html
[careconnect-patient-1]: careconnect-patient-1.html
[careconnect-practitioner-1]: careconnect-practitioner-1.html
[CareConnect-Organization-1]: CareConnect-Organization-1.html
[CareConnect-ADW-Encounter-1]: careconnect-adw-encounter-1.html
[CareConnect-Organization-1]: CareConnect-Organization-1.html
[careconnect-location-1]: careconnect-location-1.html


[MessageHeader.timestamp (ADW Reject Response Message Sent Time)]: adw-assessment-notice-reject-response-message-header-1-dict.html#MessageHeader.ADW%20Reject%20Response%20Message%20Sent%20Time
[MessageHeader.event.code (Reject Response Type)]: adw-assessment-notice-reject-response-message-header-1-dict.html#MessageHeader.event.Reject%20Response%20Type
[ReferralRequest.status]: adw-referral-request-rejected-1-dict.html#ReferralRequest.The%20Transfer%20Status
[MessageHeader.reason.text (Reject Reason)]: adw-assessment-notice-reject-response-message-header-1-dict.html#MessageHeader.reason.Reject%20Reason%20Details
[Patient.identifier.value (NHS Number)]: careconnect-patient-1-dict.html#Patient.identifier.value
[Patient.identifier (Local Identifier)]: careconnect-patient-1-dict.html#Patient.identifier.value 
[Patient.name.family]: careconnect-patient-1-dict.html#Patient.name.family
[Patient.name.given]: careconnect-patient-1-dict.html#Patient.name.given
[Patient.birthDate]: careconnect-patient-1-dict.html#Patient.birthDate
[Patient.gender]: careconnect-patient-1-dict.html#Patient.gender
[Organization.identifier.value (ODS Site Code)]: CareConnect-Organization-1-dict.html#Organization.identifier.value
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Location.name]: careconnect-location-1-dict.html#Location.name
[Organization.identifier.value (ODS Site Code)]: careconnect-organization-1-dict.html#Organization.identifier.value
[Organization.name]: CareConnect-Organization-1-dict.html#Organization.name
[Practitioner.name.family]: careconnect-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-practitioner-1-dict.html#Practitioner.telecom.value
[Organization.identifier.value (ODS Organisation Code)]: careconnect-organization-1-dict.html#Organization.identifier.value
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Practitioner.name.family]: careconnect-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-practitioner-1-dict.html#Practitioner.telecom.value

----------


### Referencing of profiles for ADW Assessment Notice Reject Response message bundle.###


The diagram shows the referencing for a typical Assessment Notice Reject Response message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for an Assessment Notice Reject Response](../Profile.ADW-AssessmentNoticeRejectResponse/MessageReferencing4.png)

----------


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html
