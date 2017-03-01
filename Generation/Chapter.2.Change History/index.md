# Change History #
### Version: 1.0: Status: RC5 ###
 - All profile urls containing the string http://fhir.nhs.net have this string replaced by https://fhir.nhs.uk  
 - All system urls for valuesets containing the string http://fhir.nhs.net/Valueset have this string replaced by https://fhir.nhs.uk when the url appears as data in the coding.system element.
 - All system urls for valuesets containing the string http://hl7.org/fhir/ValueSet have this string replaced by http://hl7.org/fhir when the url appears as data in the coding.system element.
 - Inserted CareConnect standard profiles as replacements for ADW Patient, Condition, Encounter, Location, Organization and Practitioner. The impact on instances is as follows:-
 - **ADW-Patient-1-0**
 - All labels for elements removed.
 - Patient.identifier slice NHS number renamed to Identifier # 1 [nhsNumber]
 - Identifier slice Identifier # 1 [nhsNumber].use element removed. 
 - Identifier slice Identifier # 1 [nhsNumber].type element removed. 
 - Patient.type (NHS Number Status indicator) changed to extension nhsNumberVerificationStatus in Identifier slice Identifier # 1 [nhsNumber].
 - Patient.identifier slice Hospital Patient Identifier renamed to Identifier slice identifier#2 [other] and fixed value in its system element removed.
 - Patient.name element is sliced into two slices, name # 1 [usual] and name # 2 [other].
 - Patient.name slice name # 1 [usual] has mandatory element name.use 1..1 with fixed value "usual" and fixed valueset NameUse.
 - Patient.telecom element is no longer sliced.
 - Patient.gender valueset renamed from ADW-Person-Stated-Gender-1-0 to CareConnect-AdministrativeGender-1.
 - Patient.contact.relationship valueset changed to CareConnect-PersonRelationshipType-1.
 - Patient.contact.relationship.coding.system has fixed value removed.
 - Patient.contact.relationship.coding.userSelected element removed.
 - Patient.contact.relationship.text element removed.
 - Patient.contact.name changed to mandatory element 1..1.
 - Patient.contact.name.use changed to mandatory element 1..1 with fixed value "usual".
 - Patient.contact.name.period element removed.
 - Patient.contact.name.period.start element removed.
 - Patient.contact.name.period.end element removed.
 - Patient.contact.telecom is not sliced.
 - Patient.contact.telecom.rank element removed.
 - Patient.careProvider reference changed to CareConnect-Organization-1 or CareConnect-Organization-1.
 - Patient.communication element removed and replaced by nhsCommunication extension  
 
### Version: 1.0: Status: RC4 ###
 - Changed values in adw-person-stated-gender-1-0 name and description elements to reflect those in the FHIR valueset at http://hl7.org/fhir/valueset-administrative-gender.html (AdministrativeGender).
 - Changed valueset reference in ADW-Message-AssessmentNotice-1-0-Ex01.xml group.question (Patient Consent) from http://fhir.nhs.net/ValueSet/adw-consultation-status-1-0 to 	http://fhir.nhs.net/ValueSet/adw-patient-consent-status-1-0.
 - Removed red warning text from About page.
 - Amended About page to show October 2015 (latest) version of FHIR.
 - Amended all profile referencing diagrams to reflect design changes from Draft G onwards. 
 - Changed Binding strength in Patient.contact.relationship to Required.
 - Re-worked the maximum xml bundle examples suffixed Ex02.
 - Added in optional identifier.type element for Practitioner, Lead Clinician and Social Services Organization for the Local Identifier.
 - Added explanatory description to Patient.identifier.type (NHS Number) valueset (NHS Number status indicator) to indicate that code and display 08: Trace postponed (baby under six weeks old) is not required.
 - Amended resource names in textual descriptions for Message Headers, Questionnaire Responses, Referral Requests to reflect FHIR naming of these resources.
 - Added labels to Patient.telecom (Patient Contact Details) and Patient.contact.telecom (Carer Contact Details) to reflect Information Standard naming.
 - Replaced profile 'None given' example values with more illustrative and relevant values.
 - Corrected binding strength in Organization.type (including Social Services organization) to read Required.
 - Amended code NA to N/A in valueset at http://fhir.nhs.net/ValueSet/adw-third-party-consent-source-1-0 to reflect Information Standard revision.
 
 **Known Issues**
 
 - Question marks appear after the cardinality entries in the Control label on the dictionary pages. The cardinalities given in these instances are correct; this is a tooling issue which is currently under investigation.
 - There are inconsistencies in some of the descriptions in the dictionary/definition pages for profiles. Where this is the case, the profile tree view page takes precedence. The cause of this is currently under investigation.
 - Xml examples for individual profiles have not been updated.
    
