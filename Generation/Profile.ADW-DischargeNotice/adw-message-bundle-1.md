
The ADW-Message-Bundle-1 bundle is used in ADW as a container to collect the ADW profiles listed below:- 

- ADW-DischargeNotice-MessageHeader-1 [ADW-DischargeNotice-MessageHeader-1]
- ADW-Discharge-ReferralRequest-1 [ADW-Discharge-ReferralRequest-1]
- CareConnect-ADW-Encounter-1 [CareConnect-ADW-Encounter-1]
- CareConnect-Patient-1 [CareConnect-Patient-1]
- CareConnect-Practitioner-1 [CareConnect-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]
- ADW-Discharge-QuestionnaireResponse-1 [ADW-Discharge-QuestionnaireResponse-1]
- ADW-Condition-1 [ADW-Condition-1]

----------

The following example has been saved as a .txt file only to allow correct viewing within a web browser; xml copies are available in the examples folder within this specification.

An instance of a DocumentReference and a Binary resource have been added to the end of this Discharge bundle to illustrate how a supporting document, in this case a pdf, could be attached to the message.

Example of the Discharge Notice Bundle for viewing in a web browser [ADW-Message-Discharge-Notice-Bundle-1-Example-2.txt] 


[ADW-Message-Discharge-Notice-Bundle-1-Example-2.txt]: ../Chapter.5.Examples/ADW-Message-Discharge-Notice-Bundle-1-Example-2.txt

###  ADW Data set Mapping for ADW Discharge Notice message bundle. ###

----------

| REQUIRED DATA FIELD                          | FHIR PROFILE ELEMENT                             |
|----------------------------------------------|--------------------------------------------------|
| **Discharge Notice**                         |                                                  |
| Discharge Notice Issued Date                 | [MessageHeader.timestamp (ADW Message Sent Time)]                |
| **Patient Identifiers**                      |                                                  |
| Patient NHS Number                           | [Patient.nhsNumber]                         |
| NHS Number Status Indicator                  |[Patient.identifier.nhsNumberVerificationStatus]                                    |
| Hospital Patient Identifier                  | [Patient.localIdentifier]                                   |
| **Patient Name**                             |                                                  |
| Family Name                                  |[Patient.name.family]                                       |
| First Given Name                             |[Patient.name.given]                                       |
| **Patient Birth Date**                       |                                                  |
| Patient Birth Date                           |[Patient.birthDate]                                         |
| **Person Stated Gender**                     |                                                  |
| Patient Stated Gender                         |[Patient.gender]                                           |
| **Patient Address**                          |                                                  |
| Address Line 1                               |[Patient.address.line]                                      |
| Address Line 2                               |[Patient.address.line]                                     |
| Address Line 3                               |[Patient.address.line]                                     |
| Address Line 4                               |[Patient.address.city]                                     |
| Address Line 5                               |[Patient.address.district]                                     |
| Postcode                                     |[Patient.address.postalCode]                               
| **Hospital**                                 |                                                  |
| Organization Site Code                       |[Organization.identifier (Organisation Site Code)]                                         |
| Hospital Name                                |[Organization.name]                                              |
| Ward Name                                    |[Location.name]                                              |
| **Proposed Discharge Date**                  |                                                  |
| Proposed Discharge Date                      |[Encounter.period.end]                                       |
| **Discharge Date Informed Status**           |                                                  |
| Discharge Notice Patient Consulted Indicator | [QuestionnaireResponse.group.Patient Consultation]                                    |
| Discharge Notice Carer Consulted Indicator   | [QuestionnaireResponse.group.Carer Consultation]    |
| **Lead Clinician Name**                      |                                                  |
| Family Name                                  | [Practitioner.name.family]                                      |
| First Given Name                             | [Practitioner.name.given]                                      |
| **Hospital Liaison Name**                    |                                                  |
| Family Name                                  | [Practitioner.name.family]                             |
| First Given Name                             | [Practitioner.name.given]                             |
| **Hospital Liaison Contact Details**         |                                                  |
| Hospital Liaison Email Address               | [Practitioner.telecom.value]                                        |
| Hospital Liaison Telephone Number            | [Practitioner.telecom.value]                                |
| **Carer Name**                               |                                                                   |
| Family Name                                  | [Patient.contact.name.family]                                        |
| First Given Name                             | [Patient.contact.name.given]                                      |
| **Carer Contact Details**                    |                                                                   |
| Carer Email Address                          | [Patient.contact.telecom.value]                                                           |
| Carer Telephone Number                       | [Patient.contact.telecom.value]                                          |
| **Local Authority**                          |                                                  |
| Organization Code                            | [Organization.identifier (ODS Organisation Code)]                                         |
| Local Authority Name                         | [Organization.name]                                             |
| Social Services Team                         | [Organization.name]                                             |


