
The ADW-Message-Bundle-1 bundle resource profile is used in the ADW interfaces as a container to collect the ADW profiles in the following combined order: 

- ADW-AssessmentNotice-Message-Header-1 [ADW-AssessmentNotice-Message-Header-1] 
- ADW-Referral-Request-1 [ADW-Referral-Request-1]
- CareConnect-ADW-Encounter-1 [CareConnect-ADW-Encounter-1]
- CareConnect-ADW-Condition-1 [CareConnect-ADW-Condition-1]
- Careconnect-Patient-1 [CareConnect-Patient-1]
- Careconnect-Practitioner-1 [CareConnect-Practitioner-1]
- CareConnect-Organization-1 [CareConnect-Organization-1]
- CareConnect-Location-1 [CareConnect-Location-1]
- ADW-QuestionnaireResponse-1 [ADW-QuestionnaireResponse-1]
- ADW-Composition-1 [ADW-Composition-1]


----------

The following example contains a composition resource and has been a .txt extension only to allow correct viewing within a web browser, xml copies are available within the examples folder within this specification.
 
Example of the Assessment Notice Bundle with ADW Data set fields + optional FHIR elements populated [ADW-Message-AssessmentNotice-1-Ex02.txt] 

Note: Only the ADW data set fields are supported by the National Adapter and therefore optional data will not be retained within transformed messages. Optional data in FHIR messages that are "passed through" the adapter will not be removed.  

----------

[ADW-Message-AssessmentNotice-1-Ex02.txt]: ../Chapter.5.Examples/ADW-Message-AssessmentNotice-1-Ex02.txt


###  ADW Data set Mapping for ADW Assessment Notice message bundle. ###


----------