### Version: 1.0: Status: RC3 ###
 - Changed url of ADW-Discharge-Notice-Accept-Response-Message-Header-1-0 to http://fhir.nhs.net/StructureDefinition/adw-discharge-notice-accept-response-message-header-1-0 from http://fhir.nhs.net/StructureDefinition/adw-discharge-notice-agreement-response-message-header-1-0 to make all Accept Notice urls consistent.
 - Amended Profile names for all MessageHeaders, ReferralRequests and QuestionnaireResponses to reflect their url naming.
 - Amended profile textual descriptions to reflect more clearly the nature of profiles in the message.
 - Added 'Where the sender is able to look up the Organisation Site Code, Hospital Name should be derived.' into the description for Organization.name element in Organization profiles to reflect requirements.
 - Amended Patient.identifier across all Patient profiles to make it an optional element rather than mandatory to reflect a revised requirement.
 - Amended ADW-WithdrawalNoticeAcceptResponse/adw-message-bundle-1-0.html to correct three broken links.
 - Added additional value NKC: No Known Carer to ADW Carer Consultation Status valueset.
 - Corrected ADW-Message-AssessmentNotice-1-0-Ex01.xml to show reference to http://fhir.nhs.net/ValueSet/adw-carerconsultation-status-1-0 valueset for patient's carer consultation in QuestionnaireResponse entry.
 - Amended Admission Date and Proposed Discharge Date values to show date, not dateTime, in Assessment and Discharge notice bundle examples to reflect requirements.

**Known Issues**
 
 - Question marks appear after the cardinality entries in the Control label on the dictionary pages. The cardinalities given in these instances are correct; this is a tooling issue which is currently under investigation.
 - There are inconsistencies in some of the descriptions in the dictionary/definition pages for profiles. Where this is the case, the profile tree view page takes precedence. The cause of this is currently under investigation.
 - Xml examples for individual profiles and maximal bundle xml examples (suffixed Ex02) have not been updated; the latter will be revised in RC3.
 - Valuesets have not been fully reviewed and this will happen for the next Release Candidate.
 
