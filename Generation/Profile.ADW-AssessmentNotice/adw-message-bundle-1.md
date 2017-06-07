
The ADW-Message-Bundle-1 bundle resource profile is used in the ADW interfaces as a container to collect the ADW profiles in the following combined order: 

- ADW-AssessmentNotice-Message-Header-1 [ADW-AssessmentNotice-Message-Header-1] 
- ADW-Referral-Request-1 [ADW-Referral-Request-1]
- CareConnect-ADW-Encounter-1 [CareConnect-ADW-Encounter-1]
- ADW-Condition-1 [ADW-Condition-1]
- Careconnect-Patient-1 [CareConnect-Patient-1]
- Careconnect-Practitioner-1 [CareConnect-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]
- ADW-QuestionnaireResponse-1 [ADW-QuestionnaireResponse-1]
- ADW-Composition-1 [ADW-Composition-1]


----------

The following example has been saved as a .txt file only to allow correct viewing within a web browser; xml copies are available in the examples folder within this specification.
 
Example of the Assessment Notice Bundle for viewing in a web browser [ADW-Message-Assessment-Notice-Bundle-1-Example-2.txt] 

 

----------

[ADW-Message-Assessment-Notice-Bundle-1-Example-2.txt]: ../Chapter.5.Examples/ADW-Message-Assessment-Notice-Bundle-1-Example-2.txt


###  ADW Data set Mapping for ADW Assessment Notice message bundle. ###


----------

Note that for some sliced elements and extensions within CareConnect profiles, it is not possible to link to the exact element in this mapping table.