| REQUIRED DATA FIELD                              | FHIR PROFILE ELEMENT                                                |
|--------------------------------------------------|---------------------------------------------------------------------|
| **Assessment Notice**                            |                                                                     |
| Assessment Notice Issued Date                    | [MessageHeader.timestamp (ADW Message Sent Time)]                   |
| ****Patient Identifiers****                      |                                                                     |
| Patient NHS Number                               | [Patient.identifier (NHS Number)]                                   |
| NHS Number Status Indicator                      | [Patient.identifier.type (NHS Number Status Indicator)]                                 |
| Hospital Patient Identifier                      | [Patient.identifier (Hospital Patient Identifier)]                                       |
| ****Patient Name****                             |                                                                     |
| Family Name                                      | [Patient.name.family (Family Name)]                                        |
| First Given Name                                 | [Patient.name.given (First Given Name)]                                   |
| **Patient Birth Date**                           |                                                                     |
| Patient Birth Date                               | [Patient.birthDate (Patient Birth Date)]                            |
| **Patient Stated Gender**                        |                                                                     |
| Patient Stated Gender                            | [Patient.gender (Patient stated gender)]                            |
| **Patient Address**                              |                                                                     |
| Address Line 1                                   | [Patient.address.line]                                              |
| Address Line 2                                   | [Patient.address.line]                                              |
| Address Line 3                                   | [Patient.address.line]                                              |
| Address Line 4                                   | [Patient.address.city]                                              |
| Address Line 5                                   | [Patient.address.district (County)]                                 |
| Postcode                                         | [Patient.address.postalCode]                                        |
| **Patient Contact Details**                      |                                                                     |
| Patient Email Address                            | [Patient.telecom.value (Patient Email Address)]                           |
| Patient Telephone Number                         | [Patient.telecom.value (Patient Telephone no.)]                           |
| **Patient Language Details**                     |                                                                     |
| Patient Language                                 | [Patient.communication.language]                                    |
| Patient Preferred Language                       | [Patient.communication.Patient Preferred language]              |
| Interpreter Required Indicator                   | [Patient.communication.extension-interpreter-required]          |
| **Hospital**                                     |                                                                     |
| Organization Site Code                           | [Organization.identifier (Organization Site Code)]                                        |
| Hospital Name                                    | [Organization.name (Hospital/Local Authority)]                                        |
| Ward Name                                        | [Location.name (Ward)]                                              |
| **Admission Date**                               |                                                                     |
| Admission Date                                   | [Encounter.period.start (Inpatient Stay Period)]                    |
| **Reason for Admission**                         |                                                                     |
| Reason for Admission                             | [Condition.code.text]     |
| **Admission Type**                               |                                                                     |
| Admission Type                                   | [Encounter.priority (Admission priority)]                                                          |
| **Proposed Discharge Date**                      |                                                                     |
| Proposed Discharge Date                          | [Encounter.period.end (Inpatient Stay Period)]                                           |
| **Lead Clinician Name**                          |                                                                     |
| Family Name                                      | [Lead Clinician.name.family (Family Name)]                                      |
| First Given Name                                 | [Lead Clinician.name.given (First Given Name)]                                             |
| **Hospital Liaison Name**                        |                                                                     |
| Family Name                                      | [Practitioner.name.family (Family Name - Hospital Liaison)]                                 |
| First Given Name                                 | [Practitioner.name.given (First Given Name - Hospital Liaison)]                               |
| **Hospital Liaison Contact Details**             |                                                                     |
| Hospital Liaison Email Address                   | [Practitioner.telecom.value (Hospital Liaison Email)]                                  |
| Hospital Liaison Telephone Number                | [Practitioner.telecom.value (Hospital Liaison Telephone no.)]                          |
| **Carer Name**                        |                                                                     |
| Family Name                                      | [Patient.contact.name.family (Family Name - Carer)]                                          |
| First Given Name                                 | [Patient.contact.name.given (First Given Name - Carer)]                                     |
| **Carer Contact Details**                        |                                                                     |
| Carer Email Address                              | [Patient.contact.telecom.value (Carer Email)]                                  |
| Carer Telephone Number                           | [Patient.contact.telecom.value (Carer Telephone no.)]                                              |
| **Assessment Notice Consultation Status**        |                                                                     |
| Assessment Notice Patient Consultation Indicator | [QuestionnaireResponse.group.question.answer.valueCoding (Patient Consultation)]                |
| Assessment Notice Carer Consultation Indicator   | [QuestionnaireResponse.group.question.answer.valueCoding (Carer Consultation)]                  |
| **Assessment Notice Consent Status**             |                                                                     |
| Assessment Notice Patient Consent Indicator      | [QuestionnaireResponse.group.question.answer.valueCoding (Patient Consent Result)]              |
| Assessment Notice Third Party Consent Response   | [QuestionnaireResponse.group.question.answer.valueCoding (Third Party Consent Result)]          |
| **NHS CHC Assessment**                           |                                                                     |
| NHS CHC Assessment Considered Indicator          | [QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Assessment Considered Indicator)] |
| CHC Assessment Considered Result                 | [QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Considered Result)]            |
| **Safeguarding Indicator**                       |                                                                     |
| Safeguarding Indicator                           | [QuestionnaireResponse.group.question.answer.valueCoding (Safeguarding Issues)]                 |
| **Local Authority**                              |                                                                     |
| Organization Site Code                           | [Organization.identifier (Organization Site Code)]                                        |
| Local Authority Name                             | [Organization.name (Hospital/Local Authority)]                                        |
| Social Services Team                             | [Organization.name (Social Services' team)]                                             |


[ADW-AssessmentNotice-Message-Header-1]: adw-assessment-notice-message-header-1.html
[ADW-Referral-Request-1]: adw-referral-request-1.html
[CareConnect-Patient-1]: careconnect-patient-1.html
[CareConnect-Practitioner-1]: careconnect-practitioner-1.html
[CareConnect-Organization-1]: CareConnect-Organization-1.html
[CareConnect-ADW-Encounter-1]: CareConnect-ADW-Encounter-1.html
[ADW-QuestionnaireResponse-1]: adw-questionnaire-response-1.html
[ADW-Composition-1]: adw-composition-1.html
[CareConnect-Location-1]: careconnect-location-1.html
[CareConnect-ADW-Condition-1]: CareConnect-ADW-Condition-1.html



[MessageHeader.timestamp (ADW Message Sent Time)]: adw-assessment-notice-message-header-1-dict.html#MessageHeader.ADW%20Message%20Sent%20Time
[Patient.identifier (NHS Number)]: careconnect-patient-1-dict.html#Patient.NHS%20Number
[Patient.identifier.type (NHS Number Status Indicator)]: careconnect-patient-1-dict.html#Patient.identifier.NHS%20Number%20Status%20Indicator  
[Patient.identifier (Hospital Patient Identifier)]: careconnect-patient-1-dict.html#Patient.Hospital%20Patient%20Identifier 
[Patient.name.family (Family Name)]: careconnect-patient-1-dict.html#Patient.name.Family%20name
[Patient.name.given (First Given Name)]: careconnect-patient-1-dict.html#Patient.name.First%20given%20name
[Patient.birthDate (Patient Birth Date)]: careconnect-patient-1-dict.html#Patient.Patient%20Birth%20Date
[Patient.gender (Patient stated gender)]: careconnect-patient-1-dict.html#Patient.Patient%20stated%20gender
[Patient.address.line]: careconnect-patient-1-dict.html#Patient.address.line
[Patient.address.city]: careconnect-patient-1-dict.html#Patient.address.city
[Patient.address.district (County)]: careconnect-patient-1-dict.html#Patient.address.County
[Patient.address.postalCode]: careconnect-patient-1-dict.html#Patient.address.postalCode
[Patient.telecom.value (Patient Email Address)]: careconnect-patient-1-dict.html#Patient.telecom.Patient%20Email%20address%20string  
[Patient.telecom.value (Patient Telephone no.)]: careconnect-patient-1-dict.html#Patient.telecom.Patient%20Telephone%20number%20string
[Patient.communication.language]: careconnect-patient-1-dict.html#Patient.communication.language
[Patient.communication.Patient Preferred language]:  careconnect-patient-1-dict.html#Patient.communication.Patient%20Preferred%20language
[Patient.communication.extension-interpreter-required]: careconnect-patient-1-dict.html#Patient.communication.Interpreter%20Required%20Indicator
[Organization.identifier (Organization Site Code)]: CareConnect-Organization-1-dict.html#Organization.Organization%20Site%20Code
[Organization.name (Hospital/Local Authority)]: CareConnect-Organization-1-dict.html#Organization.Hospital%20or%20Local%20Authority%20Name
[Location.name (Ward)]: careconnect-location-1-dict.html#Location.Ward%20name
[Encounter.period.start (Inpatient Stay Period)]: CareConnect-ADW-Encounter-1-dict.html#Encounter.period.start
[Encounter.period.end (Inpatient Stay Period)]: CareConnect-ADW-Encounter-1-dict.html#Encounter.period.end
[Condition.code.text]: careconnect-adw-condition-1-dict.html#Condition.code.text
[Encounter.priority (Admission priority)]: CareConnect-ADW-Encounter-1-dict.html#Encounter.Admission%20priority
[Lead Clinician.name.family (Family Name)]: careconnect-practitioner-1-dict.html#Practitioner.name.Family%20name 
[Lead Clinician.name.given (First Given Name)]: careconnect-practitioner-1-dict.html#Practitioner.name.First%20given%20name
[Practitioner.name.family (Family Name - Hospital Liaison)]: careconnect-practitioner-1-dict.html#Practitioner.name.Family%20name
[Practitioner.name.given (First Given Name - Hospital Liaison)]: careconnect-practitioner-1-dict.html#Practitioner.name.First%20given%20name
[Practitioner.telecom.value (Hospital Liaison Email)]: careconnect-practitioner-1-dict.html#Practitioner.telecom.Practitioner%20Email%20address%20string
[Practitioner.telecom.value (Hospital Liaison Telephone no.)]: careconnect-practitioner-1-dict.html#Practitioner.telecom.Practitioner%20Telephone%20number%20string
[QuestionnaireResponse.group.question.answer.valueCoding (Carer Consultation)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Carer%20Consultation
[QuestionnaireResponse.group.question.answer.valueCoding (Patient Consultation)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Patient%20Consultation
[QuestionnaireResponse.group.question.answer.valueCoding (Patient Consent Result)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Patient%20Consent
[QuestionnaireResponse.group.question.answer.valueCoding (Third Party Consent Result)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Third%20Party%20Consent
[QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Assessment Considered Indicator)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.NHS%20CHC%20Assessment%20Considered%20Indicator
[QuestionnaireResponse.group.question.answer.valueCoding (NHS CHC Considered Result)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.NHS%20CHC%20Considered%20Result
[QuestionnaireResponse.group.question.answer.valueCoding (Safeguarding Issues)]: adw-questionnaire-response-1-dict.html#QuestionnaireResponse.group.question.answer.Safe%20Guarding%20Issues
[identifier (Local Authority - ODS Organisation Code)]: CareConnect-Organization-1-dict.html#Organization.ODS%20Organisation%20Code
[Organization.name (Hospital/Local Authority)]: CareConnect-Organization-1-dict.html#Organization.Hospital%20or%20Local%20Authority%20Name
[Organization.name (Social Services' team)]: CareConnect-Organization-1-dict.html#Organization.Social%20Services%20team
[Patient.contact.name.family (Family Name - Carer)]: careconnect-patient-1-dict.html#Patient.contact.name.Family%20name
[Patient.contact.name.given (First Given Name - Carer)]: careconnect-patient-1-dict.html#Patient.contact.name.First%20given%20name
[Patient.contact.telecom.value (Carer Email)]: careconnect-patient-1-dict.html#Patient.contact.telecom.Carer%20Email%20address%20string
[Patient.contact.telecom.value (Carer Telephone no.)]: careconnect-patient-1-dict.html#Patient.contact.telecom.Carer%20Telephone%20number%20string

----------


###  Profile Referencing Diagram for an Assessment Notice #

The FHIR profiles in the message are referenced in the XML instance instead of being contained. 

This means only one instance is required for each instance of the profile.

The diagram shows the referencing for a typical Assessment Notice message. It is intended for illustrative purposes only. The diagram can be viewed here:

[Profile Referencing Diagram for an Assessment Notice](../Profile.ADW-AssessmentNotice/MessageReferencing4.png)


**Further Information**

For more information about message profiles visit the [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on [FHIR website].

[Profiling FHIR]: http://hl7.org/fhir/profiling.html
[FHIR website]: http://hl7.org/fhir/index.html
[Base Resource Definitions]: http://hl7.org/fhir/resource.html