### Version: 1.0: Status: RC2 ###
 - Made Patient.address optional across all messages and added in text to its description to outline that it should be mandatory in all Notices, but optional in all Responses.
 - Made Patient.type (NHS Number Status Indicator) optional across all messages to reflect requirements.
 - Amended the MessageHeader.receiver element in the Assessment notice minimum dataset bundle xml example to contain the Social Services' community team to reflect requirements.
 - Amended the ReferralRequest.recipient element in the Discharge and Withdrawal notice minimum dataset bundle xml examples to contain the Social Services' community team rather than the Local Authority to maintain consistency across notice bundles.
 - The incorrect reference to the Local Authority Contact in ADW-Message-AssessmentNotice-1-0-Ex01 xml example has been removed.
 - Amended label for MessageHeader.responsible element across all messages to show Lead Clinician for Notices and Local Authority Organisation for all Responses.
 - Reinstated MessageHeader.responsible element for all Response minimum dataset bundle xml examples to ensure data about the responsible Local Authority organisation can be sent.
 - Corrected profile uri for ADW-Organization-1-0 from profile value="http://fhir.nhs.net/StructureDefinition/adw-organisation-1-0" to profile value="http://fhir.nhs.net/StructureDefinition/adw-organization-1-0". 
 - Corrected profile uri for ADW-Organization-Social-Services-Organization-1-0 from profile value="http://fhir.nhs.net/StructureDefinition/adw-social-services-team-organisation-1-0" to profile value="http://fhir.nhs.net/StructureDefinition/adw-social-services-team-organization-1-0".
 - Made ADW-Organization-Social-Services-Organization-1-0.partOf element mandatory in order to carry the Local Authority organisation.
 - Amended ReferralRequest.recipient element to reference ADW-Organization-Social-Services-Organization-1-0 across all messages.
 - Amended MessageHeader.receiver element to reference only ADW-Organization-Social-Services-Organization-1-0 for all Notice profiles.
 - Amended MessageHeader.receiver element to reference only ADW-Practitioner-1-0 for all Response profiles.
 - Reinstated Encounter.serviceProvider element in all minimum dataset xml bundles to reflect that it is mandatory in profiles. 
 - Amended reference to incorrect GUID in ADW-Message-DischargeNoticeRejectResponse-1-0-Ex01 bundle xml example at Encounter.serviceProvider to reference the correct GUID for an organisation within the bundle.
 - Removed a duplicate email address for the Local Authority Contact within the ADW-Message-DischargeNoticeRejectResponse-1-0-Ex01 minimum dataset bundle xml example at Practitioner.telecom.
 - Removed all display elements from all references within all minimum dataset bundle xml examples.
 - Removed reference end tag in minimum dataset xml bundle examples in MessageHeader.requester element and corrected format of this reference element.
 - Corrected cardinality of QuestionnaireResponse.group.question element to 1..* for all messages.
 - Corrected any typos relating to capitalisation which unsynchronised profiles and minimum dataset bundle xml examples.
 - Removed Reason for Admission from QuestionnaireResponse structure definitions across all messages.
 - Corrected value in Patient.identifier.system (Hospital Patient identifier) to http://fhir.nhs.net/Id/hospital-patient-identifier for all response profiles and minimum dataset bundle xml examples.
 - Removed Patient.identifier.use element from Withdrawal and Discharge notice minimum dataset bundle xml examples.
 - Removed FixedCode value="official" from Patient profiles' Patient.name associated child element.
 - Status wrongly coded in Discharge questionnaire response.status element in ADW-Message-DischargeNotice-1-0-Ex01.xml. Removed incorrect extension to this element.  
   
 **Known Issues**
 
 - Question marks appear after the cardinality entries in the Control label on the dictionary pages. The cardinalities given in these instances are correct; this is a tooling issue which is currently under investigation.
 - There are inconsistencies in some of the descriptions in the dictionary/definition pages for profiles. Where this is the case, the profile tree view page takes precedence. The cause of this is currently under investigation.
 - The Profile Referencing Diagrams do not reflect changes from Draft G onwards and will be updated for the future RC2.
 - Xml examples for individual profiles and maximal bundle xml examples (suffixed Ex02) have not been updated and will be revised in RC3.
 