| REQUIRED DATA FIELD                              | FHIR PROFILE ELEMENT                                                |
|--------------------------------------------------|---------------------------------------------------------------------|
| **Assessment Notice**                            |                                                                     |
| Assessment Notice Issued Date                    | [MessageHeader.timestamp (ADW Message Sent Time)]                   |
| ****Patient Identifiers****                      |                                                                     |
| Patient NHS Number                               | [Patient.identifier.value (NHS Number)]                                   |
| NHS Number Status Indicator                      | [Patient.identifier.nhsNumberVerificationStatus]   |
| Hospital Patient Identifier                      | [Patient.identifier.value (Local Identifier)]                                       |
| ****Patient Name****                             |                                                                     |
| Family Name                                      | [Patient.name.family]                                        |
| First Given Name                                 | [Patient.name.given]                                   |
| **Patient Birth Date**                           |                                                                     |
| Patient Birth Date                               | [Patient.birthDate]                            |
| **Patient Stated Gender**                        |                                                                     |
| Patient Stated Gender                            | [Patient.gender]                            |
| **Patient Address**                              |                                                                     |
| Address Line 1                                   | [Patient.address.line]                                              |
| Address Line 2                                   | [Patient.address.line]                                              |
| Address Line 3                                   | [Patient.address.line]                                              |
| Address Line 4                                   | [Patient.address.city]                                              |
| Address Line 5                                   | [Patient.address.district]                                 |
| Postcode                                         | [Patient.address.postalCode]                                        |
| **Patient Contact Details**                      |                                                                     |
| Patient Email Address                            | [Patient.telecom.value]                           |
| Patient Telephone Number                         | [Patient.telecom.value]                           |
| **Patient Language Details**                     |                                                                     |
| Patient Language                                 | [Patient.nhsCommunication.extension (language)]                                    |
| Patient Preferred Language                       | [Patient.nhsCommunication.extension (preferred)]              |
| Interpreter Required Indicator                   | [Patient.nhsCommunication.extension (interpreterRequired)]          |
| **Hospital**                                     |                                                                     |
| Organisation Site Code                           | [Organization.identifier.value (Organisation Site Code)]                                        |
| Hospital Name                                    | [Organization.name]                                        |
| Ward Name                                        | [Location.name]                                              |
| **Admission Date**                               |                                                                     |
| Admission Date                                   | [Encounter.period.start]                    |
| **Reason for Admission**                         |                                                                     |
| Reason for Admission                             | [Condition.code.text]     |
| **Admission Type**                               |                                                                     |
| Admission Type                                   | [Encounter.priority.coding.display]                                                          |
| **Proposed Discharge Date**                      |                                                                     |
| Proposed Discharge Date                          | [Encounter.period.end]                                           |
| **Lead Clinician Name**                          |                                                                     |
| Family Name                                      | [Practitioner.name.family]                                      |
| First Given Name                                 | [Practitioner.name.given]                                             |
| **Hospital Liaison Name**                        |                                                                     |
| Family Name                                      | [Practitioner.name.family]                                 |
| First Given Name                                 | [Practitioner.name.given]                               |
| **Hospital Liaison Contact Details**             |                                                                     |
| Hospital Liaison Email Address                   | [Practitioner.telecom.value]                                  |
| Hospital Liaison Telephone Number                | [Practitioner.telecom.value]                          |
| **Carer Name**                        |                                                                     |
| Family Name                                      | [Patient.contact.name.family]                                          |
| First Given Name                                 | [Patient.contact.name.given]                                     |
| **Carer Contact Details**                        |                                                                     |
| Carer Email Address                              | [Patient.contact.telecom.value]                                  |
| Carer Telephone Number                           | [Patient.contact.telecom.value]                                              |
| **Assessment Notice Consultation Status**        |                                                                     |
| Assessment Notice Patient Consultation Indicator | [QuestionnaireResponse.group.question.answer.valueCoding (Patient Consultation)]                |
| Assessment Notice Carer Consultation Indicator   | [QuestionnaireResponse.group.question.answer.valueCoding (Carer Consultation)]                  |
| **Assessment Notice Consent Status**             |                                                                     |
| Assessment Notice Patient Consent Indicator      | [QuestionnaireResponse.group.question.answer.valueCoding (Patient Consent)]              |
| Assessment Notice Third Party Consent Source   | [QuestionnaireResponse.group.question.answer.valueCoding (Third Party Consent Source)]          |
| **NHS CHC Assessment**                           |                                                                     |
| NHS CHC Assessment Considered Indicator          | [QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Assessment Considered Indicator)] |
| CHC Assessment Considered Result                 | [QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Considered Result)]            |
| **Safeguarding Indicator**                       |                                                                     |
| Safeguarding Indicator                           | [QuestionnaireResponse.group.question.answer.valueCoding (Safeguarding Issues)]                 |
| **Local Authority**                              |                                                                     |
| Organisation ODS Code                           | [Organization.identifier.value (ODS Organisation Code)]                                        |
| Local Authority Name                             | [Organization.name]                                        |
| Social Services Team                             | [Organization.name]                                             |


[ADW-AssessmentNotice-Message-Header-1]: adw-assessment-notice-message-header-1.html
[ADW-Referral-Request-1]: adw-referral-request-1.html
[CareConnect-Patient-1]: careconnect-patient-1.html
[CareConnect-Practitioner-1]: careconnect-practitioner-1.html
[CareConnect-Organization-1]: careconnect-organization-1.html
[CareConnect-ADW-Encounter-1]: careconnect-adw-encounter-1.html
[ADW-QuestionnaireResponse-1]: adw-questionnaire-response-1.html
[ADW-Composition-1]: adw-composition-1.html
[CareConnect-Location-1]: careconnect-location-1.html
[ADW-Condition-1]: adw-condition-1.html