----------


###  Profile Referencing Diagram for a Discharge Notice #

The FHIR profiles in the message are referenced in the XML instance instead of being contained. 

This means only one instance is required for each instance of the profile.

The diagram shows the referencing for a typical Discharge Notice message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for a Discharge Notice](../Profile.ADW-DischargeNotice/DiagramDNRefs.pdf)



[ADW-DischargeNotice-MessageHeader-1]: adw-dischargenotice-messageheader-1.html
[ADW-Discharge-ReferralRequest-1]: ADW-Discharge-ReferralRequest-1.html
[CareConnect-Patient-1]: careconnect-patient-1.html
[CareConnect-Practitioner-1]: careconnect-practitioner-1.html
[ADW-Lead-Clinician-Practitioner-1]: careconnect-practitioner-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[ADW-Discharge-QuestionnaireResponse-1]: adw-discharge-questionnaireresponse-1.html
[CareConnect-ADW-Encounter-1]: careconnect-adw-encounter-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-Location-1]: careconnect-location-1.html
[ADW-Condition-1]: adw-condition-1.html



[MessageHeader.timestamp (ADW Message Sent Time)]: adw-dischargenotice-messageheader-1-dict.html#MessageHeader.ADW%20Message%20Sent%20Time
[Patient.nhsNumber]: careconnect-patient-1-dict.html#Patient.nhsNumber
[Patient.localIdentifier]: careconnect-patient-1-dict.html#Patient.localIdentifier
[Patient.identifier.nhsNumberVerificationStatus]: careconnect-patient-1-dict.html#Patient.identifier.nhsNumberVerificationStatus
[Patient.name.family]: careconnect-patient-1-dict.html#Patient.name.family
[Patient.name.given]: careconnect-patient-1-dict.html#Patient.name.given
[Patient.birthDate]: careconnect-patient-1-dict.html#Patient.birthDate
[Patient.gender]: careconnect-patient-1-dict.html#Patient.gender
[Patient.address.line]: careconnect-patient-1-dict.html#Patient.address.line
[Patient.address.city]: careconnect-patient-1-dict.html#Patient.address.city
[Patient.address.district]: careconnect-patient-1-dict.html#Patient.address.district
[Patient.address.postalCode]: careconnect-patient-1-dict.html#Patient.address.postalCode
[Organization.identifier (Organisation Site Code)]: careconnect-organization-1-dict.html#Organization.ODS%20Site%20Code
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Location.name]: careconnect-location-1-dict.html#Location.name
[Encounter.period.end]: careconnect-adw-encounter-1-dict.html#Encounter.period.end
[QuestionnaireResponse.group.Patient Consultation]: adw-discharge-questionnaireresponse-1-dict.html#QuestionnaireResponse.group.Patient%20Consultation
[QuestionnaireResponse.group.Carer Consultation]: adw-discharge-questionnaireresponse-1-dict.html#QuestionnaireResponse.group.Carer%20Consultation
[Practitioner.name.family]: careconnect-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.name.family]: careconnect-practitioner-1-dict.html#Practitioner.name.family
[Practitioner.name.given]: careconnect-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-practitioner-1-dict.html#Practitioner.telecom.value
[Practitioner.telecom.value]: careconnect-practitioner-1-dict.html#Practitioner.telecom.value
[Organization.identifier.value (ODS Organisation Code)]: careconnect-organization-1-dict.html#Organization.identifier.value
[Organization.identifier (ODS Organisation Code)]: careconnect-organization-1-dict.html#Organization.ODS%20Organisation%20Code 
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Organization.name]: careconnect-organization-1-dict.html#Organization.name
[Patient.contact.name.family]: careconnect-patient-1-dict.html#Patient.contact.name.family
[Patient.contact.name.given]: careconnect-patient-1-dict.html#Patient.contact.name.given
[Patient.contact.telecom.value]: careconnect-patient-1-dict.html#Patient.contact.telecom.value
[Patient.contact.telecom.value]: careconnect-patient-1-dict.html#Patient.contact.telecom.value

----------


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on the [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html