### Version: 1.0: Status: RC1 ###
 - The Reason for Admission element has been removed from Assessment message ADW Questionnaire Response profile and is now in a new ADW Condition profile. This is an important change, which was required to maintain compliancy with the FHIR standard.
 - Amended Assessment Notice ADW-Patient-1-0.communication.preferred and communication.interpreterRequired to be mandatory in line with Information Standard requirements.
 - Produced revised xml example bundles suffixed Ex01.xml to show only the minimum dataset elements from the Information Standard requirements.
 - Added mustSupport attribute to ADW-Practitioner-1-0.practitionerRole and its child role element.
 - Made ADW-Patient-1-0 generic; the same profile for all messages.
 - Added labels to elements in Patient, Practitioner and Organisation profiles in line with Dataset naming. 
 - Added cardinality for top level slice in Short description for all Patient, Practitioner, Organisation based profile slices.
 - Amended name of Assessment Notice ADW-QuestionnaireResponse-1-0.CHC Assessment Considered Indicator and Result to NHS CHC Assessment Considered Indicator and Result in line with Dataset requirements.
 - Amended name of Practitioner.telecom.value sliced element to email address string and telephone number string respectively for the two different slices.
 - Amended name of Patient.telecom.value sliced element to email address string and telephone number string respectively for the two different slices.
 - Amended name of Patient.contact.telecom.value sliced element to email address string and telephone number string respectively for the two different slices.
 - Verified Dataset mappings on adw-message-bundle-1-0 pages against Dataset requirements.
 - Produced minimum dataset-based bundles for all messages to show only those elements which are required to meet requirements. 
 - Added mustSupport attribute to ADW-Location-1-0.name element to support requirements. 
 - Added mustSupport attribute to all MessageHeaders for all elements with mandatory cardinality and for the responsible element.
 - Reinstated responsible element to Response MessageHeaders to provide optional link to either a responsible organisation or practitioner.
 - Amended ADW-Organization-1-0-Ex02 to show a Local Authority rather than a Local Authority Social Services department to reflect requirements.
 - Removed all unnecessary spaces from questions in all QuestionnaireResponse profiles.
 - Amended MessageHeader.receiver element to reference Local Authority Social Services community team instead of Social Worker practitioner in all Notice bundles.
 - Removed Local Authority Social Worker (Practitioner) from all Notice bundle examples.
 - Removed ServiceProvider element from all Encounter profiles in the minimum dataset bundle examples.
 - Amended Local Authority Social Services department organisation in bundle xml examples to show a Local Authority rather than a Local Authority Social Services' department to reflect Information Standard requirements more accurately.
 - Amended typo in all MessageHeaders.destination elements to adjust the label to (Local Authority Receiving System) rather than (Local Authority Receving System).
 - Amended slices for telecom elements in Patient and Practitioner-based profiles to Closed to reflect specification.
 - Amended ADW-Lead-Clinician-Practitioner-1-0.identifier (SDS Identifier) cardinality to 0..1.
 - Amended cardinality of ADW-Patient-1-0.identifier to 1..2 to reflect specification.
 - ADW-WithdrawalNotice-Message-Header-1-0.event.code now contains an example value rather than a fixed value to reflect specification for a choice of two possible values.
 - Re-ordered profiles in the messages and ordered profiles in bundle xml examples to match order in each message.
  
 **Known Issues**
 
 - Question marks appear after the cardinality entries in the Control label on the dictionary pages. The cardinalities given in these instances are correct; this is a tooling issue which is currently under investigation.
 - There are inconsistencies in some of the descriptions in the dictionary/definition pages for profiles. Where this is the case, the profile tree view page takes precedence. The cause of this is currently under investigation.
 - The Profile Referencing Diagrams do not reflect changes from Draft G onwards and will be updated for the future RC2.
 - Xml examples for individual profiles and maximal bundle xml examples (suffixed Ex02) have not been updated and will be revised in RC2.