[MessageHeader.timestamp (ADW Message Sent Time)]: adw-assessment-notice-message-header-1-dict.html#MessageHeader.ADW%20Message%20Sent%20Time
[Patient.identifier.value (NHS Number)]: careconnect-patient-1-dict.html#Patient.identifier.value
[Patient.identifier.nhsNumberVerificationStatus]: extension-careconnect-nhsnumberverificationstatus-1-dict.html#Extension.valueCodeableConcept  
[Patient.identifier.value (Local Identifier)]: careconnect-patient-1-dict.html#Patient.identifier.value 
[Patient.name.family]: careconnect-patient-1-dict.html#Patient.name.family
[Patient.name.given]: careconnect-patient-1-dict.html#Patient.name.given
[Patient.birthDate]: careconnect-patient-1-dict.html#Patient.birthDate
[Patient.gender]: careconnect-patient-1-dict.html#Patient.gender
[Patient.address.line]: careconnect-patient-1-dict.html#Patient.address.line
[Patient.address.city]: careconnect-patient-1-dict.html#Patient.address.city
[Patient.address.district]: careconnect-patient-1-dict.html#Patient.address.district
[Patient.address.postalCode]: careconnect-patient-1-dict.html#Patient.address.postalCode
[Patient.telecom.value]: careconnect-patient-1-dict.html#Patient.telecom.value  
[Patient.nhsCommunication.extension (language)]: extension-careconnect-nhscommunication-1-dict.html#Extension.extension.valueCodeableConcept
[Patient.nhsCommunication.extension (preferred)]: extension-careconnect-nhscommunication-1-dict.html#Extension.extension.valueBoolean
[Patient.nhscommunication.extension (interpreterRequired)]: extension-careconnect-nhscommunication-1-dict.html#Extension.interpreterRequired
[Organization.identifier.value (Organisation Site Code)]: CareConnect-Organization-1-dict.html#Organization.identifier.value
[Organization.name]: CareConnect-Organization-1-dict.html#Organization.name
[Location.name]: careconnect-location-1-dict.html#Location.name
[Encounter.period.start]: CareConnect-ADW-Encounter-1-dict.html#Encounter.period.start
[Encounter.period.end]: CareConnect-ADW-Encounter-1-dict.html#Encounter.period.end
[Condition.code.text]: adw-condition-1-dict.html#Condition.code.text
[Encounter.priority.coding.display]: CareConnect-ADW-Encounter-1-dict.html#Encounter.priority.coding.display
[Practitioner.name.family]: careconnect-practitioner-1-dict.html#Practitioner.name.family 
[Practitioner.name.given]: careconnect-practitioner-1-dict.html#Practitioner.name.given
[Practitioner.telecom.value]: careconnect-practitioner-1-dict.html#Practitioner.telecom.value
[QuestionnaireResponse.group.question.answer.valueCoding (Carer Consultation)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Carer%20Consultation
[QuestionnaireResponse.group.question.answer.valueCoding (Patient Consultation)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Patient%20Consultation
[QuestionnaireResponse.group.question.answer.valueCoding (Patient Consent)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Patient%20Consent
[QuestionnaireResponse.group.question.answer.valueCoding (Third Party Consent Source)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Third%20Party%20Consent%20Source
[QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Assessment Considered Indicator)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.NHS%20CHC%20Assessment%20Considered%20Indicator
[QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Considered Result)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.NHS%20CHC%20Considered%20Result
[QuestionnaireResponse.group.question.answer.valueCoding (Safeguarding Issues)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Safeguarding%20Issues
[Organization.identifier.value (ODS Organisation Code)]: CareConnect-Organization-1-dict.html#Organization.identifier.value
[Patient.contact.name.family]: careconnect-patient-1-dict.html#Patient.contact.name.family
[Patient.contact.name.given]: careconnect-patient-1-dict.html#Patient.contact.name.given
[Patient.contact.telecom.value]: careconnect-patient-1-dict.html#Patient.contact.telecom.value

----------


###  Profile Referencing Diagram for an Assessment Notice #

The FHIR profiles in the message are referenced in the XML instance instead of being contained. 

This means only one instance is required for each instance of the profile.

The diagram shows the referencing for a typical Assessment Notice message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for an Assessment Notice](../Profile.ADW-AssessmentNotice/MessageReferencing4.png)


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html