### Version: 1.0: Status: Draft H ###
 - Added new value of "X" (Other) to adw-admission-type-1-0 valueset.
 - Amended cardinality of responsible element to 0..1 for all notice MessageHeader profiles to reflect requirements.
 - Removed responsible element from Response MessageHeader profiles to reflect specification. This will be reviewed in next draft.
 - Amended author, receiver and responsible elements for all notice and response MessageHeaders to reference practitioner and organisation or practitioner only.
 - Sliced Patient.telecom and Patient.contact.telecom to reflect specification with cardinality of 0..2 and showing email and telephone contact details only for Assessment Notice.
 - Removed Patient.telecom and Patient.communication and sliced Patient.contact.telecom from Patient profile in 
 - Discharge notice as above to reflect specification.
 - Removed Patient.telecom, Patient.communication and all Patient.contact details from Patient profile in Withdrawal message to reflect specification.
 - Removed Patient.telecom, Patient.address, Patient.communication, Patient.managingOrganization and all Patient.contact details from all Responses to reflect specification.
 - Created new ADW-Lead-Clinician-Practitioner-1-0 profile to reflect requirements for a Lead Clinician.
 - Created new ADW-Social-Services-Team-Organization-1-0 profile to reflect requirements for a Social Services team.
 - Amended ADW-Practitioner-1-0 profile to reflect requirements for email and telephone contact details. 
 - Amended Encounter.location cardinality to 0..* for all Encounter-based profiles.
 - Amended values and renamed administrative gender valueset for Patient.gender to person-stated-gender-1-0 to reflect specification.
 - Added mandatory reason element to Withdrawal and Response MessageHeaders.
 - Removed reference to Composition profile in Assessment Notice and Discharge Notice Encounter profiles supportingInformation elements.
 - Amended all xml examples and bundles to reflect above changes.
### Version: 1.0: Status: Draft G ###
 - Changed Ward from an Organisation to a Location resource. Added in to all messages.
 - Created revised corresponding Ward xml example and deleted existing Ward xml example.
 - Added revised Ward xml example to all bundles and removed previous Ward xml example.
 - Added ADW-Response-Encounter-1-0 to all responses to link Ward into all messages.
 - Created Response encounter xml examples for all responses.
 - Added location element to all Encounter profiles to reference a Hospital Ward.
 - Amended identifier.value in all Encounter xml examples to make it the same for all.
 - Updated Referral in Withdrawal and all Response messages to reference newly created Encounter profiles.
 - Updated all bundles with xml example changes.
 - Added "Not Applicable" as extra value to adw-third-party-consent-source-1-0 valueset.
 - Changed values in adw-admission-type-1-0 valueset to "P" (Elective) and "E" (Emergency).
 - Amended ADW-Encounter-1-0-Ex01 and ADW-Message-AssessmentNotice-1-0-Ex01 xml examples to reflect changed adw-admission-type-1-0 values.
 - Amended example identifier.value in all Referral profiles to make it the same for all.
### Version: 1.0: Status: Draft F ###
 - Updated all xml examples and added unique UUIDs for all.
 - Amended ADW-Discharge-Composition xml example to reflect its profile.
 - Updated all profile referencing diagrams to reflect revised UUID allocation.
### Version: 1.0: Status: Draft E ###
 - Removed placeholder Bundle XML examples from DMS.
 - Added ADW Data set Mapping tables to ADW-Message-Bundle.html for every message.
 - Added  Profile Referencing diagrams to ADW-Message-Bundle.html for every message.
 - Added Social Worker Practitioner xml example.
 - Added ADW-ReferralRequest-Cancelled-1-0 to Withdrawal Notice Accept Response and Withdrawal Notice Reject response.
 - Removed organisation link from the author element in all Message Headers. 
### Version: 1.0: Status: Draft D ###
This release accommodates the changes following review by the NHS Digital business and the technical modelling teams. It includes the following changes:

 - Renamed the specification from Social Care Integration to Social Care.
 - Added more detailed XML examples.  
- Added complete message (bundle) examples.  
- Added diagram to illustrate the referencing for a typical Assessment Notice message.  
- Added table for FHIR message element to ADW dataset mapping.
### Version: 1.0: Status: Draft C ###
- Updated ADW-WithdrawalNotice-Message-Header-1-0 to include reason for withdrawal.
### Version: 1.0: Status: Draft B ###
- Second draft of the SCI Message Specification was created to resolve the broken links in the previous release.
### Version: 1.0: Status: Draft A ###
- First draft of the Social Care Integration Domain (SCI) Message Specification.


 


